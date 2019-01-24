---
title: "Enrich Profiles MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 11/05/2018
ms.reviewer: ""
ms.service: "dynamics-365-ai"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
# Enrich Profiles

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Through it's **Configure Data** process, Customer 360 enables you, the user, to consolidate data around your customers from all of your sources. At the same time, Customer 360 goes beyond that and put at your fingertips additional ML-produced knowledge about your customers that comes from propriatery data. This section covers the **Enrich Profiles** screen that can be used to **unlock data on the affinity of your customers to hundreds of brands and dozens of interest-categories** (which might be *Home Appliances*, *Shoes* or *Financial loans* as an example).

Note: The *Enrich Profiles* screen can be accessed both through the app left-side menu and from the *Configure Data* screen as shown:

// enrich 1

Note: Completing both the **Data Ingestion** and **Data Configuration** processes is a prerequisite to enrichment. Hence, if you didn't complete one or more of those steps you can expect to get the following notification:

// enrich notification

### Exploring the *Enrich Profiles* Screen

//enrich 2

As shown above, this screen includes two major sections:
- The **Demographics** section, where you should make selections for at least two fields among **Date of Birth**, **Gender** and **Zip Code**. The intent behind these selections is to focus on the specific cohort of customers for which you wish to gain knowledge around preferred brands and interests. 
- The **Brands and Categories** section, where you can take one of two approaches: **Choose on my own** and **Industry's top Brands and Categories**.

### Making Selections on the *Demographics* Section

// enrich 3

As mentioned earlier, you are required to make at least two selections. 
**Note** that only some formats are supported for each of the fields:
- Supported formats for **Date of Birth**: M/d/yyyy, MMMM d, yyyy-mm-dd, MMMM yyyy
- Supported formats for **Gender**: Male, Female, Unknown
- Supported formats for **Zip Code**: Should be a 5-digit US zip code (only US supported at this point)

### Making Selections on the *Brands and Categories* Section

// enrich 3

First choose one of the following options. Then complete your selections for that option.
- 1.**Choose on my own**: This option allows you to choose brands and interest-categories that are of most interest to you and get your customers' affinities for those selections. For example, *Coca-Cola* and *Starbucks* were chosen in the example below:
  
// enrich 4

To add a brand or interest, type the keywords field (highlighted in blue above) and than type a keyword. If that keyword matches a brand or interest name in the Microsoft database it will be saved. Note however that you can save up to five selections. If there is no match, you will get the following clickable notice which you can use to send a suggestion to the Customer 360 team:

// enrich 5

- 2. **Industry's top brands and categories**: Get the brands and interests which all of your customers, taken together, have the highest affinities with. Note that in *Customers* we refer only to the customers you chose in the *Demographics* section. In the example below, *Home&Garden* was chosen as an industry:
  
// enrich 6

Here is the list of supported industries: 
  
### Running the Enrichment Process
That can be easily done via the **Run** button at the top of the screen:

// enrich 6

### Exploring the Enrichment Process Output


