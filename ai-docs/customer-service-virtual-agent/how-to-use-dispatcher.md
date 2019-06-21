---
title: "Using your existing Bot Framework bot with Dynamics 365 Virtual Agent for Customer Service"
description: "Step by step guidance on using an existing Bot Framework bot with Dynamics 365 Virtual Agent for Customer Service"
ms.date: 06/17/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Using your existing Bot Framework bot with Dynamics 365 Virtual Agent for Customer Service

## Overview 

This document covers the following steps to use Microsoft Bot Framework's dispatcher tool and integrate your existing bot with your Dynamics 365 Virtual Agent for Customer Service bot,

* A. [Retrieve topics, utterances and secrets from your virtual agent tenant](#a-retrieve-topics-utterances-and-secrets-from-your-virtual-agent-tenant)
* B. [Train dispatcher custom model with your virtual agent's topics](#b-train-dispatcher-custom-model-with-your-virtual-agents-topics)
* C. [Register and trigger your new dispatch endpoint in code](#c-register-and-trigger-your-new-dispatch-endpoint-in-code)
* D. [Deploy your bot & test dispatcher](#d-deploy-your-bot--test-dispatcher)

## Pre-requisites

  * Bot build using Microsoft Bot Framework Bot Builder v4 SDK
  * Visual Studio 2017 or higher - [click here to download](https://visualstudio.microsoft.com/vs/)
  * Understanding of Microsoft Bot Framwork's dispatcher tool. [Read more](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-tutorial-dispatch?view=azure-bot-service-4.0&tabs=csaddref%2Ccsbotconfig)
  * Understanding how to test & debug bots using Bot Framework Emulator - [Learn more](https://docs.microsoft.com/en-us/azure/bot-service/bot-service-debug-bot?view=azure-bot-service-4.0)

### Code samples & dependencies
Code snippets used in this document are available below.

  * [Bot Framework Dispatcher app sample](https://github.com/Microsoft/BotBuilder-Samples/tree/master/samples/csharp_dotnetcore/14.nlp-with-dispatch)
  * [TO DO - Dynamics Bot Content Converter](https://msazure.visualstudio.com/CCI/_git/Users?path=%2Fsabacha%2FCCIToLU&version=GBmaster)
  * [Microsoft Bot Framework LU down utility](https://github.com/microsoft/botbuilder-tools/tree/master/packages/Ludown)
  * [Nuget packet manager](https://nodejs.org/en/)
  * [.NET Core 2.1 runtime](https://dotnet.microsoft.com/download/thank-you/dotnet-sdk-2.1.700-windows-x64-installer)

### A. Retrieve topics, utterances and secrets from your virtual agent tenant
First, we will need to retrieve retrieve your Dynamics Bot content (topics & utterances) and your tenant’s endpoint and direct line secret.

#### 1.	Retrieve bot ID, tenant ID, and auth token from your bot

1.	Open Developer Tools (F12) for your web browser

2.	Sign-in to your Virtual Agent using your AAD credentials http://va.ai.dynamics.com

3.	Go to `Network Tab` (see screenshot below)
      <TO DO - Screenshot>

4.	Filter and look for “client” request (see screenshot below)
      <TO DO - Screenshot>

5.	Copy and persist the following details (see screenshot below)
```javascript
signedInUserAccountInfo.defaultBot.aadTenantId
signedInUserAccountInfo.defaultBot.id
signedInUserAccountInfo.defaultBot.name
```
<TO DO - Screenshot>

6.	Store the above information on your PC - you will need it later.

#### 2. Retrieve topics and utterances from your bot
  1.	Export `BotContent` and `Annotations` from Common Data Store. [Click here for instructions](https://docs.microsoft.com/en-us/dynamics365/ai/customer-service-virtual-agent/gdpr-export).
  2.  Content will be exported and downloaded as a zip file 
        (e.g. `ExportedFiles_1c5d21e9-1d25-4759-a622-0e232a49e197.zip`)
  3.  Unzip the file to find two CSV files - `annotations.csv` and `msdynce_botcontents.csv`
  
#### 3. Convert the exported content to LU format
  1.  Convert your bot content into LU format using our [TO DO - sample "ContentConverter" utility]()
    Note: You will need to use Visual Studio to compile this sample.
  2. Once compiled and built, use the following command to convert your virtual agent topics & utterances into LU format
```
Content-Converter.exe -botinfo msdynce_botcontents.csv -botcontent annotations.csv -botid <bot id>
```
3. Convert LU file to LUIS Json file format
```
ludown parse ToLuis --in content.lu
```

### B. Train dispatcher custom model with your virtual agent's topics
Follow these steps to train and recreate the dispatcher app and add your exported topics & utterance with your existing Cognitive Service’s intents (eg. LUIS and/or QnA maker) using the dispatch tool. For more information, [follow guidance here](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-tutorial-dispatch?view=azure-bot-service-4.0&tabs=cs).

####  1.  Install the dispatch tool (using npm)
```
CMD> npm install -g botdispatch
```

####  2.  Add exported topics & utterances (exported from step 2 above) using the dispatch tool.

```
CMD> dispatch add -type file -name l_cci -f luis.json
Please enter required field(s) below.

What name would you like for your dispatch:
l_cci
What's your LUIS authoring key (from https://www.luis.ai/user/settings):
<enter authoring key>
What's your LUIS authoring region [westus, westeurope, australiaeast]:
<pick your region: eg. westus>
File: content.lu added to l_cci.dispatch
```

####  3.  Generate a dispatch model containing exported topics & utterances
    a. Note that you will need to re-train your dispatcher model as more intents are added in future

```
CMD> dispatch create

Exporting services for dispatch...
Creating dispatch LUIS model json...
Creating training data...
Updating l_cci model...
Importing l_cci model...
Setting up intents to child services mapping for l_cci...
Add subscription key and publish child LUIS apps...
Training l_cci model...
Publishing l_cci model...
Writing summary file ('test_prediction')...
{
  "authoringRegion": "westus",
  "hierarchical": true,
  "useAllTrainingData": false,
  "dontReviseUtterance": false,
  "copyLuisData": true,
  "services": [
    {
      "path": "luis.json",
      "type": "file",
      "name": "l_cci"
    }
  ],
  "serviceIds": [
    "1"
  ],
  "appId": "<REDACTED>",
  "authoringKey": "<REDACTED>",
  "version": "Dispatch",
  "region": "westus",
  "type": "dispatch",
  "name": "l_cci"
}
Please review your dispatch model in ..\Summary.html
```

### C. Register and trigger your new dispatch endpoint in code
The following steps will require you to add code that registers your new dispatch endpoint and trigger it everytime a user's utterance matches intent. We are using the [following sample](https://github.com/Microsoft/BotBuilder-Samples/tree/master/samples/csharp_dotnetcore/14.nlp-with-dispatch) provided by Microsoft Bot Framework team.

####  1.  Update `appsettings.json` in your dispatcher app to include the new endpoint for Virtual agent
  
```csharp
{
  "CCIBotId": "<Bot Id>",
  "CCITenantId": "<Tenant Id>",
  "CCIBotName": "<Bot Name>",
  "CCITokenEndpoint": "https://va.ai.dynamics.com/api/botmanagement/v1/directline/directlinetoken",
}
```

####  2. Add a new `DynamicsBot` class to your project

```csharp
public class DynamicsBot
{
  private readonly HttpClient _httpClient;

  public DynamicsBot(CCIEndpoint endpoint, string botName)
  {
    Endpoint = endpoint;
    BotName = botName;
    _httpClient = new HttpClient();
  }

  public string BotName { get; }

  public CCIChannelData ChannelData { get; }
  public CCIEndpoint Endpoint { get; }

  public async Task<string> GetTokenAsync()
  {
    var httpRequest = new HttpRequestMessage();
    httpRequest.Method = new HttpMethod("GET");
    httpRequest.RequestUri = Endpoint.TokenUrl;
    var response = await _httpClient.SendAsync(httpRequest);
    var responseStr = await response.Content.ReadAsStringAsync();
    return SafeJsonConvert.DeserializeObject<DirectLineToken>(responseStr).token;
  }
}

public class DynamicsBotChannelData
{
  public DynamicsBotChannelData(string botId, string tenantId, string contentVersion)
  {
    cci_bot_id = botId;
    cci_tenant_id = tenantId;
  }

  public string cci_bot_id { get; }
  public string cci_tenant_id { get;  }
}

public class DynamicsBotEndpoint
{
  public DynamicsBotEndpoint(string botId, string tenantId, string tokenEndPoint)
  {
    BotId = botId;
    TenantId = tenantId;
    TokenEndPoint = tokenEndPoint;
    UriBuilder uriBuilder = new UriBuilder(tokenEndPoint);
    uriBuilder.Query = $"botId={BotId}&tenantId={TenantId}";
    TokenUrl = uriBuilder.Uri;
  }

  public string BotId { get; }

  public string TenantId { get; }

  public string TokenEndPoint { get; }

  public Uri TokenUrl { get; }
}

public class DirectLineToken
{
  public string token { get; set; }
}
```

####  3.  Add a reference to Dynamics bot in `IBotServices.cs` file
  
 ```csharp
public interface IBotService
{
  LuisRecognizer Dispatch { get; }
  QnAMaker SampleQnA { get; }
  CCIService CCIService { get; }
}
 ```
 
####  4. Update BotServices constructor to instatiate `DynamicsBotService` in `BotServices.cs` file

```csharp
DynamicsBotService = new DynamicsBotService(new CCIEndpoint(
    configuration["DynamicsBotId"],
    configuration["DynamicsBotTenantId"],
    configuration["DynamicsBotTokenEndpoint"]),
    configuration["DynamicsBotName"]
);
```
  
####  5.  Update file `DispatchBot.cs` to add trigger Dynamics Bot on intent match
  
```csharp
private async Task ProcessDynamicsBotAsync(ITurnContext<Microsoft.Bot.Schema.IMessageActivity> turnContext, CancellationToken     cancellationToken)
{
    var token = await _botService.DynamicsBotService.GetTokenAsync();

    using (var directLineClient = new DirectLineClient(token))
    {
        var conversation = await directLineClient.Conversations.StartConversationAsync();
        var conversationtId = conversation.ConversationId;

        var response = await directLineClient.Conversations.PostActivityAsync(conversationtId, new Microsoft.Bot.Connector.DirectLine.Activity()
        {
            Type = Microsoft.Bot.Connector.DirectLine.ActivityTypes.Message,
            From = new Microsoft.Bot.Connector.DirectLine.ChannelAccount { Id = "userId", Name = "userName" },
            Text = turnContext.Activity.Text,
            ChannelData = JObject.FromObject(_botService.DynamicsBotService.ChannelData),
            TextFormat = "plain",
            Locale = "en-Us",
        });

        Thread.Sleep(4000);

        var activities = await GetActivitiesAsync(directLineClient, conversationtId, _botService.DynamicsBotService.BotName);

        var activity = turnContext.Activity as Microsoft.Bot.Schema.Activity;

        await turnContext.SendActivitiesAsync(
                   activities
                   .Select(message =>
                   {
                       var reply = activity.CreateReply(message.Text);
                       reply.Attachments = message?.Attachments?.Select(a => new Microsoft.Bot.Schema.Attachment()
                       {
                           Content = a.Content,
                           ContentType = a.ContentType,
                           ContentUrl = a.ContentUrl
                       }).ToList();

                       reply.SuggestedActions = new Microsoft.Bot.Schema.SuggestedActions()
                       {
                           Actions = message?.SuggestedActions?.Actions?.Select(a => new Microsoft.Bot.Schema.CardAction()
                           {
                               Title = a.Title,
                               Value = a.Value,
                               Type = a.Type,
                               Image = a.Image
                           }).ToList(),
                       };

                       return reply;
                   })
                   .ToArray());
    }
}

private async Task<List<Microsoft.Bot.Connector.DirectLine.Activity>> GetActivitiesAsync(DirectLineClient directLineClient, string conversationtId, string botName)
{
    ActivitySet response = null;
    List<Microsoft.Bot.Connector.DirectLine.Activity> result = new List<Microsoft.Bot.Connector.DirectLine.Activity>();
    string watermark = null;

    do
    {
        response = await directLineClient.Conversations.GetActivitiesAsync(conversationtId, watermark);
        watermark = response.Watermark;

        result = response?.Activities?.Where(x =>
          x.Type == Microsoft.Bot.Connector.DirectLine.ActivityTypes.Message &&
            string.Equals(x.From.Name, botName, StringComparison.Ordinal)).ToList();

        if (result != null && result.Any())
        { return result; }

        Thread.Sleep(1000);
    } while (response.Activities.Any());

    return result;
}
```

####  6.  If you want your Dynamics bot to handle unmatched intents for a single fallback, update method `DispatchToTopIntentAsync`
  
```csharp
case "l_cci":
case "None":
default:
    await ProcessDynamicsBotAsync(turnContext, cancellationToken);
    break;
```


### D. Deploy your bot & test dispatcher
We're ready to test our dispatcher to ensure seamless interaction between Dynamics bot and your other bots.

####  1.  Deploy your Dynamics bot using [instructions provided here](https://docs.microsoft.com/en-us/dynamics365/ai/customer-service-virtual-agent/getting-started-deploy#to-share-your-bot-on-the-demo-website).
  <TO DO - Add screenshot for deploy>
  
####  2.  Build (Ctrl + Shift + B) and run (F5) your dispatcher app
  
####  3.  Open Bot Emulator, add the name and endpoint to your bot.
  <TO DO - Add bot emulator screenshot>
  
## Conclusion
Dynamics 365 Virtual Agent for Customer enables businesses to seamlessly interact with existing bots using dispatcher.
