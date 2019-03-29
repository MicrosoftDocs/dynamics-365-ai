---
title: "Topics dashboard"
description: "Learn about the customer service insights available on the Topics dashboard​."
keywords: ""
ms\.date: 3/27/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Topics dashboard

[!INCLUDE [public-preview](../includes/public-preview.md)]

> ![Topics dashboard](media/topics-dash.png)

The Topics dashboard uses artificial intelligence technology to group related support cases as support topics and display them in order of the number of cases associated with each topic. You can then filter the list by searching for topics related to a specific keyword, view each topic's support cases, and fine-tune the way cases are grouped into topics.

## Filter the list by searching for topics related to a specific keyword

You can narrow down the list of topics displayed on the Topics dashboard by searching for a specific keyword in the **Search** box in the upper right corner of the dashboard.

For example, to find topics related to login issues, enter *login* in the **Search** box. Customer Service Insights narrows down the list to topics that include the word *login*.

> ![Search box](media/search-box.png)

To restore the original topic list, clear the search box by selecting the close icon.

> ![Clear search](media/clear-search.png)

## View a topic's support cases

You can view the support cases associated with a topic by selecting it in the Topics list. For example, to view the support cases associated with the *Password reset link is invalid* topic, select it in the list.

> ![View cases](media/view-cases.png)

Customer Service Insights displays a list of the support cases associated with the topic.

> ![Cases list](media/cases-list.png)

Note that the titles of the support cases associated with the *Password reset link is invalid* topic include variations of phrases related to password reset problems. Based on these similarities, Customer Service Insights uses artificial technology to group the cases together in a single topic.

To view the details of a support case, click the case title in the list.

> ![View support details](media/view-support-details.png)

Customer Service Insights opens the support case details in Dynamics 365.

> ![Open support details](media/open-support-details.png)

## Fine-tune the way cases are grouped into topics

You can fine-time the way Customer Service Insights artificial intelligence technology groups support cases into topics by rating the the placement of cases within topics. By rating the placement, you can help the artificial intelligence technology learn and improve case grouping.

To rate a case, hover over the case title, and you will see two rating icons appear.

Select Thumbs Up to indicate the case has been classified correctly. Select Thumbs Down to indicate the case was not classified correctly.