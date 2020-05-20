---
title: "Subscription churn prediction | Microsoft Docs"
description: "Predict whether a customer is at risk for no longer using your company’s subscription products or services."
ms.date: 05/20/2020
ms.reviewer: zacook
ms.service: dynamics-365-ai
ms.topic: "article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Subscription Churn
The Subscription Churn prediction feature enables you to predict whether a customer is at risk for no longer using your company’s subscription products or services.  You can create new Subscription Churn predictions in the Intelligence -> Predictions page, and see other predictions you may have created by clicking "My predictions".

## Prerequisites

[!NOTE] To create a prediction, a user must have Contributor or Administrator level permissions in your instance.

1. Data about your subscriptions and their history including:
- Subscription Identifiers – how do we distinguish subscriptions?
- Customer Identifiers – how can we match subscriptions to your customers?
- Subscription Event Dates – Start dates, end dates, what dates the subscription events occurred on.
- Subscription Information – Is this a recurring subscription?  How often does it recur?
    1. Required semantic data schema:
    - Subscription ID: This is the identifier of a subscription - it should be a unique value per subscription
	- Subscription End Date: This is the date the subscription expires for the customer
	- Subscription Start Date: This is the date the subscription starts for the customer
	- Transaction Date: This is the date a subscription change happened.  For instance, a customer renewing a subscription, starting a subscription, or ending a subscription would all be considered transactions on the subscription record.
	- Is it a recurring subscription: This is a true/false field that determines if the subscription will renew with the same subscription ID for the customer without customer intervention
	- Recurrence Frequency (in months): For recurring subscriptions, this is the period the subscription will renew for.  It is represented in months.  For instance, a yearly subscription that auto-renews for a customer in year-long increments should have 12 as a value for the record.
	- (Optional)Subscription Amount: This is the amount of currency the subscription renewal would cost the customer.  This can help identify patterns for different levels of subscriptions.
2. Data about customer activities including:
- Activity Identifiers: how do we distinguish one activity from another for the same type of activity?
- Customer Identifiers: how can we match activities to your customers?
- Activity Information: What is the name of the activity?  When did it happen?
	1. Required semantic data schema:
	- Primary key: This is the identifier for a unique activity event.  For instance, a website visit for a customer, or a usage record showing the customer viewed a television show episode would have a unique identifier for each event of a website visit, or viewing of a television episode.
	- Timestamp: This is the date/time of the event identified by the Primary key.
	- Event: This field should represent the name of the event you want to use.  For instance, a field called "UserAction" in a streaming video service could have the value of "Viewed".
	- Details: This field should represent detailed information about the event.  For instance, a field called "ShowTitle" in a streaming video service could have the value of a video a customer watched.
3. Business Knowledge
- What does churn mean for your business? We support time-based churn definitions, meaning a customer is considered to have churned a period of time after their subscription is ended.

## Create a Subscription Churn prediction

[!TIP] At any point of configuring the Subscription Churn prediction, you can choose to "Save and close" to save your progress for later alterations.  You can always return to your saved prediction by navigating to the My predictions tab in the Intelligence -> Predictions page

1. In Customer Insights, go to Intelligence -> Predictions
2. Find the tile titled "Subscription churn model (preview)" and select "Use this model"
3. Enter a name for the model so you can distinguish it from other models you may create
4. Enter an output entity name - this is the name that will be given to the model entity and appear on the Entities page after your run your model. Include letters and numbers only, without any spaces
5. Click next
6. Enter the amount of days from a subscription end date that your business would consider a customer to be in a churned state.  This time period is typically associated with business activities, like offers or other marketing efforts, to attempt to recover a customer and prevent the customer loss.
7. Click next
8. Click Add data for Subscription history
9. Select the entity that provides the subscription history information as described in the prerequisite section of this document
10. If the fields below are not populated, you'll need to configure the relationship from your subscription history entity to the Customer entity.
    1. Select the Field that identifies the customer from your subscription history table that can be directly related back to the primary customer id of your Customer entity.
    2. Select the Customer entity that matches your primary Customer entity
    3. Enter a name that describes the relationship.  For instance, a good pattern can be Entityname1Entityname2ID, replacing the Entityname1 with the name of your first entity, and Entityname2 with the name of your second entity
    3. Click Next
11. Map the semantic fields to attributes within your subscription history entity.  For descriptions of the fields, refer to the prerequisites section of this document.
12. Click Save
13. Click Add data for Customer activities
14. Select the entity that provides the customer activity information as described in the prerequisite section of this document
15. Select an activity type that matches to the type of customer activity you are configuring.  If you don't see an option that matches to the activity type you need, select "Create new" and type in the name of the activity type.
16. If the fields below are not populated, you'll need to configure the relationship from your customer activity entity to the Customer entity.
    1. Select the Field that identifies the customer from your customer activity table that can be directly related back to the primary customer id of your Customer entity.
    2. Select the Customer entity that matches your primary Customer entity
    3. Enter a name that describes the relationship.  For instance, a good pattern can be Entityname1Entityname2ID, replacing the Entityname1 with the name of your first entity, and Entityname2 with the name of your second entity
    4. Click Next
17. Map the semantic fields to attributes within your customer activity entity.  For descriptions of the fields, refer to the prerequisites section of this document.
18. Click Save
19. (Optional) If you have any other customer activities you would like to include, repeat steps 13 - 18.
20. Click Next
21. Set a frequency to retrain your model. This is important to update the accuracy of predictions as new data is imported into Customer Insights. Most businesses can retrain once per month and retain good accuracy for their prediction.
22. Click Next
23. Review the selections you have made.  You can navigate back to any part of the prediction configuration from this page by clicking the edit link under the value presented, or clicking the associated configuration step from the left side menu.
24. If all values are configured correctly, click "Save and run".  The configuration process will begin the prediction process and will navigate you back to the My predictions tab in the Intelligence -> Predictions page.  You can see the status of your prediction, as well as other predictions.  The run process may take several hours to complete depending on the amount of data used in the prediction.

## Reviewing a prediction status and results

1. Navigate to the My predictions tab in the Intelligence -> Predictions page.
2. Find the prediction you would like to review and note the following fields:
    1. Prediction name: This is the name of the prediction chosen during the configuration of a prediction.
    2. Prediction type: Displays the type of model used for the prediction
    3. Output entity: this is the name that was provided while configuring the prediction to store the output of the prediction.  You can find an entity with this name in the Entities page.
    4. Predicted field: this is populated only for some types of predictions, and is not used for Subscription Churn.
    5. Status: contains the current status of the prediction's run state including
        - Queued: the prediction is currently waiting for prerequisite processes to run.
        - Refreshing: the prediction is currently executing the "score" stage of processing, producing output results that will flow into the Output entity.
        - Failed: the prediction has failed.  Click "Logs" for more details
        - 
    6. Edited: The last date the configuration for the prediction was altered and saved.
    7. Last refreshed: The last date the prediction executed and refreshed results in the Output entity.
3. Click the vertical ellipses next to the prediction you would like to review results for, then click View.
4. Review the results for the prediction.  There are three primary sections of data within the results page
    1. Training model performance: A, B, or C values can be represented in this section.  This indicates the performance of the prediction, and can help you make the decision to use the results stored in the Output entity.
        - Scores lower than "C" will result in a failed execution of the prediction. Look to [Fixing a failed prediction](#fixing-a-failed-prediction) for how to potentially resolve this and finish your prediction.
    2. Likelihood to churn (number of customers): This shows bucketed groups of customers based on their predicted risk of churn. This can help you later if you want to create a segment of high risk customers to understand where your cutoff should be for segment membership.
    3. 

## Fixing a failed prediction

1. Navigate to the My predictions tab in the Intelligence -> Predictions page.
2. Click the vertical ellipses next to the prediction you would like to view error logs for, then click Logs.
3. Open each error that is presented.  There are several types of errors that can occur, and they should describe what condition caused the error.  For instance, an error noting there was not enough data to accurately predict can typically be resolved by loading additional data into Customer Insights.

## Refreshing a prediction

[!NOTE] Predictions will automatically refresh on the same schedule your data refreshes as configured in the Admin -> System -> Schedule tab

1. Navigate to the My predictions tab in the Intelligence -> Predictions page.
2. Click the vertical ellipses next to the prediction you would like to manually refresh results for, then click Refresh.

## Deleting a prediction

[!NOTE] Deleting a prediction will not remove its corresponding Output entity.

1. Navigate to the My predictions tab in the Intelligence -> Predictions page.
2. Click the vertical ellipses next to the prediction you would like to delete, then click Delete.