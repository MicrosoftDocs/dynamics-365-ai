---
title: "Intelligence | MicrosoftDocs"
description: Manage workflows used to generate machine learning insights
ms.custom: ""
ms.date: 06/28/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
# Intelligence 
The **Intelligence** page shows you workflows that have been created to generate machine learning insights.  Workflows are designed to help you choose the data you want to use, select what will generate the machine learning insight, and map the results back into your Customer Insights data.

> [!div class="mx-imgBorder"] 
> ![Configure Web Service inputs](media/intelligence-main.png "Configure Web Service inputs")

## Add a new workflow

1. On the **Intelligence** page, select **New Workflow**.

   > [!div class="mx-imgBorder"] 
   > ![Configure Web Service inputs](media/intelligence-newworkflow.png "Configure Web Service inputs")

2. Give your workflow a recognizable name in the **Display name** field, and then select the web service you've published using Azure Machine Learning services in the **Web service that contains your model** drop-down list.  Learn more about how to [Deploy an Azure Machine Learning Studio web service](https://docs.microsoft.com/azure/machine-learning/studio/publish-a-machine-learning-web-service).

   When you're done, select **Next**.

   > [!div class="mx-imgBorder"] 
   > ![Workflow Name and Web Service](media/intelligence-screen1.png "Workflow Name and Web Service")

3. For each **Web service input**, select the matching **Entity** from Customer Insights. When you're done, select **Next**.

   > [!div class="mx-imgBorder"] 
   > ![Configure Web Service inputs](media/intelligence-screen2.png "Configure Web Service inputs")

4. Select the matching attribute from the **Customer ID in results** drop-down list that maps to your Customer Insights CustomerId. When you're done, select **Save**.

   > [!div class="mx-imgBorder"] 
   > ![Configure Web Service output](media/intelligence-screen3.png "Configure Web Service output")

5. You'll see the **Workflow Saved** screen, and attributes about your new workflow that will be important to remember.

   > [!div class="mx-imgBorder"] 
   > ![Review Workflow Configuration](media/intelligence-screen4.png "Review Workflow Configuration")

   1. **Workflow name:** This is the recognizable name for your workflow.
   2. **Entity created:** This is the name of the entity where the output from your workflow will be stored. You can find this entity on the **Entities** page.

6. Select **Done** to return to the **Intelligence** page.

## Edit a workflow

1. Within the **Intelligence** page, select the vertical ellipses in the **Actions** column next to a workflow you've previously created, and then select **Edit**.

   > [!div class="mx-imgBorder"] 
   > ![Edit Action](media/intelligence-action-edit.png "Edit Action")

2. You can update your workflow's recognizable name in the **Display name** field, but changing the web service is not possible. If you wish to create a new prediction using a different web service, you can refer to the Add a new workflow section for instructions. When you're done, select **Next**.

3. For each **Web service input**, select the matching **Entity** from Customer Insights. When you're done, select **Next**.

4. Select the matching attribute from the **Customer ID in results** drop-down list that maps to your Customer Insights CustomerId. When you're done, select **Save**.

## Running a workflow

1. Within the **Intelligence** page, select the vertical ellipses in the **Actions** column next to a workflow you've previously created, and then select **Run**.

   > [!div class="mx-imgBorder"] 
   > ![Run Action](media/intelligence-action-run.png "Run Action")

Your workflow will also automatically run each time you have a scheduled refresh. Learn more about [setting up scheduled refreshes](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-settings#schedule-tab).

## Deleting a workflow

1. Within the **Intelligence** page, select the vertical ellipses in the **Actions** column next to a workflow you've previously created, and then select **Delete**.

   > [!div class="mx-imgBorder"] 
   > ![Edit Action](media/intelligence-action-delete.png "Edit Action")

Your workflow will be deleted, but the entity that was created when you created the workflow will remain in the **Entities** page.

