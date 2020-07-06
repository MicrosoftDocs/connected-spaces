---
author: kfrankc-ms
description: Learn how to prepare your network and install Azure Stack Edge to use with Dynamics 365 Connected Store (public preview)
ms.author: frch
ms.date: 07/01/2020
ms.service: crm-online
ms.topic: article
title: Prepare your network and install Azure Stack Edge to use with Dynamics 365 Connected Store (public preview)
ms.reviewer: v-brycho
--- 

# Prepare your network and install Azure Stack Edge to use with Dynamics 365 Connected Store (public preview)

This article covers the steps to prepare and install Azure Stack Edge for use with Microsoft Dynamics 365 Connected Store (public preview). 

> [!IMPORTANT]
> The Azure Stack Edge gateway that you order for Connected Store (public preview) can only be used for Connected Store (public preview). You can't deploy any other resources to Azure Stack Edge during the public preview. 

## Azure Stack Edge installation requirements	

The following table shows the requirements for installing and connecting the Azure Stack Edge hardware for Dynamics 365 Connected Store.

|Requirement|Description|
|----------------|--------------------------------------------------------------------------------------------|
|Size|To mount Azure Stack Edge, you need a 1U slot in a standard 19” datacenter rack.<br><br>Device dimensions: 1.75" (height) x 17.09" (width) x 29.15" (length)|
|Airflow|Azure Stack Edge requires adequate ventilation for cooling. The system airflow is front to rear, so make sure that there are no obstructions to air flow from front to back.<br><br>The system must be operated with a low-pressure, rear-exhaust installation.|
|Power|Azure Stack Edge requires an independent source or a rack power distribution unit (PDU) with an uninterruptible power supply (UPS). The AC power source needs to have the capacity to supply the 750 Watt maximum power draw of the Azure Stack Edge. [Learn more about power requirements](https://docs.microsoft.com/azure/databox-online/azure-stack-edge-technical-specifications-compliance#power-supply-unit-specifications).|
|Noise|Azure Stack Edge uses fan cooling which results in noticeable fan noise. Do not mount or install Azure Stack Edge where people perform daily operations which may be affected by prolonged noise exposure.|
|Network|Azure Stack Edge requires a standard 20 MB internet connection for data flow to the Dynamics 365 Connected Store services and application. Azure Stack Edge and cameras must be on the same local area network (LAN). A Power Over Ethernet (PoE) switch is also required for the IP cameras to connect Azure Stack Edge to the LAN.|
|Operating temperatures|See the [Azure Stack Edge technical specifications](https://docs.microsoft.com/azure/databox-online/azure-stack-edge-technical-specifications-compliance) for detailed operating and power requirements.|

## Site preparation	
This section covers what you need to know to prepare your site for Azure Stack Edge installation and configuration.

### Prepare your LAN information

You’ll need the following LAN information when you configure Azure Stack Edge:

- Local Area Network IP

- Subnet mask

- Gateway

- DNS:

   - Primary DNS

   - Secondary DNS

> [!NOTE]
> When configuring your network, make sure that Azure Stack Edge and cameras are all on the same subnet. At this time, Azure Stack Edge does not support dual-homed networks.

### Secure the IP addresses

You'll need to secure a range of static IP addresses for your edge hardware (cameras and gateway). 

- The IP cameras require a range of 10 IP addresses. To enable future camera expansion, we recommend securing additional IP addresses. If possible, assign these static IP addresses in sequence for ease of troubleshooting. 

- Azure Stack Edge requires 3 static IP addresses initially. If possible, assign these static IP addresses in sequence for ease of troubleshooting. 

### Check power and ventilation 

Make sure the site meets the power and ventilation requirements outlined in the requirements section of this article. 

### Check server rack accessibility

Verify that the server rack is accessible and is ready for you to load the Azure Stack Edge device into position.

## Install and connect Azure Stack Edge	

> [!NOTE]
> Download and install the Dynamics 365 Connected Store mobile app before you start.

1. Unpack and install Azure Stack Edge using the following instructions: https://docs.microsoft.com/azure/databox-online/data-box-edge-deploy-install

2. To connect Azure Stack Edge to the network switch:

    a. Install your network PoE switch if it’s not already installed. We recommend installing it in close proximity to Azure Stack Edge.
    
    b. Use the following tutorial to connect Azure Stack Edge to the network switch: https://docs.microsoft.com/azure/databox-online/data-box-edge-deploy-connect-setup-activate
    
    c. As shown in the Azure Stack Edge documentation, connect Azure Stack Edge to PORT 3 if you have an SFP cable, or PORT 2 if you have an RJ45 cable. Connect the other end to the dedicated network switch.
    
    d. Connect the laptop you’re using to configure Azure Stack Edge to PORT 1.
    
    > [!NOTE]
    > Configure the Ethernet adapter on your computer to connect to the Azure Stack Edge device with a static IP address of 192.168.100.5 and subnet 255.255.255.0. In addition, confirm that Azure Stack Edge has connectivity to the NTP server.
    
    e. When your laptop is connected to PORT 1 and your ethernet adapter or port is configured on your laptop, go to the Dynamics 365 Mobile App guide to

      i. [Set up a store](mobile-app-create-store.md).
       
      ii. [Pair a gateway](mobile-app-pair-gateway.md).
       
      iii. [Connect cameras](mobile-app-add-cameras.md).
      
      iv. [Add camera skill zones](mobile-app-add-camera-skill-zones.md)

## Next step

[Connect Azure Stack Edge to your network](ase-connect.md)
