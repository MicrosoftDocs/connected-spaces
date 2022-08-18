---
author: kfrankc-ms
description: Learn how to prepare your network and install Azure Stack Edge Pro (2 GPU) to use with Dynamics 365 Connected Spaces Preview.
ms.author: rapraj
ms.date: 08/18/2022
ms.topic: article
title: Prepare your network and install Azure Stack Edge Pro (2 GPU) to use with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
--- 

# Prepare your network and install Azure Stack Edge Pro (2 GPU) to use with Dynamics 365 Connected Spaces Preview

After you receive your Azure Stack Edge Pro (2 GPU) gateway for Microsoft Dynamics 365 Connected Spaces Preview, you'll need to prepare your network and install the device. 

> [!IMPORTANT]
> This document provides helpful guidelines, but it is your responsibility to ensure that you are properly securing and maintaining the equipment and infrastructure located on your premises, including Azure Stack Edge Pro, your cameras, network, and video feeds from your cameras.

## Azure Stack Edge Pro installation requirements	

> [!NOTE]
> The Azure Stack Edge Pro gateway that you order for Connected Spaces Preview can only be used for Connected Spaces Preview. You can't deploy any other resources to Azure Stack Edge Pro during the preview. 

The following table shows tips for installing and connecting the Azure Stack Edge Pro gateway for Dynamics 365 Connected Spaces.

|Requirement|Description|
|----------------|--------------------------------------------------------------------------------------------|
|Size|To mount Azure Stack Edge Pro, you need a 1U slot in a standard 19" datacenter rack.<br><br>Device dimensions: 1.75" (height) x 17.09" (width) x 29.15" (length)|
|Airflow|Azure Stack Edge Pro requires adequate ventilation for cooling. The system airflow is front to rear, so make sure that there are no obstructions to air flow from front to back.<br><br>The system must be operated with a low-pressure, rear-exhaust installation.|
|Power|Azure Stack Edge Pro requires an independent source or a rack power distribution unit (PDU) with an uninterruptible power supply (UPS). The AC power source needs to have the capacity to supply the 750-watt maximum power draw of Azure Stack Edge Pro. [Learn more about power requirements](/azure/databox-online/azure-stack-edge-technical-specifications-compliance#power-supply-unit-specifications).|
|Noise|Azure Stack Edge Pro uses fan cooling which results in noticeable fan noise. Do not mount or install Azure Stack Edge Pro where people perform daily operations which may be affected by prolonged noise exposure.|
|Network|Azure Stack Edge Pro requires a 5-megabits-per-second internet connection for data flow to the Dynamics 365 Connected Spaces services and application. Azure Stack Edge Pro and cameras must be on the same local area network (LAN). See also [Adding URLs to allow lists for firewalls](ase-install.md#adding-urls-to-allow-lists-for-firewalls) below.<br><br>If this port can't be opened because of firewall policies, use AMQP over web sockets (port 443).|
|Operating temperatures|See the [Azure Stack Edge Pro technical specifications](/azure/databox-online/azure-stack-edge-technical-specifications-compliance) for detailed operating and power requirements.|

## Adding URLs to allow lists for firewalls

In addition to using [URL patterns for firewall rules](/azure/databox-online/azure-stack-edge-system-requirements#url-patterns-for-gateway-feature), customers that have a firewall that has allow lists of fully qualified domain names (FQDNs) will have to add the following URLs to use Connected Spaces.

|URL|Description|
|----------------------------------------------|-----------------------------------------------|
|'https://*.monitoring.azure.com'|Required so that Connected Spaces can receive telemetry information about the health of the Azure Stack Edge Pro device|
|'https://*.cognitiveservices.azure.com/'|Needed to use computer vision APIs|
|'https://csppe*.azurewebsites.net'|Provides access to the Connected Spaces reality services|
|'https://csprod*azurewebsites.net'|Provides access to the Connected Spaces reality services|
|'https://dev.azure.com/proddynamicscrm'|Provides access to the Git-Ops repository|
|'https://pkgs.dev/azure.com/dynamicscrm'|Provides access to the Kubernetes cluster endpoints|

See also these links for other URLs to add to the allowed list:

- [URL patterns for gateway feature](/azure/databox-online/azure-stack-edge-gpu-system-requirements#url-patterns-for-gateway-feature)
- [URL patterns for compute feature](/azure/databox-online/azure-stack-edge-gpu-system-requirements#url-patterns-for-compute-feature)

## Site preparation	
This section covers what you need to know to prepare your site for Azure Stack Edge Pro installation and configuration.

### Prepare your LAN information

You'll need the following LAN information when you configure Azure Stack Edge Pro:

- Local Area Network IP

- Subnet mask

- Gateway

- DNS:

   - Primary DNS

   - Secondary DNS

> [!NOTE]
> When configuring your network, make sure that Azure Stack Edge Pro and cameras are all on the same subnet. At this time, Azure Stack Edge Pro does not support dual-homed networks.

### Secure the IP addresses

You'll need to secure a range of static IP addresses for your edge hardware (cameras and gateway). 

- The IP cameras require a range of 10 IP addresses. To enable future camera expansion, we recommend securing additional IP addresses. If possible, assign these static IP addresses in sequence to make troubleshooting easier. 

- Azure Stack Edge Pro requires 4 static IP addresses initially. If possible, assign these static IP addresses in sequence to make troubleshooting easier. 

### Check power and ventilation 

Make sure the site meets the power and ventilation requirements outlined in the requirements section of this article. 

### Check server rack accessibility

Verify that the server rack is accessible and is ready for you to load the Azure Stack Edge Pro device into position.

## Install and connect Azure Stack Edge Pro	

> [NOTE] 
> The steps in this section will be completed by your Microsoft Solution Implementation partner. Contact your partner directly. 

Use the following tutorials to install and connect Azure Stack Edge Pro:

1. [Tutorial: Install Azure Stack Edge Pro with GPU](/azure/databox-online/azure-stack-edge-gpu-deploy-install)

    > [!IMPORTANT]
    > In the **Prerequisites** section of this tutorial, skip the **For the Azure Stack Edge resource** subsection since the device will be activated in a different way, as described below.

2. [Tutorial: Connect to Azure Stack Edge Pro with GPU](/azure/databox-online/azure-stack-edge-gpu-deploy-connect)

3. [Tutorial: Configure network for Azure Stack Edge Pro with GPU](/azure/databox-online/azure-stack-edge-gpu-deploy-configure-network-compute-web-proxy)

   > [!IMPORTANT]
   > Stop after the **Configure network** section of this tutorial. **DO NOT COMPLETE THE ENABLE COMPUTE NETWORK SECTION.**
    
## Next step

- [Connect your Azure Stack Edge Pro device to the network](ase-connect.md)
