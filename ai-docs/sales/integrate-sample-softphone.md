---
title: "Integrate a sample softphone dialer with Dynamics 365 Sales | MicrosoftDocs"
description: "Learn how to integrate a sample softphone dialer with Dynamics 365 Sales  ."
ms.date: 04/01/2020
ms.service: crm-online
ms.topic: article
author: sbmjais
ms.author: shjais
manager: shujoshi
---

# Integrate a sample softphone dialer with Dynamics 365 Sales

A softphone dialer provides a simple and integrated way to call customers from within Microsoft Dynamics 365 Sales. When a phone call is made, a Phone Call activity is created in Dynamics 365 Sales.   The Phone Call activity captures details such as subject, phone number, and name of the contacts who made and received the call.

Organizations can integrate a softphone dialer from their telephony provider in Dynamics 365 Sales using Dynamics 365 Channel Integration Framework. Once integrated, sales reps can quickly call their contacts with a single click from within the Sales Hub app using the Sales Acceleration features.  

This topic describes how to install a sample app and test the calling capabilities.

> [!IMPORTANT]
> - The sample code for softphone integration with Dynamics 365 using Dynamics 365 Channel Integration Framework is made available so customers can get early access and provide feedback. The sample code is not meant for production use and might have limited or restricted functionality.
> - Microsoft doesn't provide support for this sample code. Microsoft Dynamics 365 Technical Support won’t be able to help you with issues or questions. This is subject to a [separate supplemental terms of use](https://go.microsoft.com/fwlink/p/?LinkId=511446).

## Integrate and configure the sample softphone dialer

To configure the sample:

1.	Get Dynamics 365 Channel Integration Framework from Microsoft AppSource. For information on prerequisites and how to get Dynamics 365 Channel Integration Framework, see [Get Dynamics 365 Channel Integration Framework](https://docs.microsoft.com/dynamics365/customer-service/channel-integration-framework/get-channel-integration-framework).

2.	Integrate the sample app available on the [Download Center](https://go.microsoft.com/fwlink/p/?linkid=2104590) using Dynamics 365 Channel Integration Framework. To learn more about integrating a sample app, see [Sample softphone integration using Channel Integration Framework](https://docs.microsoft.com/dynamics365/customer-service/channel-integration-framework/sample-softphone-integration).

    > [!IMPORTANT]
    > You must use the sample app from the [Download Center](https://go.microsoft.com/fwlink/p/?linkid=2104590) link, and not the one that's mentioned in the [Sample softphone integration using Channel Integration Framework topic](https://docs.microsoft.com/dynamics365/customer-service/channel-integration-framework/sample-softphone-integration).

3.	Configure the channel provider for your Dynamics 365 Sales organization. More information: [How to configure a channel provider for your Dynamics 365 organization](https://docs.microsoft.com/dynamics365/customer-service/channel-integration-framework/configure-channel-provider-channel-integration-framework)

> [!IMPORTANT]
> A Phone Call activity is created before a phone call is initiated from the softphone dialer. As an existing customer of Channel Integration Framework, if you have configured or implemented your system to create a Phone Call activity within the softphone dialer, you must remove the configuration or implementation to avoid creation of duplicate Phone Call activities. 
