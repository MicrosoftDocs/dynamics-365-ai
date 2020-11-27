---	
title: "Analyze deals flow between snapshots in Dynamics 365 Sales Insights | MicrosoftDocs"	
description: "Analyze deals flow between snapshots in Dynamics 365 Sales Insights."	
ms.date: 10/26/2020	
ms.service: crm-online
ms.custom: 	
ms.topic: article	
author: udaykirang	
ms.author: udag	
manager: shujoshi	
---	

# Analyze deals flows between snapshots	

The **Flow** chart provides a visual representation of how the forecast changes between two moments in time. Managers can use flow charts to drill into the specific deals that have contributed to the increase or decrease in forecast commitment, thus, enabling them to follow up with their teams and coach their teams on how to improve their forecast accuracy.	

Review the following prerequisite before you start using deals flow analysis:	

- Verify that at least two snapshots have been created for the forecast. To learn more, see [Take snapshots automatically](manage-snapshots-forecast.md).	

**View and understand a deals flow**	

1.	Sign in to the **Sales Hub** app and go to **Performance** > **Forecasts**.	  
2.	Select a forecast, and then choose a forecast period for the forecast.	  
3.	Select the **Flow** tab.	  
    A sankey chart is displayed with a comparison between two latest snapshots for the forecast. The order of forecast categories depends on how the forecast columns are arranged in the grid view.   
    > [!div class="mx-imgBorder"]	
    > ![Deal flown sankey chart](media/predictive-forecasting-deal-flow-sankey-chart.png "Deal flown sankey chart")    
4.	To compare snapshots, choose a **Start** and **End** dates from the calendar. The start date should always be older than the end date. In this example, the start date is selected as **1** and end date is selected as **27** in the month of July.	  
    > [!div class="mx-imgBorder"]	
    > ![Select start and end date](media/predictive-forecasting-deal-flow-select-start-end-date.png "Select start and end date")    	  

    Select **Apply**. The chart is updated to display the deal flow.	  

    > [!div class="mx-imgBorder"]	
    > ![Deal flow chart between dates](media/predictive-forecasting-deal-flow-chart-between-dates.png "Deal flow chart between dates")    	 	
    
    - The topmost stack in the column displays the date with aggregated opportunity amount, and the number of opportunities that are influencing the aggregated amount.	
    -	The other columns on the stack display the forecast categories and the aggregated opportunity amount for that snapshot in the order defined when the forecast was configured.	
    
    -	The opportunities that are not part of end date snapshot and part of start date snapshot are classified under **Removed** category, and added to the bottom of the column stack under the end date snapshot.    
        The opportunities that are not part of the end date snapshot due to ownership change (with in forecast) or date change (with in forecast), are not part of this category rather part of another category known as [**Pushed out**](#pushed-out) and [**Pulled in**](#pulled-in) categories.   

    -	New opportunities that are present in the end date snapshot and not available in start date snapshot are classified as **New deals** category under the start date snapshot column stack.    
        The opportunities that are added to the end date snapshot due to ownership change (with in forecast) or date change (with in forecast), are not part of this category rather part of another category known as [**Pushed out**](#pushed-out) and [**Pulled in**](#pulled-in) categories. 	
    
    - <a name="pulled-in"></a>The opportunities that are added to the end date snapshot due to ownership change (with in forecast) or date change (with in forecast), are classified under **Pulled in** category under the bottom of the start date snapshot.   
    
    - <a name="pushed-out"></a>The opportunities that are added to the start date snapshot due to ownership change (with in forecast) or date change (with in forecast), are classified under **Pushed out** category under the bottom of the end date snapshot.   
        Let's look at the following examples:    
        - **Date change**: Few opportunities of Kenny Smith are moved from the 22 July (Q3) to 26 November (Q4) and these opportunities are shown under **Pushed out** category for Q3 and **Pulled in** category for Q4.     

            > [!div class="mx-imgBorder"]	
            > ![Example for pulled in and pushed out](media/predictive-forecasting-deal-flow-chart-kenny-smith.png "Example for pulled in and pushed out")    

            1. **Pulled in**: Opportunities date is moved from Q3 to Q4.   
            2. **Pushed out**: Owner moved out of the forecast hierarchy.     
        
        - **Ownership change**: Dustin Ochs has two opportunities and are transferred to Amber Rodriguez. The transferred opportunities appear under the Pushed out category for Dustin Ochs and **Pulled in** category for Amber Rodriguez.   

5.	To view the summary and flow of a forecast category:	

    -	Hover over a forecast category in the stack, a summary of the category is displayed, including the forecast category with snapshot date, the aggregated budget amount, and the number of opportunities that are influencing the aggregated amount. Also, the flow is highlighted to show how the opportunities are trending between the snapshots.	

    -	This flow depends on how the status of the opportunity in a forecast category of the snapshot of start date changed to the other forecast category in the snapshot of end date. If there's no change in the status of the opportunity, the flow remains the same between forecast categories in the snapshots.	

6.	To view underlying opportunities, select a forecast category. The opportunities are displayed in a grid with side-by-side comparison of how the granular data for each opportunity—such as owner, value, date, and forecast category&mdash;is changing in columns from start date to end date.	

    > [!div class="mx-imgBorder"]	
    > ![Underlying opportunities of a forecast category](media/predictive-forecasting-deal-underlying-opportunities-forecast-category.png "Underlying opportunities of a forecast category")	

    You can't edit the opportunities inline. However, in the **Action** column, select the navigate icon corresponding to the opportunity that you want to edit and the opportunity is opened in a browser tab. The saved changes won't affect the status of the opportunity in the snapshot, because the snapshots are taken at a moment in time by using frozen data.	

### Whose deals flow am I viewing?	

You can identify whether the selected flow is for a team or an individual by looking at the deals flow heading:	

-	If the heading name contains **Username (Group)**, you're looking at a user's team's deals flow.	

-	If the heading name contains only **Username**, you're looking at an individual user's deals flow.	

The deals flow of other users that you can see depend on the sales hierarchy defined for you. To learn more, see [Forecasts and sales hierarchy](https://docs.microsoft.com/dynamics365/sales-enterprise/view-forecasts#forecasts-and-sales-hierarchy).	


### See also	

[Manage snapshots for a forecast](manage-snapshots-forecast.md)<br>	
[About premium forecasting](configure-premium-forecasting.md)
