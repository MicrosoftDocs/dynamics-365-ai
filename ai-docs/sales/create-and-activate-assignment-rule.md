---
title: "Create and activate assignment rules for routing | MicrosoftDocs"
description: "Create and activate assignment rules for leads and opportunities by defining conditions to automatically assign records to sellers when the defined conditions are met in Dynamics 365 Sales."
ms.date: 09/10/2021
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# Create and activate an assignment rule

As a sequence manager, you create an assignment rule for lead and opportunity records by defining different conditions such as segment, sellers, and lead or opportunity distribution. After a rule is activated and a record satisfies the conditions that are defined in the rule, the record is automatically assigned to a seller. When records are created in Dynamics 365 Sales, you don't have to manually assign them to sellers.

When a lead or opportunity record is created in an organization, assignment rules are applied from the top of the order in which they're listed. When the record satisfies the conditions defined for a rule, that rule is applied to the record. By default, rules are listed in the order in which they were created, with the most recent at the bottom. You can select and drag the rules into any order you want.

>[!NOTE]
>For the example in this procedure, we create a lead assignment rule. Similarly, you can use this procedure to create an opportunity assignment rule.  

**To create and activate an assignment rule**

1. Sign in to your Dynamics 365 Sales Hub app.

2. Go to the **Change area** ![change area](media/change-area-icon.png) in the lower-left corner of the page, and select **Sales Insights settings**.

3. Under **Sales accelerator**, select **Assignment rules (preview)**.

4. On the **Assignment rules** page, select **+ New rule** and then select **Lead assignment rule**.

   >[!div class="mx-imgBorder"]
   >![Select the lead assignment rule option from a new rule.](media/sa-ar-create-assignment-rule-select-lead.png "Select the ead assignment rule option from a new rule")   

    The **Create assignment rule** pane opens.    
    >[!div class="mx-imgBorder"]
    >![Create assignment rule pane.](media/sa-ar-create-assignment-rule-right-pane.png "Create assignment rule pane")   

5. Under **Rule name**, enter a name for the rule.

6. <a name="setSegment"></a>Under **Select eligible Leads for this rule**, select one of the following options:

    - **All incoming leads**: All the new leads that are created will be assigned to sellers in accordance with the conditions defined in the rule.
    - **Specific lead**: Select a segment from the **Choose segment** dropdown menu to connect leads that are available in the segment to sellers in accordance with the conditions defined in this rule. All the active segments that are related to leads that are displayed in the list. However, if you want to create a segment that's not in the list and is specific to this rule, select **+ New segment** from the **Choose segment** dropdown list. More information: [Create and activate a segment](create-and-activate-a-segment.md)

      >[!div class="mx-imgBorder"]
      >![Select a new segment from the Choose segment dropdown menu.](media/sa-segment-assignment-rule-specific-lead.png "Select new segment from choose segment dropdown")

      >[!NOTE]
      >If no segment is selected for a rule, or no segment is defined in the application, you can select the default segment that's applied on all leads.

      Also, you can configure more settings to determine how the leads in the segment must be assigned to sellers. Select **Additional condition**, and then select **+ Add**. Configure the conditions as follows:

        - **Add row**: Add conditions for when the segment should be applied. In the following example, we add a row to specify that this segment be applied to leads created by the user **John Thomas**:

          1. Select an attribute from the dropdown list in the first column.
          2. Select an operator from the dropdown list in the second column.
          3. Enter a value to filter by in the third column.

          >[!div class="mx-imgBorder"]
          >![Screenshot showing the attribute Created By, the operator Equals, and the value John Thomas.](media/sa-segment-condition-add-row.png "Add a condition row")

          Similarly, you can create more conditions to further filter the leads to apply the segment to.

        - **Add group**: Add multiple conditions as a group to your segment if you want to filter leads by using more than one field:

          1. Select **And** or **Or** to group the conditions.   

             >[!div class="mx-imgBorder"]
             >![Add a condition group.](media/sa-segment-condition-add-group.png "Add a condition group")

          2. Select the conditions that you want to add to the group.

             >[!div class="mx-imgBorder"]
             >![Add conditions to the group.](media/sa-segment-condition-add-group-select-condition.png "Add conditions to the group")

            When you select **And**, this segment is only applied to leads that meet both criteria. When you select **Or**, the segment is applied to leads that meet any of the filter criteria. For example, to apply this segment to leads that were created by Kenny Smith and have the company name Contoso, select **AND**. Similarly, you can create multiple groups and further filter the leads based on the conditions defined in the groups.

        -	**Add related entity**: Add a condition based on the attributes of related entities.
            Select an attribute from the **Related Entity** list in the topmost field, and then choose **Contains data** or **Does not contain data**. This enables the condition section.

            >[!div class="mx-imgBorder"]
            >![Add related entity condition.](media/sa-segment-condition-add-related-entity.png "Add related entity condition")

7. Under **Assign these leads to sellers or a team**, choose one of the options described in the following table.

    | Option | Description |
    |--------|-------------|
    | Any seller | Assign leads to any seller according to their availability, capacity, or distribution pattern. |
    | Seller with matching attributes | Assign leads to sellers who satisfy the conditions defined through attributes selected from Dynamics 365 or assignment rules. The following options are available:<ul><li>Use existing fields from seller records in Dynamics 365.</li><li>Use seller attributes defined for assignment rules. More information: [Manage seller attributes](manage-seller-attributes.md)</li></ul>For example, you want to assign leads to sellers who are based out of Seattle. Select the **Use existing fields from seller records in Dynamics 365** option, and then select **+ Add** > **Add row**. Enter the condition as **City** (attribute) **Equals** (condition) **Seattle** (value).<br>![Seller with matching attributes.](media/sa-ar-seller-with-matching-attributes.png "Seller with matching attributes") |
    | Specific sellers | Assign leads to specific sellers. Select the sellers from the **Choose sellers** lookup.<br>**Note**: The security roles for sellers displayed in the list were added when the sales accelerator was configured. More information: step 4 in [Configure the sales accelerator](enable-configure-sales-accelerator.md)<br>![Select specific sellers.](media/sa-ar-select-specific-sellers.png "Select specific sellers") |
    | Specific teams | Assign leads to a specific team. The lead will be available for all members of the team you select. The teams must be defined in your organization. More information: [Manage teams](/power-platform/admin/manage-teams#ownergroup-team-or-access-team) |

8. Under **Distribute leads by**, choose one of the following options. This setting is available only when you select a seller option in the **Assign these leads to** section.

   >[!NOTE]
   >The **Distribute leads by** setting isn't available for teams.

   - **Round robin**: Leads are distributed on a cyclical basis to sellers who are qualified to receive the lead, based on the conditions of the assignment rule.
   - **Load balancing**: Leads are distributed among sellers depending on their current workload. This helps ensure that all sellers are equally busy.
   - **Consider seller availability** (optional): Select this checkbox to take the availability of the seller into account when assigning leads. More information: [Configure your work availability](personalize-sales-accelerator.md#configure-your-work-availability)

     >[!NOTE]
     >
     >- If sellers don't update their [work availability](personalize-sales-accelerator.md#configure-your-work-availability), the application always considers them to be available and assigns them leads.
     >- To assign leads, the application first considers those sellers who are currently available. If no seller is currently available, the application considers the sellers who will be available within 24 hours. If no seller will be available within this timeframe, the application considers sellers who will be available within 48 hours. In this manner, the application verifies the sellers' availability up to 120 hours. If no seller will be available within the 120-hour limit, the lead isn't assigned.

   - **Consider seller capacity** (optional): Select this checkbox to take into account the maximum number of leads a seller can handle at once. More information: [Set lead capacity for sellers](manage-sales-teams.md#set-capacity-for-sellers)

      >[!div class="mx-imgBorder"]
      >![Screenshot showing the Distribute leads by setting with the Consider seller capacity checkbox selected.](media/sa-ar-distribute-leads-by.png "Consider seller capacity checkbox")

9. Select **Create rule**.

The rule is created and activated. It will be listed in the **Rules** section, which is organized in ascending order by date; the most recently created rule is always listed at the bottom of the list unless you move it.


### See also

[Manage assignment rules](create-manage-assignment-rules.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
