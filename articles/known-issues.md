---
author: kfrankc-ms
description: Learn about known issues related to Dynamics 365 Connected Store
ms.author: frch
ms.date: 09/01/2020
ms.service: crm-online
ms.topic: article
title: Known issues with Dynamics 365 Connected Store
ms.reviewer: v-brycho
---

# Known Issues with Dynamics 365 Connected Store

## Can’t delete stores, gateways, cameras, or skills in mobile app

At this time, stores, gateways, cameras, and skills can’t be deleted in the mobile app. 

## Activating Azure Stack Edge within 24 hours of generating the activation key

After receiving your activation key, you have 24 hours to use the key. If you try to use an activation key after the 24 hours has passed, Azure Stack Edge will be activated but will not be paired to the store in the mobile app. 

To work around this issue, generate the activation key again to unblock the store/gateway pairing.

>[!NOTE]
<Re-generating the activation key will create a duplicate gateway with the same name. 

## Once a gateway is activated and assigned to a store, the store information can’t be changed

Store details can’t be updated or edited after the store is connected to a gateway.

## A gateway can’t support more than 10 zones

Adding more than 10 zones to a gateway can cause performance degradation because of the concurrent number of people being tracked, which exceeds the performance threshold of 
Azure Stack Edge.  

## To rename a camera in the mobile app, you must re-enter your ONVIF camera profile credentials

After you add a camera, if you change the camera name without entering a username and password, the new name will be saved, but the camera will be disconnected. Make sure to 
enter your user name and password when renaming a camera. 

## Camera shows “Disconnected” status for all camera issues, including credentials, network connection, timing, or missing profile

When sign-in fails for any reason, the camera will show “Disconnected” status. [Make sure that cameras are set up correctly](install-cameras.md). 

## The sign-up form doesn’t accept phone numbers with the “+” prefix

When completing the sign-up form for a new Azure Active Directory account, the form will not accept a business phone number with a “+” prefix, such as: **+44 1234 123456**. To 
work around this issue, enter the number without the "+” prefix. For example: **44 1234 123456**

![Phone number field](media/known-issues-phone-prefix.PNG "Phone number field")
 
## Selecting the “Users” link in the order receipt page returns an error

When you sign up for Connected Store using an existing Azure Active Directory tenant admin account, the order receipt page includes a “Users” link that doesn’t work. 

![User's link](media/known-issues-users-link.PNG "User's link")
 
To work around this, select **Continue**, and then [Install Connected Store](admin-install-web-app.md).

## Changing the Environment URL for your Power Platform environment breaks the flow of data from Connected Store

If you change the **Environment URL** for your Power Platform environment (for example, to make the URL easier to remember), you’ll break the connection to Connected Store. The original URL will expire after 24 hours, which 
will cause the mobile app to fail to connect. It will also prevent new data from appearing in the Connected Store web app reports. 

If this happens, sign in to the [Connected Store Setup page](https://ppe.connectedstore.dynamics.com/) to trigger a connection refresh. The Connected Store service will 
start using the new URL within an hour.

![Environment url](media/known-issues-environmental-url.PNG "Environment url")
