---
title: "Use and manage workspaces to connect to different customer service environments in Dynamics 365 Customer Service Insights"
description: "Understand how to use and manage workspaces to connect to different customer service environments the Dynamics 365 Customer Service Insights product."
keywords: ""
ms.date: 02/01/2021
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid:
author: lalexms
ms.author: laalexan
manager: shujoshi
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150

---

# Use and manage workspaces to connect to different customer service environments

When you work with the dashboards in Dynamics 365 Customer Service Insights, you have a choice of connecting to a live customer service environment or exploring the dashboards using sample data in the demo workspace. You can then create additional workspaces to gain insights into different customer service environments and switch between the workspaces.

You can use and manage workspaces in a variety of ways, including:

- [Create a workspace](#create-a-workspace)
- [Open the demo workspace](#open-the-demo-workspace)
- [Switch between workspaces](#switch-between-workspaces)
- [Share a workspace](#share-a-workspace)
- [Delete a workspace](#manage-access-to-workspaces)

## Create a workspace

> [!Note] 
> For users who hold hold Customer Service Enterprise licenses, you will no longer be able to create new workspaces. Instead, consider migrating to the embedded experience within the core Dyanmics Customer Service Applications.

1. Launch Customer Service Insights by opening a browser and navigating to https://csi.ai.dynamics.com.
   
   ![Launch Customer Service Insights](media/launch-csi.png "Launch Customer Service Insights from a browser")

    Customer Service Insights opens a **Connect your data** page, where you can create a workspace by connecting to a data source.
    
 2. Each workspace displays customer service data from a specific customer service data environment. To connect to a Dynamics 365 Customer Service Insights environment, select **Dynamics 365** to display the **Choose an environment** page.
 
    ![Select an environment](media/select-environment.png "Select an environment")
 
    You can gain insights into multiple sets of customer service data by creating workspaces that each connect to a different environment. For example, you could create different workspaces for environments containing customer support information for specific areas, such as beauty products, retail, or banking.
    
    ![Create workspaces](media/create-workspaces.png "Create workspaces")
    
 3. To configure the workspace, select the environment you want to use. 
 
    Customer Service Insights opens the workspace and displays that environment's customer support data in the dashboards. 

4. You can also create a new workspace by selecting the **Workspaces** icon on the Customer Service Insights title bar, and then selecting **+Workspace**. 

    ![Create a new workspace](media/create-new-workspace.png "Create a new workspace")

## Open the demo workspace

By default, Customer Service Insights displays sample customer support data in a demo workspace. To open the demo workspace, select **demo workspace** on the **Connect your data** page, or close the **Connect your data** page. 

![Open a demo workspace](media/workspace-demo.png "Open a demo workspace")

## Switch between workspaces

Once you've created one or more workspaces, you can easily switch between them, including the demo workspace. 

To switch to a different workspace, select the **Workspaces** icon on the Customer Service Insights title bar. Customer Service Insights opens the **My workspaces** pane. The current workspace is marked with a checkmark. Select a different workspace to make it the current workspace.

![Switch between workspaces](media/workspaces-switch.png "Switch between workspaces")

Customer Service Insights opens the workspace and displays the customer service data associated with the workspace in the dashboards. The next time you visit Customer Service Insights, it will open the last workspace you switched to.

## Share a workspace

If you want other users to have access to your workspace, you can share it.

To share a workspace, select the **Workspaces** icon on the Customer Service Insights title bar to open the **My workspaces** pane. Hover over the workspace you want to share to display the **Share** icon, and then select the icon. 

 ![Share a workspace](media/share-a-workspace.png "Share a workspace")

On the **Share** tab of the **Share this workspace** dialog box, enter the email address of a user who has a Customer Service Insights license to share the workspace. Users receive an email with an optional message when a workspace is shared.

## Manage access to workspaces

There are two roles, with different permissions levels, for users of workspaces: 

- **Owner**: Creator of a workspace.
  Owners can manage access to their workspaces by adding and removing users. 

- **Viewer**: Read-only role to see a shared workspace without the ability to edit.
  Viewers can access workspaces shared with them, and remove shared workspace from their "My workspaces" list. 

### Delete a workspace 

If you no longer want Customer Service Insights to display a workspace in the list of current workspaces, you can delete it. 

To delete a workspace:

1. If you are the owner of a workspace, select the **Workspaces** icon on the Customer Service Insights title bar to open the **My workspaces** pane.

2. Hover over the workspace you want to delete, then select the **Delete** icon.

    ![Delete a workspace](media/delete-workspace.png "Delete a workspace")

If you are a viewer of a shared workspace, you can remove a shared workspace from your view by using the same **Delete** icon as noted above, or use the **Share** icon to use the **Share this workspace** dialog box to remove yourself from the list. **Note**: This only removes the shared workspace from your view. It doesn't delete the workspace for other users.

 ![Remove a workspace from view](media/remove-workspace-1.png "Remove a workspace from your view")
     
 ![Delete a workspace from view](media/remove-workspace-2.png "Delete a workspace from your view")
    
