---
author: kfrankc-ms
description: Learn how to install LP cameras to use with Dynamics 365 Connected Spaces Preview
ms.author: alwinv
ms.date: 11/02/2021
ms.topic: article
title: Install a camera to use with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Install a camera to use with Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

This article describes how to install and configure a Loss Prevention (LP) camera to use with Microsoft Dynamics 365 Connected Spaces Preview.

## Supported cameras

Dynamics 365 Connected Spaces supports the following LP cameras:

- Axis:

   - M3045-V (must have 9.60.1 or later firmware)
   
   - M3065-V
   
   - M5065 
   
   - P3224-V Mk II
   
   - P3225-V Mk II
   
   - M3047-P
   
## Install a camera	

Use the steps below in addition to your local standards and requirements for installing ethernet.

> [!NOTE]
> If you’re using Axis cameras, create your ONVIF user profile before installing the cameras.

1. Review the [camera placement checklist](camera-placement-checklist.md) to plan your installation.

2. To make camera installation easier, use tape to mark the camera locations on the floor.

3. Install the CAT5e/CAT6 Ethernet cabling. Route the cable from the server/switch location to the planned camera placement location.

    > [!NOTE] 
    > It's a good idea to leave a service loop of about 10 extra feet to enable camera movement, as necessary.
    
4.	Remove the camera from the packaging.

5.	Pre-configure the camera by setting up a temporary PoE switch, connecting your laptop to the switch, and then connecting the camera to the switch through an ethernet cable.

6.	Change the default username/password as instructed by the camera manufacturer documentation, to align with your corporate security guidelines.

    > [!NOTE] 
    > Make sure to set the date/time correctly, according to your local time zone.
  
7.	Mount the camera to the ceiling or drop structure (pole or truss structure used to lower the camera height) as outlined in the [camera height, angle, and focal-point recommendations](camera-placement-recommendations.md) article.

    > [!NOTE] 
    > For camera mounting, we recommend focusing the lens 0-degree position toward your point of interest when mounted (not the 180-degree position).
   
    ![O-degree camera position.](media/orientation-0.PNG "0-degree camera position")
 
    If installed at 180 degrees, or moved later, ensure the ONVIF profile settings correspond to the camera lens position. 
   
    ![180-degree camera position.](media/orientation-180.PNG "180-degree camera position")
 
    > [!NOTE]  
    > If the camera is positioned at 180 degrees, the ONVIF media profile should also specify 180.
   
    ![ONVIF media profile.](media/ONVIF.PNG "ONVIF media profile")
 
When you’re finished mounting and installing the camera per the manufacturer’s documentation, and if you have already installed Azure Stack Edge Pro (2 GPU) and connected it to the network, you’re ready to [add a store with the mobile app, and then pair a gateway to the store](mobile-app-create-store.md).

> [!IMPORTANT]
> The Connected Spaces mobile app is no longer available for download. Go to [Dynamics 365 Connected Spaces](https://dynamics.microsoft.com/en-us/ai/connected-store/) for the latest product news and updates.
