---
title: "Frequently asked questions for Market Insights | Microsoft Docs"
description: "Find answers to frequently asked questions about Market Insights."
keywords: "FAQ, questions, common issues, quota, search setup, search topics"
ms.date: 04/01/2019
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 30351228-2274-4998-933f-6a3fa6453274
author: m-hartmann
ms.author: mhart
ms.custom: dyn365-ai-marketinsights
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# [!INCLUDE[Dynamics 365 Market Insights](../includes/pn-market-insights-long.md)] FAQ

(This topic is pre-release documentation and is subject to change.)

Are you new to [!INCLUDE[Dynamics 365 Market Insights](../includes/pn-market-insights-long.md)] or looking for some help? We've compiled a list of frequently asked questions and provided brief answers to help you get to your information quickly.  

## I did not receive an alert email. What happened?

- After you [create an alert](alerts-management.md#create-an-alert), you will receive your first alert the next morning. We are working on sending you a confirmation email right away (coming soon).
- We don't send an email when there isn't something important enough to alert you about. 
- Please [sign in](alerts-management.md#sign-in-to-the-app) to your account to verify if you had created an alert.

## The news articles in the email don't seem relevant to my topic. What's going on?

Making sure the [email content is relevant to you](alerts-data-science.md) is our top priority. Please send us feedback if you have this issue. You can select the **Flag as irrelevant** link in the email to make this process most efficient.

## The preview I am seeing doesn't seem that relevant. Why?

There's a lot of AI that goes into curating the best content for you. In order to show you a preview immediately, we only do some of it - so rest assured that in most cases what you get in your email will be better than what you see in the preview. The preview is there to help you refine your topic. In the coming months, we will improve the preview significantly.

## How do I setup a topic with more than just a phrase?

Please use the **Show advanced** functionality to [refine your topic](alerts-management.md#tips-on-refining-your-topic). 

## Which open source components are used?

   - "@babel/core": "7.1.0",
    - "@babel/polyfill": "^7.0.0",
    - "@skype/ecsclient": "^2.0.7",
    - "@svgr/webpack": "2.4.1",
    - "@types/dateformat": "^3.0.0",
    - "@types/enzyme": "^3.1.16",
    - "@types/react-test-renderer": "^16.0.3",
    - "@types/redux-saga-routines": "2.1.0",
    - "@uifabric/fluent-theme": "0.3.0",
    - "applicationinsights-js": "1.0.20",
    - "axios": "0.18.0",
    - "babel-core": "7.0.0-bridge.0",
    - "babel-eslint": "9.0.0",
    - "babel-jest": "^24.0.0",
    - "babel-loader": "8.0.4",
    - "babel-plugin-named-asset-import": "0.2.0",
    - "babel-preset-react-app": "5.0.0",
    - "bfj": "6.1.1",
    - "case-sensitive-paths-webpack-plugin": "2.1.2",
    - "chalk": "2.4.1",
    - "classnames": "2.2.6",
    - "connected-react-router": "4.5.0",
    - "css-loader": "1.0.0",
    - "dateformat": "^3.0.3",
    - "dotenv": "6.0.0",
    - "dotenv-expand": "4.2.0",
    - "eslint": "5.6.0",
    - "eslint-config-react-app": "3.0.0",
    - "eslint-loader": "2.1.1",
    - "eslint-plugin-flowtype": "2.50.1",
    - "eslint-plugin-import": "2.14.0",
    - "eslint-plugin-jsx-a11y": "6.1.1",
    - "eslint-plugin-react": "7.11.1",
    - "file-loader": "2.0.0",
    - "flag": "3.0.0-1",
    - "fork-ts-checker-webpack-plugin": "0.4.9",
    - "fs-extra": "7.0.0",
    - "history": "4.7.2",
    - "html-webpack-plugin": "4.0.0-alpha.2",
    - "http-status-codes": "1.3.0",
    - "identity-obj-proxy": "3.0.0",
    - "jwt-decode": "2.2.0",
    - "lodash": "4.17.11",
    - "mini-css-extract-plugin": "0.4.3",
    - "msal": "0.2.4",
    - "node-sass": "4.10.0",
    - "office-ui-fabric-react": "6.100.0",
    - "optimize-css-assets-webpack-plugin": "5.0.1",
    - "postcss-flexbugs-fixes": "4.1.0",
    - "postcss-loader": "3.0.0",
    - "postcss-preset-env": "6.0.6",
    - "postcss-safe-parser": "4.0.1",
    - "query-string": "6.2.0",
    - "react": "16.6.0",
    - "react-app-polyfill": "0.1.3",
    - "react-dev-utils": "6.0.1",
    - "react-dom": "16.6.0",
    - "react-redux": "5.1.0",
    - "react-router": "4.3.1",
    - "react-router-dom": "4.3.1",
    - "react-test-renderer": "^16.8.4",
    - "redux": "4.0.1",
    - "redux-actions": "2.6.4",
    - "redux-persist": "5.10.0",
    - "redux-saga": "0.16.2",
    - "redux-saga-routines": "3.1.3",
    - "redux-thunk": "2.3.0",
    - "resolve": "1.8.1",
    - "sass-loader": "7.1.0",
    - "simplerestclients": "^0.2.6",
    - "source-map-loader": "0.2.1",
    - "style-loader": "0.23.0",
    - "synctasks": "^0.3.3",
    - "terser-webpack-plugin": "1.1.0",
    - "thread-loader": "1.2.0",
    - "ts-jest": "^24.0.0",
    - "ts-loader": "4.x.x",
    - "tsconfig-paths-webpack-plugin": "2.0.0",
    - "tslint": "5.12.0",
    - "tslint-config-prettier": "1.10.0",
    - "tslint-react": "3.2.0",
    - "url-loader": "1.1.1",
    - "webpack": "4.19.1",
    - "webpack-manifest-plugin": "2.0.4",
    - "workbox-webpack-plugin": "3.6.1"

  
### See also

[Market Insights alerts - track topics that matter to you](alerts-overview.md)    
[How relevancy is determined in alerts](alerts-data-science.md)    
[Data handling for Dynamics 365 Market Insights alerts](alerts-data-handling.md)
 
