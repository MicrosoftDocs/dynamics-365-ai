# Overview about data sources

Customer Insights connects data from a broad set of sources. Connecting a data source to Customer Insights is often referred to as the process of *data ingestion*. After bringing th data into customer Insights, you can unify the data and get a holistic view of the customer data, and take action on it.

You can add a data source via three main ways:

- [Through dozens of Power Query connectors](connect-power-query.md)
- [From a Common Data Model folder](connect-common-data-model.md)
- [From your own Common Data Service lake](connect-common-data-service-lake.md)

> [!NOTE]
> You can't add data from on-premises data sources yet.

## Manage existing data sources

**Michael** to re-use the existing content that applies to all types of data sources

### Edit an existing data source

### Delete a data source from Customer Insights

## Incremental refresh for large data sources

Incremental refresh for data sources in Customer Insights provides the following advantages:

- **Faster refreshes** - Only data that has changed gets refreshed. For example, you might refresh only the past five days of a historical dataset.
- **Increased reliability** - With smaller refreshes, you don't need to maintain connections to volatile source systems for as long, reducing the risk of connection issues.
- **Reduced resource consumption** - Refreshing only a subset of your total data leads to more efficient use of computing resources and decreases the environmental footprint.

### Configure incremental refresh

Customer Insights allows incremental refresh for data sources that support incremental ingestion. For example, Azure SQL databases with date and time fields, which indicate when data records were last updated.

1. In Customer Insights, [create a new data source](data-sources.md).

1. Provide a name for the data source.

1. Select a data source that supports incremental refresh, such as Azure SQL database.

1. Select the entities or tables to ingest into Customer Insights and transform the data.

1. Complete the transformation steps and select **Next**.

1. In the **Set up incremental refresh** dialog box, select **Set up** to open the **Incremental refresh settings**. If you select **Skip**, the data source will refresh the entire data set.
   > [!TIP]
   > You can also apply incremental refresh later by editing an existing data source.

1. On **Incremental refresh settings**, you'll configure the incremental refresh for all entities that you selected when creating the data source.

   > [!div class="mx-imgBorder"]
   > ![Configure entities in a data source for incremental refresh](media/incremental-refresh-settings.png "Configure entities in a data source for incremental refresh")

1. Select an entity, and provide the following details:

   - **Define the primary key**: Select a primary key for the entity or table.
   - **Define the "last updated" field**: This field will only display attributes of type date or time. Select an attribute that indicates when the records were last updated. It'll be used to identify the records that fall within the incremental refresh time frame.
   - **Check for updates every**: Specify how long you want the incremental refresh time frame to be.

1. Select **Save** to complete the creation of the data source. The initial data refresh will be a full refresh. Afterwards, the incremental data refresh happens as configured in the previous step.

## Review ingested data

After adding data sources to Customer Insights, each data source creates its own user entity. Refer to the entites article to learn more. 

**Aditya** to review the entites article if all is accurate. 