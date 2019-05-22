---
title: "Frequently asked questions"
description: "Frequently asked questions about Dynamics 365 Virtual Agent for Customer Service."
ms.date: 05/21/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
author: m-hartmann   
ms.author: mhart
manager: shellyha
---

# Frequently asked questions

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

- [General](#general)
    - [What are the various browsers supported by the Virtual Agent?](#what-are-the-various-browsers-supported-by-the-virtual-agent)
    - [Can Virtual Agent be styled and branded for an organization? What can be customized and how?](#can-virtual-agent-be-styled-and-branded-for-an-organization-what-can-be-customized-and-how)
    - [Can multiple team members collaborate on a single bot instance?](#can-multiple-team-members-collaborate-on-a-single-bot-instance)
    - [Can I do end user authentication using AAD or MSA from within the bot?](#can-i-do-end-user-authentication-using-aad-or-msa-from-within-the-bot)
    - [Virtual Agent Designer does not seem to allow us to store the user utterance that triggered the topic as a variable, is that by design?](#virtual-agent-designer-does-not-seem-to-allow-us-to-store-the-user-utterance-that-triggered-the-topic-as-a-variable-is-that-by-design)
    - [I ran into a problem. What should I do to file a bug? How quickly will you get back to me?](#i-ran-into-a-problem-what-should-i-do-to-file-a-bug-how-quickly-will-you-get-back-to-me)
    - [I have a new feature idea or some ideas on how to make a feature work better. How should I submit these ideas to the product team?](#i-have-a-new-feature-idea-or-some-ideas-on-how-to-make-a-feature-work-better-how-should-i-submit-these-ideas-to-the-product-team)
- [Bot creation and environments](#bot-creation-and-environments)
    - [Why do I get an error that I do not have permissions to any environments?](#why-do-i-get-an-error-that-i-do-not-have-permissions-to-any-environments)
    - [Why do I get "An unexpected server error occurred"?](#why-do-i-get-an-unexpected-server-error-occurred)
    - [Why does my bot creation time out after a long delay?](#why-does-my-bot-creation-time-out-after-a-long-delay)
    - [The PowerApps environment I created does not show up in the down menu of Virtual Agent, why?](#the-powerapps-environment-i-created-does-not-show-up-in-the-down-menu-of-virtual-agent-why)
    - [What is the cost involved in using Microsoft Flow Actions in Virtual Agent?](#what-is-the-cost-involved-in-using-microsoft-flow-actions-in-virtual-agent)
- [Topic creation and management](#topic-creation-and-management)
    - [How do I create my own custom Topic?](#how-do-i-create-my-own-custom-topic)
    - [How can I test topics that I've customized or created from scratch to make sure they are working properly?](#how-can-i-test-topics-that-ive-customized-or-created-from-scratch-to-make-sure-they-are-working-properly)
    - [I saved my content but when I test the bot, it doesn't seem to reflect my edits. What's happening?](#i-saved-my-content-but-when-i-test-the-bot-it-doesnt-seem-to-reflect-my-edits-whats-happening)
    - [Is it possible to link multiple topics?](#is-it-possible-to-link-multiple-topics)
    - [Is it possible to launch the bot to address a specific topic from a link on the page?](#is-it-possible-to-launch-the-bot-to-address-a-specific-topic-from-a-link-on-the-page-the-scenario-we-have-in-mind-is-a-list-of-linksactions-on-the-page-and-a-couple-of-them-will-launch-a-topic-on-the-bot)
- [Flow integration](#flow-integration)
    - [How do I create a Microsoft Flow action in Virtual Agent?](#how-do-i-create-a-microsoft-flow-action-in-virtual-agent)
    - [What license do I need to use Microsoft Flows in Virtual Agent?](#what-license-do-i-need-to-use-microsoft-flows-in-virtual-agent)
    - [I created some new flows for actions using Microsoft Flow, but they are not visible in Virtual Agent. Why?](#i-created-some-new-flows-for-actions-using-microsoft-flow-but-they-are-not-visible-in-virtual-agent-why)
    - [I created a flow with HTTP Request trigger, and it's visible in my Bot, but when I test my Topic, it fails. Why?]
    - [What are the response formats that the Virtual Agent accepts, especially in the message response provided by the Flow action?](#what-are-the-response-formats-that-the-virtual-agent-accepts-especially-in-the-message-response-provided-by-the-flow-action)
    - [Can we call a third-party API from a Flow?](#can-we-call-a-third-party-api-from-a-flow)
    - [Can we call a third-party API directly from the Virtual Agent action, without going through a flow?](#can-we-call-a-third-party-api-directly-from-the-virtual-agent-action-without-going-through-a-flow)
    - [How do I work with my data in Microsoft Flow?]
    - [If we have authentication for the user, can we pass user authentication info to a flow?])
    - [Can I share the flows I created with other users?]
    - [How do I move or copy my flows between different envrironments?]
    - [Where can I find out more about Microsoft Flows?]
- [Deployment](#deployment)
    - [How do I share my bot with others?](#how-do-i-share-my-bot-with-others)
    - [How I install the bot in a Modern SharePoint site? Is there any additional work that will be required if the given Modern SharePoint restricts embedding code from external sites?](#how-i-install-the-bot-in-a-modern-sharepoint-site-is-there-any-additional-work-that-will-be-required-if-the-given-modern-sharepoint-restricts-embedding-code-from-external-sites)
- [Analytics](#analytics)
    - [What is the difference between conversation and session? How do sessions work?](#what-is-the-difference-between-conversation-and-session-how-do-sessions-work)

## General 

### What are the various browsers supported by the Virtual Agent?

Virtual Agent is supported in the latest versions of Edge, Chrome, and Fire Fox. It is not supported in Internet Explorer.
 
### Can Virtual Agent be styled and branded for an organization? What can be customized and how?

Currently we don't have any styling or brand customization (e.g. changing the default image) for the bot. But this is on the roadmap for a future release.

### Can multiple team members collaborate on a single bot instance?

We don’t have multi author support currently. It is one bot per author. However, we have this feature on the roadmap for future releases. The current mitigation is to create a service account and share it across the content authors.

### Can I do end user authentication using AAD or MSA from within the bot?

We currently do not support any authentication from within the Virtual Agent. However, native support for end user authentication is on the roadmap.

### Virtual Agent Designer does not seem to allow us to store the user utterance that triggered the topic as a variable, is that by design?

Yes, Virtual Agent currently doesn't allow storing the user utterance that triggered the topic as a variable. This feature is on the roadmap for a future release.

### I ran into a problem. What should I do to file a bug? How quickly will you get back to me? 

You can file bugs in the in the [community forum](https://go.microsoft.com/fwlink/?linkid=2058639). We will respond within 48 hrs.
### I have a new feature idea or some ideas on how to make a feature work better. How should I submit these ideas to the product team?

That's great, we'd love to hear your thoughts. [Submit your ideas and feedback in our Idea forum](https://go.microsoft.com/fwlink/?linkid=2064961).


## Bot creation and environments

### Why do I get an error that I do not have permissions to any environments?

It is possible that you do not have read/write access to any environments. In this case, you will see the error: “You do not have permissions to any environments. Please get access from an administrator.” 
To resolve this issue, follow the steps in [To create a new PowerApps environment](getting-started-new-environment.md) to create a new environment. Use that environment to create your bot.

### Why do I get "An unexpected server error occurred"?

Is it possible that you do not have sufficient priveleges for the selected environment. Ideally the region (environment) dropdown UI should only contain environments a user has read/write access to; however, the dropdown is not currently constrained to this. If you select an environment that you have has insufficient access to, you will get the following error: “An unexpected server error occurred. Please retry creating your bot.”
To resolve this issue, follow the steps in [To create a new PowerApps environment](getting-started-new-environment.md) to create a new environment. Use that environment to create your bot.

### Why does my bot creation time out after a long delay?

When creating the first bot in an environment, there is a known issue where the bot creation takes a long time and either eventually succeeds and lands the user on the Virtual Agent home screen, or errors out. If an error occurred and you are sure you had sufficient environment privileges (i.e., you created the environment as guided above), then proceed with refreshing your browser. After the refresh, in most cases, you will find that the bot creation succeeded despite the error; else retry the bot creation again.

### The PowerApps environment I created does not show up in the down menu of Virtual Agent, why?

Please check if you selected the Region as "USA" while creating the Power Apps (Common Data Service) environment. Currently we support only environments in USA. If you created an environment in other regions, it won't be shown in Virtual Agent. The workaround is to create a new environment with location as "USA" or use an existing environment that was created in "USA" region.

### What is the cost involved in using Microsoft Flow Actions in Virtual Agent?

A Flow license is per user. Users get Flow licenses automatically when they get a Bot license (which is based on number of sessions). There may be a limit for how many Bot Author (P2 Flow licenses) you can have based on the bracket of Bot license you purchased. 

Here is how the flow licensing works in the context of the bot license.
If you have 10 bot authors in your organization:
 - each of them gets a P2 Flow license
 - every P2 license comes with 15K Flow "runs" per month
Flow runs are "pooled" and the runs are anonymous - so the org actually gets 10x15K Flow runs any Flow can use. Now, this 10x15K is a big number to have for a month, and they can be used by any Flow anyone has created.
The "1 min execution throttle" only applies to "auto-run" type of Flows and does not apply to Bot Flows. This throttle is only for the Flows that are set up to run automatically in a loop, like "every 1 min, check if there are new emails in my Inbox".


## Topic creation and management  

### What is a bot and a topic? 

A bot is a collection on Topics.  Topics may be authored – customized from provided templates, or created from scratch.  

### What is the difference between a System topic and a provided template User topic? 

A System topic are linked to provided features like a customer survey, escalate to a live agent or the bot greeting.  Some areas of the System topics may be modified but others are not.  All parts of a the provided User Topics may be modified or deleted.  They are for your customization to fulfull the needs of your Virtual Agent bot. 

### How do I create my own custom Topic?  

You can find all details about creating your own topics in this article: [Creating custom topics for your bot](getting-started-create-topics.md)

### How can I test topics that I've customized or created from scratch to make sure they are working properly?
The Virtual Agent Designer includes a Test Bot, where you can test your virtual agent and view how the conversation you designed in the conversation editor works in practice. 
You can test a virtual agent topic by entering a trigger phrase for the topic at the "Type your message" prompt at the bottom of the Test Bot.  Click on any chat bubble to navigate to that point in the conversation. 

### I saved my content but when I test the virtual agent in the Test Bot, it doesn't seem to reflect my edits.  What's happening? 
You need to make sure to hit "Save" on the Topic you're editing and then hit the "Start over" button in the Test Bot to ensure the latest content gets updated in the chat canvas when testing your virtual agent. 

### What is the Green outline that appears while I'm testing my topic? 

The Green outline appears around each node that is successfully tested while using the Test Bot. Those nodes that fail will be outlined in red. 

### What is “Follow” toggle switch in Test Bot? 
Turn on Follow to ajump between topics while testing your bot. The conversation on the right will update simultaneously. Click on any chat bubble to navigate to that point in the conversation. 

### What is Topic Checker? 
Topic Checker is where you can see a comprehensive list of all errors and warnings in your Topic.  Errors and Warnings can be saved with a Topic and cleared upon subsequent visits.  Errors should be cleared up before Deploying your bot to production, else unexpected behavior may occur.  Warnings are skipped by the Bot. 

### Is it possible to link multiple topics?
You can link a different topic within a topic by using the **Go To** option which appears while adding a new node in the dialog flow of a topic.

### Is it possible to launch the bot to address a specific topic from a link on the page? The scenario we have in mind is a list of links/actions on the page and a couple of them will launch a topic on the bot.

Currently we don't support context passing in the bot, so you will not be able to launch the bot or trigger a specific topic based on a link or action on the web page. 
Some inofficial workarounds you may want to consider: deploy the Bot on a custom page, and launch that page as an iframe or pop-up from the parent web page, when the link or action is launched.
For triggering specific topics you could have multiple bots, and have the Topic content added as part of the Greeting, which always appears when starting a conversation. The downside is that it will be cumbersome to maintain multiple bots for different sets of links/actions.

### What’s a variable and how do I use it? 

Variables store customer responses to Bot questions.  Variables can further be used in expressions evaluating a customer response or passed to a Flow.  Variables can also be used to confirm a customer response. 

## Flow integration 

### How do I create a Microsoft Flow action in Virtual Agent?

A: Here is a [video on how to create a Microsoft Flow action](https://go.microsoft.com/fwlink/?linkid=2079323) that can be executed from Virtual Agent.

### What license do I need to use Microsoft Flows in Virtual Agent?

Every bot author will be automatically licensed to use Microsoft Flows. No extra steps are needed, as bot authors will be assigned a P2 Plan Flow license as part of their Virtual Agent license. For details, please refer to [Microsoft Flow Plans documentation](https://flow.microsoft.com/en-us/pricing/).
### I created some new flows for actions using Microsoft Flow, but they are not visible in Virtual Agent. Why?

- The environment you are using to create your flows must be the same as the environment you are using for the bot.   
- Make sure to [create your Flows in Solutions](https://docs.microsoft.com/en-us/flow/overview-solution-flows), as the Bot cannot see the Flows created in My Flows tab. 
- Bots can only invoke Flows that have HTTP Request interfaces, so you need to select the right trigger for your Flow. Select **When Http Request is received** from the trigger list in the Microsoft Flow, and make sure you are using the **POST** method under advanced options in the trigger (or leave the method field empty, how it is by default). 

View this video on how to [create a Flow action](https://go.microsoft.com/fwlink/?linkid=2079323) that can be used with bots. 

### I created a flow with HTTP Request trigger, and it's visible in my Bot, but when I test my Topic, it fails. Why?
Please make sure this Flow is Turned On (enabled) on Flow portal. The Flows which are Turned Off (disabled) on Flows portal are visible to the Bot Designer and can be incorporated into an Action in the Dialog, but will fail at runtime until they are Turned On.

### What are the response formats that the Virtual Agent accepts, especially in the message response provided by the Flow action?

The Virtual Agent designer accepts only JSON object format in the message response. The JSON object can contain strings and numbers only. In the coming months, we will release a custom Flow connector that will make it easier to create Flows using key/value pairs rather than requring to use JSON format.  We do not support arrays as Flow output for Bots yet, but this feature is on the roadmap. 

### Can we call a third-party API from a Flow?

Yes, an existing API or another application can be called from a Flow and the results can be passed back to the Virtual Agent as Flow output. Microsoft Flow provides hundreds of Connectors to enable you to connect to apps, data and devices in the cloud. 

Examples of popular connectors include Microsoft Common Data Service (CDS), Salesforce, Zendesk, ServiceNow, Office 365, Microsoft Teams, Slack, Facebook, Twitter, Dropbox, MailChimp, Google services, and many more. Please refer to [Microsoft Flow Connector documentation](https://docs.microsoft.com/en-us/connectors/) to see the full list of avalaible Flow Connectors.

If there is no suitable Connector that you can use out of the box in Flow, you can use an HTTP call inside a Flow to connect to a custom 3rd-party API, like in the example below:
![Connect to 3rd party API](media/connect-API-flow.png)


### Can we call a third-party API directly from the Virtual Agent action, without going through a flow?

This capability is not currently available directly from the Virtual Agent experience, but you can call any third-party API by wrapping the call in a Flow. If this feature is critical to your business, please [submit your ideas and feedback in our Idea forum](https://go.microsoft.com/fwlink/?linkid=2064961).


### How do I work with my data in Microsoft Flow?
Microsoift Flow provides [hundreds of data Connecors](https://docs.microsoft.com/en-us/connectors/) and offers many ways to manipulate you data. Please refer to the following Microsoft Flow documentation on more information on how to:
- [Use Common Data Service (CDS)](https://docs.microsoft.com/en-us/flow/connection-cds)
- [Create a flow that uses the Common Data Service](https://docs.microsoft.com/en-us/flow/common-data-model-intro)
- [Create multi-step flows](https://docs.microsoft.com/en-us/flow/multi-step-logic-flow)
- [Add condition in a flow](https://docs.microsoft.com/en-us/flow/add-condition)
- [Use expressions with conditions](https://docs.microsoft.com/en-us/flow/use-expressions-in-conditions)
- [Use functions in expressions](https://docs.microsoft.com/en-us/azure/logic-apps/workflow-definition-language-functions-reference)
- [Perform data operations](https://docs.microsoft.com/en-us/flow/data-operations)
- [Loop through your data](https://docs.microsoft.com/en-us/flow/apply-to-each)
- [Filter and copy data](https://docs.microsoft.com/en-us/flow/odata-filters)
- [Troubleshoot your flow](https://docs.microsoft.com/en-us/flow/fix-flow-failures)

### If we have authentication for the user, can we pass user authentication info to a flow?

Currently, passing end user authentication to a Flow is not supported in Virtual Agent, but we have this feature on the Roadmap and will be enabled over the coming months.  We will start with token-based authentication.  If you have specific authentication requirements that you would like us to be aware of, please [submit your ideas and feedback in our Idea forum](https://go.microsoft.com/fwlink/?linkid=2064961).

### Can I share the flows I created with other users?
You can add other users in you orgnization as owners of the flows you have created. Please click on the flow to open its Details page, and select "Add another owner" option in Owners section:
![Add another owner](media/add-flow-owner.png)

### How do I move or copy my flows between different envrironments?
You can export and import Solutions containing your flows to move them between eniornments. Note that there is currently no way to exposrt or import a single flow. For more information on how to import and export Solutions, plesae refer to Microsoft Flow documentation on how to:
- [Export a Solution](https://docs.microsoft.com/en-us/flow/export-flow-solution)
- [Import a Solution](https://docs.microsoft.com/en-us/flow/import-flow-solution)

### Where can I find out more about Microsoft Flows?
You can find out more about the capabilities of Microsoft Flows on [Frequently asked quetsions](https://docs.microsoft.com/en-us/flow/frequently-asked-questions) page or by using [Flow documentation](https://docs.microsoft.com/en-us/flow/getting-started).
You can also learn new skills and discover the power of Microsoft Flow with step-by-step [Flow training modules](https://docs.microsoft.com/en-us/learn/browse/?products=flow).

## Deployment 

### How do I share my bot with others?

You find the details in this article: [To share your bot in the demo website](getting-started-deploy.md#to-share-your-bot-in-the-demo-website)

### How I install the bot in a Modern SharePoint site? Is there any additional work that will be required if the given Modern SharePoint restricts embedding code from external sites?

If the Modern SharePoint site allows embedding an iframe, it should be able to embed the bot. We have an iframe code snippet that you can get for your respective bot by going to the **Deploy** page. That snippet can be pasted in any html web page and from there you should see your bot appear. You can get this code to embed in your SharePoint site from **Deploy** > **Custom Website** in Virtual Agent.


## Analytics 

### What is the difference between conversation and session? How do sessions work? 

A conversation is the entire interaction between the bot and a user, starting from the user’s first message to when the chat window is closed or inactive for about an hour. Within a conversation, the user may have more than one query. 
A session is intended to capture just one query or problem within a conversation. So, a conversation can have multiple sessions. A session starts with the user’s initial query and ends when the user indicates the problem is solved (confirmed success topic) or the session is escalated (escalation topic).
