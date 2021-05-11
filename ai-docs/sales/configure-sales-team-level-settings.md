---
title: "Configure the sales team level settings in conversation intelligence (Dynamics 365 Sales) | MicrosoftDocs"
description: "Learn how to configure the sales team level settings in conversation intelligence in Dynamics 365 Sales."
ms.date: 04/14/2021
ms.service: dynamics-365-sales
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# Configure sales team-level settings

As a sales manager, you can configure conversation intelligence to match your teams’ specific requirements. The following settings are available:    
- Conversation trackers (keywords and competitors)
- Available languages
- Selection of top performers 

Follow these steps:
1.	Sign into the Dynamics 365 Sales Hub app with sales manager security role.    
2.	Select the **change area** ![change area](media/change-area-icon.png) in the lower-left corner of the page, and then select **Personal settings**.  
    > [!div class="mx-imgBorder"]
    > ![Select personal settings](media/si-admin-change-area-personal-settings.png "Select personal settings")   
3.	On the site map, under **Productivity** > **Conversation intelligence**.   
    The conversation intelligence home page opens.   
    > [!div class="mx-imgBorder"]
    > ![Conversation intelligence getting started for sales manager](media/ci-sm-getting-started-page.png "Conversation intelligence getting started for sales manager")   
4.	On the home page, select **Get started**.   
    The conversation intelligence configuration page opens.     
    > [!div class="mx-imgBorder"]
    > ![Conversation intelligence home page for sales manager](media/ci-sm-home-page.png "Conversation intelligence home page for sales manager")   
5.	Under the **Conversation tracking** section, add the keywords and competitors that you want to track on your sales team’s calls. Also, you can reduce the language list provided by the organizational admin to the languages that the sellers on your team use during their calls with customers.      
    This is a local setting that will be applied only to your sales team. You can update these keywords, competitors, languages later when required. More information: [Configure conversation content](../sales/configure-keywords-competitors.md).

    > [!div class="mx-imgBorder"]
    > ![Configure conversation tracking](media/ci-admin-conversation-trackers.png "Configure conversation tracking")    

6.	In the **Sales team management** section, configure the top performers as follows:    
    You can view the names of the team members whose calls are analyzed in conversation intelligence and select the sellers who are top performers.     
    It’s possible to choose the top performers manually, or let the application automatically select them. Select one of the following options:   
    - **Manually select top performers**: Choose top performers from the list of sellers. In the **Top performer** column, select the star icon next to your top seller. The seller is added to the top performers list, where the seller's data is compared to other sellers.     
        > [!div class="mx-imgBorder"]
        > ![Manually select top performers](media/ci-sm-manually-select-top-performers.png "Manually select top performers")    
    - **Enable automatic identification of top performers**: The application automatically selects the top performers based on the number of opportunities they won or the leads they qualified. When you select this option, you choose whether to rank performers **by won opportunities** or **by lead qualification**.   
        > [!div class="mx-imgBorder"]
        > ![Enable automatic identification of top performers](media/ci-sm-automatic-identification-top-performers.png "Enable automatic identification of top performers")    

Conversation intelligence is now configured and ready for use in your sales organization for your sales team.

### See also

[Introduction to administer conversation intelligence](intro-admin-guide-sales-insights.md#administer-conversation-intelligence)  
[First-run set up experience](fre-setup-sales-insight-app.md#microsoft-teams-conversation-intelligence)


[!INCLUDE[footer-include](../includes/footer-banner.md)]    
    
 
