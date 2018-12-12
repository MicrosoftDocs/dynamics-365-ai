---
title: "Responding to GDPR Data Subject Delete Requests for Dynamics 365 AI for Customer Service Virtual Agent"
description: "Learn how to respond​ to GDPR Data Subject Delete Requests for Dynamics 365 AI for Customer Service Virtual Agent."
keywords: ""
ms\.date: 12/10/2018
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Responding to GDPR data subject delete requests for Dynamics 365 AI for Customer Service Virtual Agent

The “right to erasure” by the removal of personal data from an organization’s customer data is a key protection in the General Data Protection Regulation (GDPR). Removing personal data includes removing all personal data and system-generated logs, except audit log information.

## Manage delete requests

Dynamics 365 AI for Customer Service Virtual Agent offers the following experiences to delete personal data for a specific user:

* [Bot chat logs](#bot-chat-logs)
* [Case data connection settings](#case-data-connection-settings)
* [Delete Virtual Agent Designer bot content](#delete-virtual-agent-designer-bot-content)
* [Delete Virtual Agent Designer telemetry](#delete-virtual-agent-designer-telemetry)
* [Extracted knowledge](#extracted-knowledge)
* [Metrics](#metrics)
* [System telemetry](#system-telemetry)

### Bot chat logs

Bot chat logs are deleted when the bot is deleted.

### Case data connection settings

Case data connection settings are deleted when the bot is deleted.

### Delete Virtual Agent Designer bot content

You can follow these steps to delete a bot from from AI for Customer Service Virtual Agent:

1. Launch the Virtual Agent Designer in your browser.
2. On the Settings menu, select **Delete Bot**.

    > [!div class="mx-imgBorder"]
    > ![Delete bot](media/delete-bot.png)

All bot content will be immediately deleted.

### Delete Virtual Agent Designer telemetry

Virtual Agent Designer telemetry data is automatically deleted within 29 days.

### Extracted knowledge

Extracted knowledge, including topic suggestions, is deleted when the bot is deleted.

### Metrics

To delete metrics data, you must delete your bot. See [Delete Virtual Agent Designer bot content](#delete-virtual-agent-designer-bot-content) for information on deleting a bot.

### System telemetry

System telemetry is automatically deleted within 29 days.