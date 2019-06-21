---
title: "Integrate a bot built using the Microsoft Bot Framework and Cognitive services with Microsoft Dynamics 365 AI for Customer Service"
description: "Step by step guidance on using your existing Bot Framework bot with Microsoft Dynamics 365 AI for Customer Service"
ms.date: 06/17/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Integrate a bot built using the Microsoft Bot Framework and Cognitive services with Microsoft Dynamics 365 AI for Customer Service

## Overview 

This document covers the following steps to use Microsoft Bot Framework's dispatcher tool and integrate your existing bot with your Dynamics 365 Virtual Agent for Customer Service bot,

1. Retrieve topics, utterances and secrets from your virtual agent tenant (TO-DO anchor links)
1. Convert virtual agent topics & utterances into LU-down format
1. Train dispatcher custom model with your virtual agent's topics
1. Deploy dispatcher with custom model
1. Test dispatcher working seamlessly with your bots

## Pre-requisites

* Bot built using Bot Builder v4 SDK - [TO DO - click here](https://URL)
* Visual Studio 2017 or higher - [TO DO - click here to download](https://URL)
* Familiarity with [Microsoft Bot Framwork's dispatcher tool](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-tutorial-dispatch?view=azure-bot-service-4.0&tabs=csaddref%2Ccsbotconfig)
* Bot Emulator v4 - [click here for github repo](https://github.com/microsoft/BotFramework-Emulator)
* Virtual Agent utilities & sample code - [TO DO - click here for github repo](https://msazure.visualstudio.com/CCI/_git/Users?path=%2Fsabacha%2FCCIToLU&version=GBmaster)

### 1. Retrieve topics, utterances and secrets from your virtual agent tenant
From your Virtual agent designer, you will need to retrieve bot content (topics & utterances) and your tenant’s endpoint and direct line secret. Here are steps to perform,

#### 1.	Retrieve bot ID, tenant ID, and auth token from your bot
  a.	Open Developer Tools (F12) for your web browser
  b.	Sign-in to your Virtual Agent using your AAD credentials http://va.ai.dynamics.com
  c.	Go to <Network Tab> (see screenshot below)
      <TO DO - Screenshot>
  d.	Filter and look for “client” request (see screenshot below)
      <TO DO - Screenshot>
  e.	Copy and persist the following details (see screenshot below)
        signedInUserAccountInfo.defaultBot.aadTenantId
        signedInUserAccountInfo.defaultBot.id
        signedInUserAccountInfo.defaultBot.name
      <TO DO - Screenshot>
  f.	Store the above information on your PC - you will need it later.

#### 1. Retrieve topics and utterances from your bot
  a.	Export your bot contents from Common Data Store. [See instructions](https://docs.microsoft.com/en-us/dynamics365/ai/customer-service-virtual-agent/gdpr-export).
  b.  Your content will be exported and downloaded as a zip file (e.g. ExportedFiles_1c5d21e9-1d25-4759-a622-0e232a49e197.zip)
  c.  Unzip the file to find two CSV files - annotations.csv and msdynce_botcontents.csv
  d.	If you have multiple bots use msdynce_botcontents.csv file and retrieve the content version number based on your bot id retrieved from step 1.
  
#### 1. Convert the exported content to LU format
  a.  Compile this utility from 


### 1. Convert virtual agent topics & utterances into LU-down format

### Train dispatcher custom model with your virtual agent's topics

### Deploy dispatcher with custom model

### Test dispatcher working seamlessly with your bots
