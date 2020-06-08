
# Prepare your network and install Azure Stack Edge to use with Dynamics 365 Connected Store

This article covers the steps to prepare and install Azure Stack Edge for use with Dynamics 365 Connected Store. After installing Azure Stack Edge using these instructions, you'll use the Dynamics 365 Connected Store mobile app to create a store and pair a gateway.

## Azure Stack Edge installation requirements	

The following table shows the requirements for installing and connecting the Azure Stack Edge hardware for Dynamics 365 Connected Store.

|Requirement|Description|
|----------------|--------------------------------------------------------------------------------------------|
|Size|To mount Azure Stack Edge, you need a U1 slot in a standard 19” datacenter rack.<br><br>Device dimensions: 1.75" (height) x 17.09" (width) x 29.15" (length)|
|Airflow|Azure Stack Edge requires adequate ventilation for cooling. The system airflow is front to rear, so make sure that there are no obstructions to air flow from front to back.<br><br>The system must be operated with a low-pressure, rear-exhaust installation.|
|Power|You’ll need standard AC power from an independent source or a rack power distribution unit (PDU) with an uninterruptible power supply (UPS).|
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

We recommend that you secure a range of static IP addresses on the same network for your edge hardware (cameras and gateway). A range of 100 IP addresses will provide room to add more cameras as your needs grow.

- The IP cameras require a range of 50 IP addresses. Keep these in sequence, if possible, for ease of troubleshooting.

- Azure Stack Edge requires a range of 25 IP addresses. Initially, you might only need 3, but for future upgrades, additional addresses may be required.

- To enable future expansion, such as additional cameras, we recommend securing an additional range of 25 IP addresses.

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
    > You must configure your ethernet adapter to have a static IP address on the same network as the Azure Stack Edge local network. The Azure Stack Edge local IP address is 192.168.100.10 so configure your ethernet adapter static IP address to be on the same network as the Azure Stack Edge by using the 192.168.100.9 IP address. In addition, confirm that the ASE has connectivity with the NTP server.
    
    e. When your laptop is connected to PORT 1 and your ethernet adapter or port is configured on your laptop, go to the Dynamics 365 Mobile App guide to set up a store, pair a gateway, and add cameras and camera skill zones.

## What's next?

[Create a store on the mobile app](create-store.md)
