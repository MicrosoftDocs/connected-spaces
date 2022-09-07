---
author: alwinv
description: Learn about known issues that are related to Microsoft Dynamics 365 Connected Spaces Preview.
ms.author: alwinv
ms.date: 09/27/2022
ms.topic: article
title: Known issues with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Known issues with Microsoft Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

## Site can crash on Settings page if viewing Connected Spaces in a non-English or non-German language

If your browser is set to a non-English or non-German language, and you go to the Settings page, Dynamics 365 Connected Spaces Preview may experience an error. To work around this known issue, update your brower's language setting to English or German. 

![Screenshot of Edge browser language setting.](media/known-issues-language-setting-edge-browser.JPG "Screenshot of Edge browser language setting")

## When I connect a camera and configure a skill, screen items aren't rendering properly

The minimum resolution required for Dynamics 365 Connected Spaces Preview is 1024 x 1366. If you use a device that has a lower resolution (for example, a mobile phone), screen items (scroll bars and buttons, for example) may not render properly. Apple iPad Pro devices have a screen resolution of 1024 x 1366. 

## My company doesn't allow team members to sign up with a work email address

You may see the following message when you try to sign up for a free trial: "Your company doesn't allow team members to sign up with their work email." 

![Screenshot of Let's get started dialog box showing error message.](media/known-issues-trial-email.jpg "Screenshot of Let's get started dialog box showing error message")

To complete the trial sign-up, [your Azure Active Directory administrator can assign you a special license so you can sign up for the trial](trial-signup-admin.md). 

## The Connected Spaces app is running in the wrong geographic region

When using Connected Spaces, make sure you're using the web app in the geographic region that your company's AAD tenant and user accounts are in.

| Your AAD account region | Connected Spaces web app URL |
| --- | --- |
| United States | https://us.connectedspaces.dynamics.com/ |
| United Kingdom | https://uk.connectedspaces.dynamics.com/ |

Doing this will ensure that Connected Spaces will be able to process your customer data within your company's geographic region.

## Changing the time zone for a store only affects the data collected after making the change

If the time zone for a store is changed, it does not change the time zone for the data already collected. Future data collected for the store will be recorded using the new time zone.


