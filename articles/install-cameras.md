
# Install cameras to use with Dynamics 365 Connected Store

This document provides an overview of the process to install and configure your IP cameras to support Dynamics 365 Connected Store.

## Supported cameras

Dynamics 365 Connected Store supports the following IP cameras:

- Axis:
   - M3045V*
   - M5055 PTZ
   - M5065 PTZ
- Bosch:
   - NUC-51022-F2
- Lorex**:
   - LNZ32P4B

* Make sure that Axis M3045V cameras have the 9.60.1 or later firmware.

** Lorex cameras are currently banned by the US government. We don’t recommended using these cameras unless they have already been installed in your environment.

## Camera installation 	

Use the steps below in addition to your local standards and requirements for installing ethernet.

> [!NOTE]Note
> If you’re using Axis cameras, create your ONVIF user profile if you haven’t already done so before installing the cameras.

1. Review the Camera Placement guide to plan your installation, if you haven’t already done so.

2. To make camera installation easier, use tape to mark the camera locations on the floor.

3. Install CAT5e/CAT6 Ethernet cabling. Route the cable from the server/switch location to the planned camera placement location.

    > [!NOTE] 
    > Leave a service loop of ~10 feet extra to enable movement of the camera, as necessary.
    
4.	Remove the camera from the packaging.

5.	Pre-configure the cameras by setting up a temporary PoE switch, connecting your laptop to the switch, and then connecting the camera to the switch through an ethernet cable.

6.	Change the default username/password as instructed by the camera manufacturer documentation, to align with your corporate security guidelines.

   > [!NOTE] 
   > Make sure to set the date/time correctly according to your local time zone.
  
7.	Mount the cameras to the ceiling or drop structure as outlined in the Camera Placement guide.

   > [!NOTE] 
   > For camera mounting, we recommend focusing the lens 0-degree position toward your point of interest when mounted (not the 180-degree position).
 
   If installed at 180 degrees, or moved later, ensure the ONVIF profile settings correspond to the camera lens position. 
 
   > [!NOTE]  
   > If the camera is positioned at 180 degrees, the media profile should specify 180.
 
When you’ve finished mounting and setting up the cameras per the manufacturer’s documentation, you’re ready to install and configure Azure Stack Edge using the Azure Stack Edge Installation guide.

## What's next?

[Install Azure Stack Edge](ase-install.md)

