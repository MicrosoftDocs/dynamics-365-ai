---
title: "Frequently asked questions for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Frequently asked questions for Dynamics 365 Sales Insights"
keywords: " "
ms.date: 10/01/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 848a488e-27ce-41e1-892b-bb8613b5da1c
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Frequently asked questions

## General

**What languages are supported now?**<br>
Sales insights supports the following languages:<br>

| Feature | Language supported |
|---------|--------------------|
| Assistant, Assistant studio, Auto capture, Email engagement, Predictive lead scoring, Predictive opportunity scoring, Premium forecasting, Relationship analytics, Sales accelerator, and Who knows whom | Arabic, Basque, Bulgarian, Catalan, Chinese Simplified (PRC), Chinese Traditional (Hong Kong SAR), Chinese Traditional (Taiwan), Croatian, Czech, Danish, Dutch, English, Estonian, Finnish, French, Galician, German, Greek, Hebrew, Hindi, Hungarian, Indonesian, Italian, Japanese, Kazakh, Korean, Latvian, Lithuanian, Malay, Norwegian, Polish, Portuguese (Brazil), Portuguese (Portugal), Romanian, Russian, Serbian (Cyrillic), Serbian (Latin), Slovakian, Slovenian, Spanish, Swedish, Thai, Turkish, Ukrainian, and Vietnamese. |
| Talking points, Notes analysis, and Exchange insight cards in Assistant | Supports only English - United States (en-US) for machine learning models. |
| Activity-content based Auto capture |- For contact suggestions, the body of emails and meetings are analyzed in English and French.<br>- For activity suggestions, the body of emails and meetings are analyzed in English, French, German, Italian, Dutch, and Norwegian. |
| Conversation intelligence (Sales insights application) | Chinese Simplified (PRC), English, French, German, Italian, Japanese, Portuguese (Brazil), and Spanish. |

To learn more, see [Infrastructure availability PDF](https://aka.ms/dynamics_365_international_availability_deck)

**In which region is Sales Insights available?**<br>
Sales insights is available in the following regions:<br>
-    Asia Pacific (APJ)
-    Canada (CAN)
-    Europe, the Middle East, and Africa (EMEA)
-    Great Britain (GBR)
-    India (IND)
-    Japan (JPN)
-    North American (NAM)
-    Oceania (OCE)

## Assistant

**How do I disable teasers?**

To disable, follow these steps:

1. Sign in to the Dynamics 365 Sales Hub app, and go to **Change area** > **Sales Insights settings**.

2. On the site map, select **Overview**.

3. Go to **Teasers** section and toggle the option to disable the teasers.

    > [!div class="mx-imgBorder"]
    > ![Disable teasers](media/disable-teasers.png "Disable teasers")

**I am getting insufficient permissions alert**

If you see an alert about having insufficient permissions to use an Insight card, take these steps:

1. Go to **Settings** > **Security** > **Security Roles**.

2. Choose the user role viewing the insight cards.

3. Select the **Core Records** tab.

4. Set the privileges to Read and Write access for **Action card** and **Action card User Settings**.

   ![Insight card security role privilege](media/action-card-permissions600.png "Insight card security role privilege")

**How do I extend the trial period of Sales Insights?**

If you want more time to evaluate your Sales Insights trial version before buying it, you can extend the trial period by following the steps specified in [Extend your trial](https://docs.microsoft.commicrosoft-365/commerce/extend-your-trial?view=o365-worldwide).

## Sales accelerator 

**How do I add the Up next widget to an entity form?**

>[!NOTE]
>You can add the **Up next** widget only to managed forms.

To add the **Up next** widget to an entity form, follow these steps:

1.	Go to **Settings** > **Solutions** and the create an empty solution. For example, **AddWidget**.

2.	Add a **Form** to the solution. 

3.	Save the changes and publish the customizations.

4.	Export the created **AddWidget** solution as **UnManaged**.

5.	Delete the Solution **AddWidget** from the organization.

6.	Extract the zip file of the downloaded solution.

7.	Change the ```<Managed>``` value to 1 in the file ```Solution.xml``` and then save. 

    ```<Managed>1</Managed>```

8.	Open the ```customizations.xml``` file and remove the parameter ```<systemform unmodified="1">```.

9.	Choose the ```<column>``` under **Summary** tab, where you want to add the widget.

10.	Add the ```<section>``` tag as following: 

    ```
    <section name="CadenceWidget" showlabel="false" showbar="false" id="{<NEW_GUID_G1>}" IsUserDefined="0" layout="varwidth" columns="1" labelwidth="115" celllabelalignment="Left" celllabelposition="Left" labelid="{<NEW_GUID_G2> }">
      <labels>
          <label description="Cadence Widget" languagecode="1033" />
      </labels>
      <rows>
          <row>
              <cell id="{<NEW_GUID_G3>}" showlabel="false" colspan="1" rowspan="6" labelid="{<NEW_GUID_G4> }">
                  <labels>
                      <label description="Cadence widget" languagecode="1033" />
                  </labels>
                  <control id="CadenceWidgetControl" classid="{F9A8A302-114E-466A-B582-6771B2AE0D92}"  uniqueid="{<NEW_GUID_G5>}" isunbound="true">
                      <parameters />
                  </control>
              </cell>
          </row>
          <row />
          <row />
          <row />
          <row />
          <row />
      </rows>
    </section>
    ```
11.	Replace all the ```<NEW_GUID_G*>``` occurrences by generating a new GUID for each place.

12.	For ```<controlDescriptions>``` node, add a child node as following:

    ```
    <controlDescription forControl="{<GUID_G5>}">
    <customControl formFactor="2" name="MscrmControls.AcceleratedSales.CadenceWidgetControl">
        <parameters />
    </customControl>
    <customControl formFactor="0" name="MscrmControls.AcceleratedSales.CadenceWidgetControl">
        <parameters />
    </customControl>
    <customControl formFactor="1" name="MscrmControls.AcceleratedSales.CadenceWidgetControl">
        <parameters />
    </customControl>
    </controlDescription>
    ```
13.	Replace the ```<GUID_G5>``` in ```customizations.xml``` with the **GUID_G5** generated from **step 11**.

14.	Save the changes and zip the folder.

15.	Open Dynamics 365 and go to **Settings** > **Solutions**.

16.	Import the zipped solution. 

17.	Publish all customizations.

18.	Verify that the **Up next** Widget successfully shows up on the form.

## Relationship analytics

**What do I need in order to use Relationship analytics?​**<br>
Relationship analytics uses data from Dynamics 365 for Sales. Optionally, it includes data from Exchange Online and LinkedIn InMail with the LinkedIn solution with sync-back enabled. For Exchange data, the graph is built only on user accounts situated in the United States.​

**How do I enable Relationship analytics?​**<br>
Install [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] and enable the Relationship analytics feature from  **Settings** > **AI setup**.​

**What is the frequency of KPI updates?​**<br>
KPIs are updated every 24 hours, potentially fewer.​

**What are the signals in relationship health?​**<br>
Relationship health looks at activity, recency, engagement, and sentiment of activities between sellers and customers.​

**Can I configure relationship health?​**<br>
An administrator can influence the relationship health score by changing the weight of activity types and the expected level of communications with customers.

## Predictive lead/opportunity scoring

**What do I need in order to use lead/opportunity scoring?​**<br>
Install [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] and use standard lead entity or standard opportunity entity.​

To build a lead score model, a minimum of 40 qualified and 40 disqualified leads are required. 

To build an opportunity scoring model, a minimum of 40 won and 40 lost opportunities are required. 

Verify that the leads and opportunities are created on or after January 01, in the previous year.

**Can I customize the model?​**<br>
You cannot customize the model. The out-of-the-box model automatically selects the features for the model.

**Can I create multiple models for leads/opportunities?​**<br>
No. In this release, you cannot create multiple models. You can create only one model for all leads and one model for all opportunities.

**What is the minimum data required to create a lead/opportunity score model?​**<br>
A minimum of 40 qualified and 40 disqualified leads are required to build a lead score model. 

A minimum of 40 won and 40 lost opportunities are required to build an opportunity scoring model.​

**What is the difference between score and grade?​**<br>
The score is generated by the machine learning model. <br>
The grade is just grouping scores in four buckets that the admin can configure.

## Notes analysis

**What do I need in order to use Notes analysis?​**<br>
Notes analysis requires Office 365.​

**How do I enable Notes analysis?​**<br>
Install [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] and enable the Notes analysis feature from **Settings** > **AI setup**.​

**What does Notes analysis look at for the intent?​**<br>
Notes analysis looks at notes and posts on the timeline for the intent that may indicate a record should be created. Notes analysis looks for meeting requests, meetings, tasks, and contacts.

## Talking points

**What do I need in order to use Talking points?​**<br>
Talking points require Office 365 Exchange and a configured server-side sync (SSS) profile (mailbox need not be enabled for SSS).​

**How do I enable Talking points?​**<br>
Install [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] and enable the Talking points feature from **Settings** > **AI setup**.​

**What do Talking points look at for the conversation starters?​**<br>
Talking points look at the inbox of the signed-in user for emails from the contact list that includes conversational topics relating to sports, entertainment, and health.​

**How is my privacy protected?​**<br>
User privacy is safeguarded because only emails from the signed-in user's mailbox are shown. Your colleagues won't be able to see those same talking points unless they were also a recipient of that email.​

**How long will it take for results to appear?​**<br>
It takes a few seconds to display the results.​

## Who knows whom

**What do I need in order to use Who knows whom?​**<br>
Who knows whom requires Office 365 Exchange. The graph is built only on user accounts situated in the United States. Geo availability will expand as Sales Insights becomes available in more regions. Server-side sync is required for email introduction requests. ​

**How do I enable Who knows whom?​**<br>
Install [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)], opt in to Connection insights from the Office 365 admin, and enable the Who knows whom feature from **Settings** > **AI setup**.​

**How long will it take for results to appear?**<br>
The graph requires approximately 24 hours to populate the results for the first time. Subsequent updates take 3-6 days based on new activities included in the graph.​

**​Who will be included in the graph?​**<br>
Everyone in the tenant (in the United States until geo availability expands) will be included in the graph. Administrators have the option to opt out users or DLs, such as C-suite, M&A, finance, and so on. Per user, the self-serve opt-out will be available in the next few months.​

**​How are the connections weighted?**<br>
Connections are weighted by a combination of how well the signed-in user knows the intermediary, and how well the intermediary knows the target contact/lead. Consequently, this means a salesperson might not see the same results as another salesperson because they know different people in the organization.

## Conversation Intelligence

**How long does it take for data updates to reflect in the app?**<br>
The data is refreshed periodically and could take up to 12 hours to reflect. We continue to make improvements to reduce this delay.

**Can sellers (or non-managers) use this app?**<br>
Yes, the application is also available for sellers and can view their conversational insights.

**Is an admin needed to enable the app for my organization?**<br>
Yes. Administrator must configure the application for you to use. If administrator did not configure the application, you can explore the application with the demo data that is provided.

**Which telephony system do you support?​**<br>
The application is independent of telephony systems. If you have stereo call recordings (two-channel stereo), we process them at scale to generate insights​.

**What does the onboarding experience include?​** <br>
As part of the onboarding experience, you must provide the access key to the Azure blob location where you upload your call recording files for processing. You must adhere to standard metadata format (in JSON) of conversation intelligence and upload that along with every call recording file. Apart from this, you must share trackers that you care about along with the competitive brands and products for conversation intelligence to track these words across calls.

**How is the sentiment model built?**<br>
Conversation intelligence transcribes the calls into text and generates sentiment from the text in the conversation.

**I have mono-channel recording files. Can I still use conversation intelligence?​**<br>
No, we DO NOT process mono-channel call recording files. We only support stereo-type call recording files.

**How long does it take to see the results?​**<br>
Conversation intelligence takes a few minutes to process and display the data on the dashboard, depending on the size of the call recording files and format. You must have at least 10 call recording files to process and display the data.

**Do you retain the call recordings?​**<br>
No. The call recordings are deleted as soon as the audio file is processed​.

### See also

[Overview](overview.md)

[Introduction to administer Sales Insights](../sales/intro-admin-guide-sales-insights.md)
