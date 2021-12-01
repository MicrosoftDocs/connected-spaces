---
author: alwinv
description: Learn about known issues that are related to Microsoft Dynamics 365 Connected Spaces Preview.
ms.author: alwinv
ms.date: 12/02/2021
ms.topic: article
title: Known issues with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Known issues with Microsoft Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

## The Connected Spaces app is running in the wrong geographic region

When using Connected Spaces, make sure you're using the web app in the geographic region that your company's AAD tenant and user accounts are in:

| Your AAD account region | Connected Spaces web app URL |
| --- | --- |
| United States | https://cspperegionalwestus.azurewebsites.net/ |
| United Kingdom | https://cspperegionaluksouth.azurewebsites.net/ |

Doing this will ensure that Connected Spaces will be able to process your customer data within your company's geographic region.

## I'm prompted to accept permissions multiple times when I start up the Connected Spaces web app

When signing in to Connected Spaces web app for the first time, this prompt might appear more than once:

![Screenshot of Permissions requested dialog box.](media/setup-permissions-requested.jpg "Screenshot of Permissions requested dialog box")

If this happens, wait a few minutes for the permissions to be applied and then try to sign in again.

## Changing the time zone for a store only affects the data collected after making the change

If the time zone for a store is changed, it does not change the time zone for the data already collected. Future data collected for the store will be recorded using the new time zone.


