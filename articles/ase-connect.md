---
author: kfrankc-ms
description: Learn how to connect Azure Stack Edge to your network to use with Dynamics 365 Connected Spaces Preview
ms.author: rapraj
ms.date: 12/02/2021
ms.topic: article
title: Connect Azure Stack Edge to your network for use with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Connect Azure Stack Edge Pro (2 GPU) to your network for use with Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

After you've [installed Azure Stack Edge Pro (2 GPU)](ase-install.md), you're ready to connect it to your network and configure the network for use with Microsoft Dynamics 365 Connected Spaces Preview. If you're working with a system integrator to install the hardware and set up the network, you might want to contact them for support with this step. 

## Initial setups and checks

1. Follow [the Windows Remote Management instructions](https://docs.microsoft.com/windows/win32/winrm/installation-and-configuration-for-windows-remote-management#quick-default-configuration) to install Windows Remote Management in your environment.

2. Pull the following files from this storage account (will need to update as the account hasn’t been created yet):

    ase_up_customer.ps1<br>
    ase_up_customer_utility.ps1<br>
    device_settings.json

3. Fill in the values in the device_settings.json file.

     ![Windows Remote Management settings.](media/ase-connect-windows-remote-management.jpg "Windows Remote Management settings")
 
    |Field|Value|
    |------------------------------------------|-----------------------------------------------------------------------------------|
    |AzureSubscriptionName|The Azure subscription name you created the resource group in|
    |AzureResourceGroupName|The Azure resource group name you created the Asure Stack Edge resource in|
    |AzureResourceDeviceName|The name of the Azure Stack Edge resource you created|
    |DeviceSerialNumber|The serial number on the side of the phsyical device or the LocalUI of the device|
    |DeviceIp|The IP address that your device is set to|
    |KubernetesNodeIpRangeStart|The first of two sequential free IP addresses on your network|
    |KubernetesNodeIpRangeEnd|The last of two sequential free IP addresses on your network|
    |KubernetesServiceIp|Another free IP address on your network|
    |ComputeNode|The number of compute nodes on your device; "2" is a solid base value|
    |ActivationKey|The key that was generated using the Azure resource|


4. After filling in the field values, open a Powershell window as an administrator. 

     ![Screenshot of Windows Powershell window.](media/ase-connect-powershell.jpg "Screenshot of Windows Powershell window")

5. Change your directory to the customer folder containing all the scripts using this command:

     ![Screenshot of cd command.](media/ase-connect-change-directory.jpg "Screenshot of cd command")

6. Run the ase_up_customer.ps1 script you downloaded earlier.

7. When prompted to enter a password, enter the password that was used to set up the Azure Stack Edge device initially. 

8. When prompted to sign in to Azure, use the same login you used to create the resources in your subscription.

9. After the script has completed, Microsoft will complete the final process before you are ready for use.

## Next step

[Install your cameras](install-cameras.md)
