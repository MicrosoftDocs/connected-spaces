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

3. Under **Add device details**, fill in the fields using the following information for assistance. 
 
    |Field|Description|
    |------------------------------------------|-----------------------------------------------------------------------------------|
    |AzureTenantID|The ID of the directory/tenant for the Azure Account being used|  
    |SubscriptionID|The ID of the Azure subscription to install Managed App| 
    |ResourceGroupName|The name of the resource group to install Managed App| 
    |DeviceIP|The local IP address of the Azure Stack Edge device (for example: 192.168.1.100)| 
    |DeviceSerialNumber|The serial number for the device (listed on the side of the physical device) or the local UI on the device (accessible by using the IP address for the device).| 
    |ComputeNode|The device interface number to install the compute node to, which should match the port number used to connect to the network (for example: 2)|
    |KubernetesNodeIpRangeStart|The first IP address of two contiguous open IP addresses on the same network as the Azure Stack Edge device| 
    |KubernetesNodeIpRangeEnd|The second and last IP address of two contiguous open IP addresses on the same network as the Azure Stack Edge device| 
    |KubernetesServiceIp|A range of open IP addresses on the same network that kubernetes can use for service endpoints. This can be a range of 1 single IP address (for example: 192.168.1.104-192.168.1.104)| 
    |Location|The location to create resources in (for example: eastus)| 
    |Service Principal App ID|Application ID of the enterprise app from the [service principal step](#create-a-service-principle)| 
    |Service Principal Object ID|Object ID of the enterprise app from the [service principal step](#create-a-service-principle)| 






4. After filling in the field values, open a Powershell window as an administrator. 

    > [!NOTE]
    > You must have administrator privileges on your computer to open PowerShell. 

     ![Screenshot of Windows PowerShell window.](media/ase-connect-powershell.jpg "Screenshot of Windows PowerShell window")

5. Use the following command to change your directory to the customer folder containing the files that you requested in step 2.

     ![Screenshot of cd command.](media/ase-connect-change-directory.jpg "Screenshot of cd command")

6. Run the following command to kick off the script to configure and activate your device:

    ./ase_up_customer.ps1

7. When prompted to enter a password, enter the password that was used to set up the Azure Stack Edge device initially. 

8. When prompted to sign in to Azure, use the same credentials you used to create the resources in your subscription.

    You'll know that the script is complete when the PowerShell window accepts input again. The last message you'll see from the script is: "Arc setup starting..."

9. After the script has completed, contact Microsoft to take over for the final steps to set up your environment. 

## Next step

[Install your cameras](install-cameras.md)
