---
author: kfrankc-ms
description: Learn how to connect Azure Stack Edge to your network to use with Dynamics 365 Connected Spaces Preview
ms.author: rapraj
ms.date: 05/24/2022
ms.topic: article
title: Activate Azure Stack Edge Pro (2 GPU) for use with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Activate Azure Stack Edge Pro (2 GPU) for use with Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

After you've [installed Azure Stack Edge Pro (2 GPU)](ase-install.md), you're ready to connect it to your network and configure the network for use with Microsoft Dynamics 365 Connected Spaces Preview. If you're working with a system integrator to install the hardware and set up the network, you might want to contact them for support with this step. 

> [!NOTE]
> Contact your Connected Spaces Implementation Partner to add your Azure subscription ID to the Preview list.

## Create a service principle

1. Follow [the Windows Remote Management instructions](/windows/win32/winrm/installation-and-configuration-for-windows-remote-management#quick-default-configuration) to verify that Windows Remote Management is installed and configured in your environment.

2. Create a [service principal](https://docs.microsoft.com/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object) in Azure Active Directory to use with Connected Spaces. To do this:

    1. In the Azure Portal, select **Azure Active Directory**.

        SCREENSHOT GOES HERE
        
    2. Select **App registrations** on the left side of the screen, and then select **New registration**. 

        SCREENSHOT GOES HERE
        
    3. In the **Register an application** screen, enter a name for the application, and then under **Supported account types**, select the **Accounts in this organizational directory only (Microsoft only - Single tenant)** option. 

        SCREENSHOT GOES HERE

        > [!NOTE]
        > You can reuse the same service principal for multiple Azure Stack Edge devices. 

## Add a gateway device

1. In the Connected Spaces web app, select the **Devices** tab, and then select **Add gateway**. 

    SCREENSHOT GOES HERE

2. In the **Add device** screen, select **Next**.

    SCREENSHOT GOES HERE

3. Use the information in the following table to fill in the information in the **Add device details** screen. 
 
    |Field|Description|
    |------------------------------------------|-----------------------------------------------------------------------------------|
    |Azure Tenant ID|The ID of the directory/tenant for the Azure Account being used|  
    |Subscription ID|The ID of the Azure subscription to install Managed App| 
    |Resource Group Name|The name of the resource group to install Managed App| 
    |Device IP|The local IP address of the Azure Stack Edge device (for example: 192.168.1.100)| 
    |Device Serial Number|The serial number for the device (listed on the side of the physical device) or the local UI on the device (accessible by using the IP address for the device).| 
    |Compute Node|The device interface number to install the compute node to, which should match the port number used to connect to the network (for example: 2)|
    |Kubernetes Node IP Range Start|The first IP address of two contiguous open IP addresses on the same network as the Azure Stack Edge device| 
    |Kubernetes Node IP Range End|The second and last IP address of two contiguous open IP addresses on the same network as the Azure Stack Edge device| 
    |Kubernetes Service IP|A range of open IP addresses on the same network that kubernetes can use for service endpoints. This can be a range of 1 single IP address (for example: 192.168.1.104-192.168.1.104)| 
    |Location|The location to create resources in (for example: eastus)| 
    |Service Principal Application ID|Application ID of the enterprise app from the [service principal step](#create-a-service-principle)| 
    |Service Principal Object ID|Object ID of the enterprise app from the [service principal step](#create-a-service-principle)| 

    When you're done fill in the fields, select **Next**.

    SCREENSHOT GOES HERE

4. If all the conditions for the values are met, you'll see a message that says that "Connected Spaces is generating your Azure Stack Edge installation script." This script is specific for the network and device.

    SCREENSHOT GOES HERE

5.  After the script is generated, you'll see a message that says **Azure Stack Edgge script generated**. Select **Download script** to download and store it on a device that has access to the Azure Stack Edge device, either through remote access by being on the same network as the device or through a physical connection using an ethernet cable to the Azure Stack Edge device. The Azure Stack Edge activation script will be namee "AzureGatewayAcivationScript.ps1".

    SCREENSHOT GOES HERE

6. Open a ‘Powershell Terminal’ as an administrator, go to the location where the file is saved, and then run the script. You’ll be prompted to sign in a few times. Sign in as the admin user that set up the Azure subscription.  

    The script does the following: 

    1. Adds permission to the created service principal. 

    2. Launches Managed App, which creates resources in the customer sub. 

    3. Downloads a compressed file containing an executable to support Azure Stack Edge activation. 

    4. Activates the Azure Stack Edge device.

    5. Sets up the device for a Kubernetes Cluster. 

    6. Initializes the Kubernetes environment. 

    7. Installs Arc. 

    8. Prints a message of successful completion of this step.   

## Next step

[Install your cameras](install-cameras.md)
