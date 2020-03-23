---
title: "Understand how to prioritize sales pipeline through work list in Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to prioritize sales pipeline through work list in Dynamics 365 Sales Insights."
ms.date: 04/01/2020
ms.service: crm-online
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# Prioritize sales pipeline through work list 

During the day, sellers have multiple tasks they need to juggle and multiple leads and opportunities they are working on. As a result, it is hard for sellers to plan and prioritize customer facing activities. The worklist in Sales accelerator of Dynamics 365 Sales Insights helps sellers to manage their day and work according to the priorities by ensuring that important leads and opportunity are not left behind. 

The work list in sales accelerator provides the following capabilities: 

- Manage and view all records, such as leads and opportunities, with the due activity for the day, sorted by priority, and remove records from the work list after an activity is complete. To learn more, see [View my records through work list](#view-my-records-through-work-list).

- Manage work list by sorting, filtering, and grouping all records. To learn more, see [Filter records in work list](#filter-records-in-work-list).

- View relevant information regarding customers, such as personal details, past and future activities, and the related entities for each record. To learn more, see [Understand the up next widget](#understand-the-up-next-widget).

- Communicate with customers through phone and mail. To learn more, see [Connect with customers through a record or the up next widget](connect-with-customers.md).

- Add manual activities to records other than those that are defined in sequence if an ad-hoc activity is required to be performed. To learn more, see [Add manual tasks to records](#add-manual-tasks-to-records).

A sales manager configures the worklist by defining the sequence for the leads and opportunities through the sequence designer. To learn more, see [Create and manage sequences](create-manage-sequences.md).

## Prerequisites

Review the following prerequisites before you start using the engagement center:

- Sales accelerator feature is installed in your organization and your role is assigned to access work list . To learn more, [Enable and configure Sales accelerator](#enable-configure-sales-accelerator.md).

- A softphone and an email server are configured for your security role. 

- Channel Integration Framework version 1 is installed, and a channel provider must be configured for your Dynamics 365 organization. To learn more, see [Integrate a sample softphone dialer with Dynamics 365 Sales](integrate-sample-softphone.md). 

- (Optional) [Predictive lead scoring](configure-predictive-lead-scoring.md) and [Predictive opportunity scoring](configure-predictive-opportunity-scoring.md) are enabled and models are generated for your organization. Contact your administrator to enable these features.

## View my records through work list

The work list displays a list of records that are assigned to you or to the security role you are associated with. The records display activities that are due for the current date and pending from previous dates that are created manually or through the sequence. This helps you to access records with activities at one location instead of navigating across multiple forms in the application. A sales manager can configure and determine the entities (leads and opportunities) to display to you in the  work list. The top of the record in the work list  will always be the next best customer with the highest prediction score.

Follow these steps to view work list: 

1. [Review the prerequisites](#prerequisites).

2. Sign in to the Dynamics 365 Sales Hub app, and go to **Change area** > **Sales**.

3. From the site map, under **My Work**, select **Sales accelerator (preview)**. 

    The engagement center page opens, and the following screen is an example.

    <image>   

    | Number | Feature | Description |
    |--------|---------|-------------|
    | 1 | **Filter, sort, group records** | You can filter, sort, and group the records that you want to view in the list to quickly identify the customers to contact. To learn more, see [Filter records in work list ](#filter-records-in-work-list).<br>By using the lookup icon, you can search for a specific record using the record name. Also, you can filter the records according to the due date, select calendar icon and select **By Today** or **From Tomorrow**.<br>Refresh the list after you complete an activity on a record and the record will be removed from the list.|
    | 2 | **Records list** | Displays a list of records that are assigned to you or to a security role that you are part of. You must perform and complete defined activities on these records from current date and from the previous dates.<br>Each record displays details, such as the name of the record, primary contact name, next best action, priority scoring, and entity name. Select the record to view more information in the entity form.<br>You can perform the specified activity for the record by selecting the activity icon in the record. to learn more, see [Connect with customers through a record or the up next widget ](connect-with-customers.md).<br>When you complete an activity on the record, select the refresh icon, the list will be refreshed, and the record will be removed from the list.<br>**Note**: The list displays records for a month from current date. The records that are older than 30 days are automatically removed and will not be displayed.|
    | 3 | **Up next widget** | Display the next best action that you can perform on a record for the given date. To learn more, see [Understand the up next widget](#understand-the-up-next-widget).|
    
## Filter records in work list

Use the filters to prioritize the records in the engagement center to reach the customers at the right time. Engagement center provides the following filtering mechanisms to prioritize the records:

- [Filter by](#filter-by)

- [Group by](#group-by)

- [Sort by](#sort-by)

### Filter by

Allows you to filter the list by selecting the entity and activity types. When you select the filters, the list is refreshed to display the filtered records.
    
- The **Entity type** filter options are **Lead** and **Opportunity**. You can select both options to view all records. Also, you can select an individual entity to view only the records that belong to that entity.
        
    You must select at least one option to display relevant records in the engagement center. Also, if there are no records that match your selected entity type, an empty list will be displayed.

    By default, all filter options are selected.

- The **Activity type** filter options are **Call**, **Email**, and **Task**. You can select all or any specific option to filter the records to display in the work list .

    You must select at least one option to display relevant records in the engagement center. Also, if there are no records that match your selected activity type, an empty list will be displayed.

    By default, all filter options are selected.

For example, when you select the entity type as **Lead** and the activity type as **Call**, the work list displays only the records that are of type lead and has the activity as call.

### Group by

Allows you to group the records with the selected group type. Also, in the header, you can see the total number of records available in each group. The following group types are available:

- **Due time**: When you select this option, the records in the engagement center are grouped according to the due time that an activity must complete. 

    For example, there are ten records available in your engagement center. The number of records for which you need to complete the activities within the due time are as follows: three for today, four from yesterday, and three from this week. When you select the **Due time** option, the records are grouped as **Today**, **Yesterday**, and **Last 7 days**. 

    By default, **Due time** is selected to group the records.

- **Entity type**: When you select this option, the records are grouped according to entities. The records in the engagement center are grouped according to **Leads** and **Opportunities**.

- **Activity type**: When you select this option, the records are grouped according to the activity type. The following activity types are available: **Call**, **Email**, and **Task**.

- **Activity source**: When you select this option, the records are grouped according to the activity source. The following activity source is available: **Sequence** and **Manual**.

### Sort by

Allows you to sort the records according the selected sorting option. Also, in the header, you can see the total number of records available in each sort order. The following sorting options are available:

- **Due time**: When you select this option, the records in the engagement center are sorted according to the due time that an activity must complete. Further, you can select the sort order as: 

    - **Oldest on top** to view the records with oldest date to complete an activity on the top in ascending order. 

    - **Newest on top** to view new records with latest date to complete an activity on the top in ascending order. 

    For example, there are ten records available in your engagement center. The number of records for which you need to complete the activities within the due time are as follows: three for today, four from yesterday, and three from this week. When you select the **Due time** option to sort by and Newest on top for sort order, the records are sorted according to the activity completion date as **Today**, **Yesterday**, and **Last 7 days** and displayed in ascending order.

    By default, **Due time** is selected for sort by and **Newest on top** for sort order to sort the records.

- **Priority score**: When you select this option, the records in the engagement center are sorted according to the priority score assigned to each task. Further, you can select the sort order as:

    - **Lowest on top** to view the records in ascending order with lowest score on top

    - **Highest on top** to view the records in descending order with highest score on the top.

    For example, you have records with priority scores as, 95, 92, 89,45, 54, and 73. When you select the **Priority score** option to sort and **Highest on top** for order, records are sorted in descending order with the record that has highest score (95) on top.

- **Name**: When you select this option, the records in the engagement center are sorted according to the record name.

    Further, you can select the sort order as **A to Z** to view the records in ascending order and **Z to A** to view the records in descending order.

## Understand the up next widget

Using the Up next widget, you can view and perform actions on activities on a record. The widget displays the current activity, upcoming activity, and completed activities. You can add these activities to a record manually or through a sequence. 

- For sequence, a sales manager creates the activities and applies them to the record according to the business requirement. The activities in the sequence are displayed in the **Up next** widget.

- For manual tasks, you or a sales manager can create a task on the timeline. The task is displayed in the **Up next** widget as an activity depending on the due time. This activity is available to you and other sellers who have access to the record.

<image>

1. **Current activity**: The current activity is a task that you must complete or skip  to go to the next activity which moves the record closer to completion. To perform an action, such as phone call or send an email, select the action icon displayed in the activity. To learn more, [Connect with customers through a record or the up next widget ](connect-with-customers.md).

    After you complete the action, select **Mark complete**, and the activity is closed and moved automatically to completed items and displays on timeline.
    
    Also, you can choose to skip the activity if you think it is not relevant to the record or you don’t want to perform the action. Select **More options** and then select **Skip** item. The activity is skipped and moved to completed items.

2. **Upcoming activity**: The upcoming activity is view only, and you can’t perform an action. The upcoming activity is displayed to you to know what activity is coming up for you when you complete the current activity.

3. **Completed activities**: The completed activities are the activities that are marked as complete or skipped for a record and the record is automatically moved to completed items.
    
    To view the completed activities  list, select **View completed** items. The section expands to display the list of completed activities with details, such as the activity is completed or skipped with date and time. You can’t perform any actions on these tasks and are view only. The following screen is an example of an expanded section of completed items:

    > [!div class="mx-imgBorder"]
    > ![View completed activities](media/sa-view-completed-activities.png "View completed activities")

## Add manual tasks to records

Using the sequence, you can define activities, such as email, call, and custom activity. As per your business requirement, you have to add extra activities to a lead or an opportunity apart from the assigned sequence. Sales accelerator allows you to add manual activities for leads and opportunities to appear in the **Up next** widget along with the activities defined in sequence for a given day. The manual activities include tasks, such as appointments, conversations, booking alerts, and send SMS.

The characteristics of manual activities are similar to an activity defined in a sequence. Sellers must perform the task and mark it as complete. Then the activity will be moved to the list of completed activities in the **Up next** widget.

A sales manager or you, as a seller, can add the manual activity to the records that you or your security role owns. To add the manual activity, follow these steps:

1. Sign in to the Dynamics 365 Sales Hub app, and go to **Change area** > **Sales**.

2. From the site map, under **My Work**, select **Sales accelerator (preview)**. 

3. Select the record for which you want to add the manual task.

4. On the **Timeline** section, select the plus icon to add a manual activity.

    The list of activities is displayed.

5. Select and configure the activity that you want to add to the record.

6. Save and close the activity.

The activity is added to the record and displayed in the **Up next** widget as per the due date.

### See also

[What is sales accelerator](sales-accelerator-intro.md)

[Create and manage sequences](create-manage-sequences.md)