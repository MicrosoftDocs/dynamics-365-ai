---
title: "Set up record creation for social activity entities from Market Insights | Microsoft Docs"
description: "Learn how to configure rules in Dynamics 365 to automatically turn social activities into records."
keywords: "rule framework, update rules, create record, entity mapping"
ms.date: 02/14/2019
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 08535190-f438-4f56-bd05-f1a7b909822e
author: m-hartmann
ms.author: mhart
ms.custom: dyn365-ai-marketinsights
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# Configure Automatic Record Creation and Update Rules in [!include[](../includes/pn-dynamics-crm.md)] to process Social Activity entities from [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)]

(This topic is pre-release documentation and is subject to change.)

To automatically create an entity record (such as a Case or a Lead) from a Social Activity record in [!include[](../includes/pn-dynamics-crm.md)], an administrator or customizer must configure Automatic Record Creation and Update Rules in [!include[](../includes/pn-dynamics-crm.md)].

In [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)], when users [link a post to Dynamics 365](link-posts-to-dynamics-365.md), a Social Activity record is created in the connected [!include[](../includes/pn-dynamics-crm.md)] instance. The entity type the user creates in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] (Case, Lead, and so on) is passed on as part of the [JSON Payload](create-dynamics-365-record-from-social-post.md#understand-the-data-sent-to-dynamics-365-when-you-create-a-social-activity) to the social activity in [!include[](../includes/pn-dynamics-crm.md)].


> [!IMPORTANT]
>  Without Automatic Record Creation and Update Rules, the Social Activity record created in [!include[](../includes/pn-dynamics-crm.md)] by [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] does not automatically result in a corresponding [!include[](../includes/pn-dynamics-crm.md)] entity record (such as a Case or Lead record).

![open drop-down menu with case and lead options for creating a record in dynamics 365 from within market insights](media/select-entity.png "Open drop-down menu with Case and Lead options for creating a record in Dynamics 365 from within Market Insights")

## Create a rule to automatically turn social activities into Lead or Case records

> [!NOTE]
> Parts of the user interface for integration scenarios might reference Microsoft Social Engagement. Nevertheless, you can configure the connections with your Market Insights solution. 

1. Sign in to [!include[](../includes/pn-dynamics-crm.md)] with your system administrator or customizer credentials.

2. Go to **Settings** > **Business Management** > **Automatic Record Creation and Update Rules**.

   ![access automatic record creation and update rules settings](media/business-management-settings-D365.png "Access Automatic Record Creation and Update Rules settings")

3. Select **New** to create a new rule.

   ![location of the new command to create new rules](media/new-record-creation-update-rule.png "Location of the New command to create new rules")

4. Provide a **Name** for the rule.

5. Set the **Source Type** to **Social Activity**.

6. Click **Save** to create the record.

   ![location of areas for name, source type, and the save command](media/create-record-creation-update-rule.png "Location of areas for Name, Source Type, and the Save command")

7. Under **Channel Properties**, select **Additional Properties**.

8. Select the **Search** button, and then select **New**.

9. In the new dialog box, provide a **Name** for the Channel Property Group. For **Source Type**, select **Social Activity**.

10. Select **Save**.

11. Select **Add Channel Property record** in the newly created Channel Property Group. Enter **userPreferredTargetEntity** for the name, and set the **Data Type** to **Single Line of Text**. It's important that you match the name as documented in the [JSON payload](create-dynamics-365-record-from-social-post.md#understand-the-data-sent-to-dynamics-365-when-you-create-a-social-activity). Now that the Channel Property is in place, you create the actual update rules.

12. Select **Save**, and then close the dialog boxes.

    ![details of the channel property record for the market insights payload](media/channel-property-group-userPreferredTargetEntity.png "Details of the Channel Property record for the Market Insights payload")


13. In **Record Creation and Update Rule**, select **Add Record Creation and Update Rule Item record**.

    ![location of the new rule command](media/specify-record-creation-and-update-details.png "Location of the New Rule command")

14. In the new dialog box that opens, provide a **Name** for the rule and then select **Save** to create the rule.

15. Under **Condition**, choose **Select**, and scroll to the bottom of the drop-down list to find **Channel Properties** under **Local Values**. Then, select **userPreferredTargetEntity** **Equals** **lead**.  
    
    > [!NOTE]
    > The value for userPreferredEntity must exactly match the value in the JSON payload. This value is the [!include[](../includes/pn-dynamics-crm.md)] entity type name that can be different from the name in the [!include[](../includes/pn-dynamics-crm.md)] user interface. For example, the entity type name for Case is *incident*.

    ![condition for a lead field in the market insights payload for userprefrerredtargetentity](media/lead-creation-condition.png "Condition for a Lead field in the Market Insights payload for userPrefrerredTargetEntity")

16. Under **Action**, select **Add Step**, and then select **Create Record**. Set the value to **Lead**. 

    ![actions area with record creation set to lead](media/configure-action-update-rule.png "Actions area with record creation set to Lead")

17. Click **Save & Close** to finalize the rule.

18. Verify that the rules were created, and then select **Activate** to activate the rule.    
    Social Activity entities created from [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] will now automatically create the configured record type in [!include[](../includes/pn-dynamics-crm.md)]. 

    ![activate the newly created rule to automatically turn social activity entities into other record types](media/activate-update-rule.png "Activate the newly created rule to automatically turn Social Activity entities into other record types")

> [!TIP]
> To create a Case record, repeat the steps above but select **userPreferredTargetEntity** **Equals** **incident**, and under **Action**, set the **Create Record** value to **Case**.

### See also

[Set up the connection to link posts from Market Insights to Dynamics 365](link-posts-to-dynamics-365.md)    
[Link posts from Market Insights to Dynamics 365](create-dynamics-365-record-from-social-post.md)    
[Set up rules to automatically create or update records in Dynamics 365](https://docs.microsoft.com/dynamics365/customer-engagement/customer-service/set-up-rules-to-automatically-create-or-update-records)
