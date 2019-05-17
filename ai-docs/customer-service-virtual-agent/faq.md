---
title: "Frequently asked questions"
description: "Frequently asked questions about Dynamics 365 Virtual Agent for Customer Service."
keywords: ""
ms.date: 05/17/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: m-hartmann   
ms.author: mhart
manager: shellyha
---

# Frequently asked questions

## General 

### What are the various Browsers supported by the Virtual Agent?

Virtual Agent is supported in the latest versions of Edge, Chrome, and Fire Fox. It is not supported in Internet Explorer.
 
### Can Virtual Agent be styled and branded for an organization? What can be customized and how?

Currently we don't have any styling or brand customization (e.g. changing the default image) for the bot. But this is on the roadmap for a future release.

### Can multiple team members collaborate on a single bot instance?

We don’t have multi author support currently. It is one bot per author. However, we have this feature on the roadmap for future releases. The current mitigation is to create a service account and share it across the content authors.

### Can I do end user authentication using AAD or MSA from within the bot?

We currently do not support any authentication from within the Virtual Agent. However, native support for end user authentication is on the roadmap.

### Virtual Agent Designer does not seem to allow us to store the user utterance that triggered the topic as a variable, is that by design?

Yes, Virtual Agent currently doesn't allow storing the user utterance that triggered the topic as a variable. This feature is on the roadmap for a future release.

### I ran into a problem. What should I do to file a bug?  How quickly will you get back to me? 

You can file bugs in the in the [community forum](https://go.microsoft.com/fwlink/?linkid=2058639). We will respond within 48 hrs.

### I have a new feature idea or some ideas on how to make a feature work better. How should I submit these ideas to the product team?

That's great, we'd love to hear your thoughts. [Submit your ideas and feedback in our Idea forum](https://go.microsoft.com/fwlink/?linkid=2064961).


## Licensing and environment

### What is the cost involved in using Microsoft Flow Actions in Virtual Agent?

A Flow license is per user. Users get Flow licenses automatically when they get a Bot license (which is based on number of sessions). There may be a limit for how many Bot Author (P2 Flow licenses) you can have based on the bracket of Bot license you purchased. 

Here is how the flow licensing works in the context of the bot license.
If you have 10 bot authors in your organization:
 - each of them gets a P2 Flow license
 - every P2 license comes with 15K Flow "runs" per month
Flow runs are "pooled" and the runs are anonymous - so the org actually gets 10x15K Flow runs any Flow can use. Now, this 10x15K is a big number to have for a month, and they can be used by any Flow anyone has created.
The "1 min execution throttle" only applies to "auto-run" type of Flows and does not apply to Bot Flows. This throttle is only for the Flows that are set up to run automatically in a loop, like "every 1 min, check if there are new emails in my Inbox".

### The Power Apps environment I created does not show up in the down menu of Virtual Agent, why?

Please check if you selected the Region as "USA" while creating the Power Apps (Common Data Service) environment. Currently we support only environments in USA. If you created an environment in other regions, it won't be shown in Virtual Agent. The workaround is to create a new environment with Location as "USA" or use an existing environment that was created in "USA" region.


## Topic creation and management  

## Flow integration 

## Deployment 

## Analytics 