---
author: alwinv
description: Learn about known issues that are related to Microsoft Dynamics 365 Connected Spaces Preview.
ms.author: alwinv
ms.date: 01/11/2022
ms.topic: article
title: Known issues with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Known issues with Microsoft Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

## When I connect a camera and configure a skill, screen items aren't rendering properly

The minimum resolution required for Dynamics 365 Connected Spaces is 1024 x 1366. If you use a device that has a lower resolution (for example, a mobile phone), screen items (scroll bars and buttons, for example) may not render properly. Apple iPad Pros have a screen resolution of 1024 x 1366. 

## My company doesn't allow team members to sign up with a work email address

You may see the following message when you try to sign up for a free trial: "Your company doesn't allow team members to sign up with their work email." 

![Screenshot of Let's get started dialog box showing error message.](media/known-issues-trial-email.jpg "Screenshot of Let's get started dialog box showing error message")

To complete the trial sign-up, you'll need to work with your Azure Active Directory administrator and have them [sign up for the trial](trial-signup.md). 

## I can’t turn the Save video data to the cloud setting to Off because the setting is disabled
 
![Screenshot of Save video data to the cloud setting.](media/known-issues-cloud-storage.jpg "Screenshot of Save video data to the cloud setting")

If the **Save video data to the cloud** setting has been recently changed, it will be disabled for several days until our service has completed the requested change. Wait for a day or two and try again. 

If you're ready to set up your edge gateway and need to change this setting, contact your Connected Spaces representative. We'll process the change directly.

## The Connected Spaces app is running in the wrong geographic region

When using Connected Spaces, make sure you're using the web app in the geographic region that your company's AAD tenant and user accounts are in.

| Your AAD account region | Connected Spaces web app URL |
| --- | --- |
| United States | https://us.ppe.connectedspaces.dynamics.com/ |
| United Kingdom | https://uk.ppe.connectedspaces.dynamics.com/ |

Doing this will ensure that Connected Spaces will be able to process your customer data within your company's geographic region.

## Changing the time zone for a store only affects the data collected after making the change

If the time zone for a store is changed, it does not change the time zone for the data already collected. Future data collected for the store will be recorded using the new time zone.


