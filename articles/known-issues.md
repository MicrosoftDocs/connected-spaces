---
author: alwinv
description: Learn about known issues that are related to Microsoft Dynamics 365 Connected Spaces Preview.
ms.author: alwinv
ms.date: 12/14/2021
ms.topic: article
title: Known issues with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Known issues with Microsoft Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

## I can’t turn the Save video data to the cloud setting to Off because the setting is disabled
 
![Screenshot of Save video data to the cloud setting.](media/known-issues-cloud-storage.jpg "Screenshot of Save video data to the cloud setting")

If the **Save video data to the cloud** setting has been recently changed, it will be disabled for several days until our service has completed the requested change. Wait for a day or two and try again. 

If you are already working with our team to set up your first edge gateway, let us team know and we can process the requested setting change.

## The Connected Spaces app is running in the wrong geographic region

When using Connected Spaces, make sure you're using the web app in the geographic region that your company's AAD tenant and user accounts are in.

| Your AAD account region | Connected Spaces web app URL |
| --- | --- |
| United States | https://us.ppe.connectedspaces.dynamics.com/ |
| United Kingdom | https://uk.ppe.connectedspaces.dynamics.com/ |

Doing this will ensure that Connected Spaces will be able to process your customer data within your company's geographic region.

## Changing the time zone for a store only affects the data collected after making the change

If the time zone for a store is changed, it does not change the time zone for the data already collected. Future data collected for the store will be recorded using the new time zone.


