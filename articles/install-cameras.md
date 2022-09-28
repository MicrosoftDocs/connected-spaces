---
author: kfrankc-ms
description: Learn how to install LP cameras to use with Dynamics 365 Connected Spaces Preview
ms.author: rapraj
ms.date: 09/30/2022
ms.topic: article
title: Install a camera to use with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Install cameras to use with Dynamics 365 Connected Spaces Preview

This article describes how to install and configure cameras to use with Microsoft Dynamics 365 Connected Spaces Preview.

## Supported cameras

Connected Spaces Preview supports standard IP cameras that:

- Can provide a Real-Time Streaming Protocol (RTSP) stream 

- Use the H.264 or M-JPEG codec standard

> [!NOTE]
> If you're using a fisheye or panoramic-type camera, the camera must have on-camera dewarping capabilities.

Connected Spaces Preview supports a variety of cameras, including Axis, Bosch, and Sony. Validated camera models include Axis M5075 PTZ, Axis M3065-V, Axis M5065, Axis P3324-V Mk II, and Axis P3325-V Mk II. Most Connected Spaces Preview customers are able to use their existing security cameras. To get the best analytics results, follow the guidelines in [Camera placement suggestions](camera-placement-recommendations.md).
   
## Install a camera	

Use the steps below in addition to your local standards and requirements for installing Ethernet.

> [!NOTE]
> If you’re using Axis cameras, create your ONVIF user profile before installing the cameras.

1. Review the [camera placement checklist](camera-placement-checklist.md) to plan your installation.

2. To make camera installation easier, use tape to mark the camera locations on the floor.

3. Install the CAT5e/CAT6 Ethernet cabling. Route the cable from the server/switch location to the planned camera placement location.

    > [!NOTE] 
    > It's a good idea to leave a service loop of about 10 extra feet to enable camera movement, as necessary.
    
4.	Remove the camera from the packaging.

5.	Pre-configure the camera by setting up a temporary PoE switch, connect your laptop to the switch, and then connect the camera to the switch through an Ethernet cable.

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
 
When you’re finished mounting and installing the camera per the manufacturer’s documentation, and if you have already installed Azure Stack Edge Pro (2 GPU) and connected it to the network, you’re ready to add a store.
