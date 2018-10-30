---
title: " View overall insights of your sales in Dynamics 365 AI for sales | MicrosoftDocs"
description: "View high-level information on forecast, leaderboard, pipeline, highlights, upcoming meetings, and relevant news with AI-driven insights readily available for Dynamics 365 for Sales"
keywords: ""
ms.date: 10/31/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 9affa7f1-5fed-4ca1-9bb5-5090aaab359e
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Preview: View overall sales insights

Applies to Dynamics 365 (online), version 9.1.0 <br>

When you log in to [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] application, homepage is displayed. Homepage provides high-level information on the forecast, leaderboard, pipeline, highlights, upcoming meetings, and relevant news to understand:
- Total days left in the period to achieve your target quota
- How much you have sold
- Number of deals you have won
- What is your win rate

> [!NOTE]
> When you log in for the first time, the application takes several minutes to gather the data and display visuals for you. Also, a status message is displayed to update you on progress.

Using this information, you can quickly take action when necessary and drill deep into a particular report for more information. The following is an example of how a home page is displayed.

> [!div class="mx-imgBorder"]
> ![Dynamics 365 AI for Sales homepage](media/d365-ai-sales-homepage1.png "Dynamics 365 AI for Sales homepage")

## Q&A 

Sometimes you want to get quick answers from your data without searching through the reports in the sections. Dynamics 365 AI for sales app provides Q&A feature to ask questions using natural language. Use **Q&A** to explore your data using intuitive, natural language capabilities and receive answers in the form of charts and graphs. For example, when you type "what were total sales last year.", the application displays charts and graphs that contains details of your last sales. Q&A is different from a search engine - **Q&A** only provides results about the data in your reports.
The Q&A displays as following on homepage:

> [!div class="mx-imgBorder"]
> ![Q&A question text box](media/d365-ai-qa.png "Q&A question text box")

Type a question that you want to ask in the text box and press Enter. For example, enter “what is the revenue by sales person?”. The Q&A screen opens with a visualization of the results.

> [!NOTE]
> You can also open the Q&A screen by selecting the chat icon.

> [!div class="mx-imgBorder"]
> ![Q&A screen](media/d365-ai-qa-page.png "Q&A screen")

You can see that some attributes in your question are highlighted. When you select the highlighted attribute, other attributes related to it are displayed. You can select the relevant attribute to change your question. For example, revenue is highlighted in the questions and when you select revenue, other attributes related to revenue are displayed.

> [!div class="mx-imgBorder"]
> ![Q&A attribute suggestions](media/d365-ai-qa-page-attributes.png "Q&A attribute suggestions")

The Q&A provides you with predefined questions. You can customize these predefined questions to fit your requirements. Select the question and key attributes are highlighted. Select these key attributes and change them according to your requirements. The results are updated to display your modified question.

## Basic KPIs

The basic KPIs provide information on the status of your current sales period. The following is an example of how the basic KPIs are displayed.

> [!div class="mx-imgBorder"]
> ![Base KPIs](media/d365-ai-sales-basekpis.png "Base KPIs")

By viewing these KPIs, you’ll know:
- The time left in the current period to achieve your sales target.
- The sum of actual revenue of all won opportunities.
- The total estimated revenues of all open opportunities.
- The total deals that are won by you in this period.
- The percentage of deals that you have won against available opportunities in this period.
- The average revenue generated through each deal in this period.

## Forecast

Using the **Forecast** section, you can predict how your team is performing to achieve quota for the period. The following is an example of how a forecast is displayed. 

> [!div class="mx-imgBorder"]
> ![Forecast section](media/d365-ai-sales-forecastsection.png "Forecast section")

The Forecast section is classified into the following subsections.

1. **Insights message:** Displays a message on how your team is performing. For example, your target is $60,000 and so far, your achievement is only $18,000 with 30 days left to close the target. The application predicts that your team has achieved only 30%-win rate and displays the message - “Based on a win rate of 30%, you are not on track to meet the quota for this Quarter.”
1. **Overall quota:** Displays the progress on how your team is performing in achieving the sales targets for the current period. You can see a comparison between actual revenue generated and the remaining target revenue to be achieved for the period.
1. **Quick view:** Select **See report** to open Forecast in a quick view pane on home page. This quick view pane provides a glance on the forecast. From this quick view pane, you can further go into detailed view of the forecast. The following is an example of how a forecast pane is displayed:
    
    > [!div class="mx-imgBorder"]
    > ![Forecast quick view pane](media/d365-ai-sales-forecastpane.png "Forecast quick view pane") 

    Select View full report icon ![Forecast quick view](media/d365-ai-sales-forecastviewfullreporticon.png "Forecast quick view") on the forecast pane to go to Forecast tab.  [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Analyze team performance](../sales/d365-ai-team-performance.md)
  
## Leaderboard

The **Leaderboard** section provides information on how each sales rep is performing in the current sales period. The following is an example of how a Leaderboard is displayed:

> [!div class="mx-imgBorder"]
> ![Leaderboard section](media/d365-ai-sales-leaderboard.png "Leaderboard section")

The Leaderboard section is classified into the following subsections.

1. **Insights message:** Displays a message on which sales rep is falling behind in achieving the quota for the period. 
For example, Delia Schroeder, Samuel Barba, Bert Hair, Jimmie Lundgren are sales reps reporting to you and set individual revenue targets. Through the graph, you can see that Delia Schroeder and Bert Hair did not generate any revenue against their set targets. The application predicts that Delia Schroeder and Bert Hair has not achieved target quota and they are more than $12000 away in doing so. The insights message displays - “Delia Schroeder and Bert Hair are more than $12000 away from achieving their quotas.”
1. **Sales reps performance:** Displays the progress of each sales rep in achieving their quota. The bar chart shows the actual revenue (Green) generated against the assigned quota (Grey). 
To further drill down into the individual performance, select the bar representing the sales rep. In the following example, we have selected Delia Schroeder and a pane appear on the screen with her performance information along with the upcoming schedule:

   > [!div class="mx-imgBorder"]
   > ![Sales rep view](media/d365-ai-sales-leaderboard-delia-schroeder.png "Sales rep view") 

   The information includes actual revenue generated against the quota, target quota, gap between the actual revenue and quota, and opportunities available in the pipeline. In the **Upcoming** section, you can see scheduled meetings of her and select the meeting request to view the details. You can also send a note through email or start a chat to discuss further on the progress in achieving the target.

1. **Quick view:** Select **See report** to open Leaderboard in a quick view pane on home page. This quick view pane provides a glance at the performance of each sales rep. From this quick view pane, you can further go into a detailed view of the Leaderboard. The following is an example of how a Leaderboard pane is displayed:
    
   > [!div class="mx-imgBorder"]
   > ![Leaderboard quick view](media/d365-ai-sales-leaderboard-pane.png "Leaderboard quick view") 

    Select View full report icon ![Forecast quick view](media/d365-ai-sales-forecastviewfullreporticon.png "Forecast quick view") on the Leaderboard pane to go to **Leaderboard** tab. More information: View sales rep performance <link to the section>

## Pipeline

The Pipeline section provides a view of the relationship health in your upcoming pipeline. The following is an example of how a Pipeline is displayed:
    
> [!div class="mx-imgBorder"]
> ![Pipeline section](media/d365-ai-sales-pipeline.png "Pipeline section")

1.	**Insights message:** Displays a message on how your opportunities are trending for the period. For example, you have an opportunity with ACME customer, whose health is decreasing and the closing in 12 days. The application predicts opportunity at risk and displays the message - “ACME opportunity has low health score and is closing in 12 days.”
1. **Pipeline view:** Displays the opportunities that are closing soon and are at risk. The opportunities are displayed as bubbles on the graph, where x-axis represent the dates and y-axis represents the health score. To further understand the opportunities, mouse-over the bubble to see the estimated revenue, closing date, and health parameters. The size of the bubble determines the estimated cost and color determines the health condition.
1. **Quick view:** Select **See report** to open Pipeline in a quick view pane on the home page. This quick view pane provides a glance on deals along with health score. From this quick view pane, you can further go into a detailed view of the pipeline. The following is an example of how a Pipeline pane is displayed:

   > [!div class="mx-imgBorder"]
   > ![Pipeline quick view](media/d365-ai-sales-pipeline-pane.png "Pipeline quick view") 
 
    Select View full report icon ![Forecast quick view](media/d365-ai-sales-forecastviewfullreporticon.png "Forecast quick view") on the Pipeline pane to go to Pipeline tab. More information: View potential opportunities <link to the section>

## Highlights

Your team constantly works on interacting with customers, closing deals, opening opportunities, or failing to close deals. The Highlights helps you to keep track of these items in real time so that you can get involved when necessary. This information is displayed as cards. The following is an example of how a Highlights section is displayed:

> [!div class="mx-imgBorder"]
> ![Pipeline section](media/d365-ai-sales-highlights.png "Pipeline section")

1. **Title:** Provides a high-level description of what the item is about. For example, recently you have won an opportunity and the heading is displayed as “Opportunity Won Recently”.
1. **Description:** Provides a detailed description of the item. The description includes the sales rep name, close date, opportunity value, and the name of the opportunity. For example, a large opportunity worth $50,000 is added to your system and the description is displayed as “This $50,000 opportunity Bert Hair from Wednesday, 17 October 2018, was just added to your system” 
1. **See all insights:** Select See all on the Highlights section to view the list of items that got highlighted recently.
Select View opportunity to open the quick edit pane on an opportunity that you want to quickly edit. This helps you not move away from the home page to access the opportunity. On these cards, you can perform actions such as:
    - Leave a congratulatory note on a won deal 
    - Edit details of an opportunity in the context    
    - Send a quick email to inquire about an opportunity at risk
    - Quickly set up a meeting with a sales rep

    The following is an example of how quick edit form displays:

   > [!div class="mx-imgBorder"]
   > ![Pipeline quick view](media/d365-ai-sales-highlights-quickedit.png "Pipeline quick view") 

## Upcoming

The **Upcoming** section provides information on your upcoming 1-on-1 meetings with sales reps. Use these 1-on-1 meetings to coach the sales reps on topics such big deals that were just won or winnable deals that were lost. The following is an example of how an Upcoming section is displayed:

> [!div class="mx-imgBorder"]
> ![Upcoming section](media/d365-ai-sales-upcoming.png "Upcoming section")

Each appointment displays the name with whom you have the appointment, subject, and description. You can view the details of the sales rep such as performance and opportunities that are at risk. Select **View scorecard** to view the details. With these details, you can assess the situation and get information forehand before you go the meeting with the sales rep. Also, you can send an email, or chat with the sales rep before you go to the meeting.
Select **More options** to snooze or dismiss the appointment.

## Relevant news

The Relevant news section keeps you informed on the latest news about your products, customers, and industry. The following is an example of how a Relevant news is displayed:

> [!div class="mx-imgBorder"]
> ![Relevant news](media/d365-ai-sales-relevantnews.png "Relevant news")

