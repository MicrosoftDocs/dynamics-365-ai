---
title: "Custom Models | Microsoft Docs"
description: "Work with custom models from Azure Machine Learning in Dynamics 365 Customer Insights."
ms.date: 02/12/2020
ms.reviewer: ""
ms.service: dynamics-365-ai
ms.topic: "article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Custom Models

The **Custom Models** page lists workflows based on Azure Machine Learning models. Workflows help you choose the data you want to generate from insights and map the results to your Customer Insights data. [Read the blog about extending Customer Insights with custom models based on Azure Machine Learning](https://cloudblogs.microsoft.com/dynamics365/it/2019/10/04/extending-dynamics-365-customer-insights-with-azure-ml-based-custom-models/) and the [blog with examples of custom models](https://cloudblogs.microsoft.com/dynamics365/it/2019/10/05/examples-of-extending-dynamics-365-customer-insights-with-azure-ml/).

## Prerequisites

- To deploy custom models, you need [Azure Machine Learning Enterprise edition](https://azure.microsoft.com/pricing/details/machine-learning/).

- You need an Azure Data Lake Storage Gen2 storage account associated with your Azure Studio instance to use this feature. For more information, see [Create an Azure Data Lake Storage Gen2 storage account](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-quickstart-create-account)

## Add a new workflow

1. On the **Custom Models** page, select **New Workflow**.

2. Give your workflow a recognizable name in the **Display name** field. Choose the [web service you've published using Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/studio/deploy-a-machine-learning-web-service#deploy-it-as-a-new-web-service) in the **Web service that contains your model** dropdown. Then select **Next**.

3. For each **Web service input**, select the matching **Entity** from Customer Insights and select **Next**.

   > [!div class="mx-imgBorder"]
   > ![Configure a workflow](media/intelligence-screen2.png "Configure a workflow")

4. Select the matching attribute from the **Customer ID in results** drop-down list that maps to your Customer Insights CustomerId and select **Save**.

5. You'll see the **Workflow Saved** screen, and attributes about your new workflow that will be important to remember:

   > [!div class="mx-imgBorder"]
   > ![Review workflow configuration](media/intelligence-screen4.png "Review workflow configuration")

   1. **Workflow name:** The display name for your workflow.
   2. **Entity created:** The name of the entity where the output from your workflow will be stored. You can find this entity in the **[Entities](pm-entities.md)** page.

6. Select **Done** to return to the **Custom Models** page.

## Edit a workflow

1. On the **Custom Models** page, select the vertical ellipses in the **Actions** column next to a workflow you've previously created and select **Edit**.

2. You can update your workflow's recognizable name in the **Display name** field, but changing the Web service isn't possible. If you want to create a new prediction using a different web service, follow the steps in [Add a new workflow](#add-a-new-workflow). When you're done, select **Next**.

3. For each **Web service input**, select the matching **Entity** from Customer Insights.  When you're done, select **Next**.

4. Select the matching attribute from the **Customer ID in results** drop-down list that maps to your Customer Insights CustomerId.  When you're done, click **Save**.

## Run a workflow

1. On the **Custom Models** page, select the vertical ellipses in the **Actions** column next to a workflow you've previously created.

2. Select **Run**.

Your workflow also runs automatically when there's a scheduled refresh. Learn more about [setting up scheduled refreshes](pm-settings.md#schedule-tab).

## Delete a workflow

1. On the **Custom Models** page, select the vertical ellipses in the **Actions** column next to a workflow you've previously created.

2. Select **Delete**.

Your workflow will be deleted. The entity that was created when you created the workflow persists, and can be viewed from the **Entities** page.
