---
author: alissapolucha
description: Learn how to use the Dynamics 365 Connected Store (public preview) mobile app to pair a gateway so you can connect LP cameras.
ms.author: alissag
ms.date: 07/23/2020
ms.service: crm-online
ms.topic: article
title: Pair a gateway with the Dynamics 365 Connected Store (public preview) mobile app
ms.reviewer: v-brycho
---

# Pair a gateway with the Dynamics 365 Connected Store (public preview) mobile app

Before you can pair a gateway with the Microsoft Dynamics 365 Connected Store (public preview) mobile app, you need to:

1. [Install Azure Stack Edge](ase-install.md)

2. [Connect Azure Stack Edge to your network](ase-connect.md)

3. [Create a store with the mobile app](mobile-app-create-store.md)

## Pair a gateway

To complete this procedure, you'll use the mobile app and your laptop, which should be connected to Azure Stack Edge as described in [Connect Azure Stack Edge to your network](ase-connect.md).

1.	On the **Stores** page, tap a store in the Stores list. 

    ![Stores list](media/stores-list.PNG "Stores list")
    
    This opens the **Gateways** page. 
 
2.	Tap the **+** sign at the bottom of the **Gateways** page.

    ![Add gateway](media/add-gateway.PNG "Add gateway")

3.	Select the gateway you want to pair with, and then tap the **Add** button next to it. You’ll see the **Add Gateway** screen and the following message: 

    “Go to aka.ms/activategateway on your laptop and enter the following serial number to get the activation key of your gateway.”

    ![Pairing instructions](media/pairing-instructions.PNG "Pairing instructions")

4.	Enter **aka.ms/activategateway** into your laptop web browser that’s connected to the gateway, and then select **Sign in**.

5.	Enter your Dynamics 365 Connected Store credentials.
     
6.	Enter the serial number from the mobile app.
 
    ![Device serial number box](media/security-number.PNG "Device serial number box")
 
7.	Select the store you created earlier in the mobile app, and then select **Submit**.

    ![Select store name](media/select-store-name.PNG "Select store name")

    > [!IMPORTANT]
    > You must activate Azure Stack Edge within 24 hours after the activation key is generated. 
 
8.	When the activation key is ready, copy the key (use **Copy to clipboard** to copy the full key), go to the Azure Stack Edge **Get Started** page, select **Activate**, paste the key into the **Activation key** field in the **Activate** pane, and then select **Activate**. 

    ![Activate pane](media/ase-activate-pane.PNG "Activate pane")
 
    The activation process can take from one to ten minutes. 
    
    >[!TIP] 
    >You can select the **Bell** button in the upper-right corner of the **Azure Stack Edge** page to monitor activation status. 
    
    When the device is activated, a notification will appear in the **Azure Stack Edge** page to let you know that the activation is complete. 

    ![Device activated notification](media/device-activated.PNG "Device activated notification")
 
    The Dynamics 365 Connected Store modules will begin downloading on the gateway. This can take up to 60 minutes. You'll know that the gateway is connected when it appears in the **Gateways** page in the mobile app. 
    
    ![Gateways page in mobile app showing gateway is paired](media/gateway-paired.PNG "Gateways page in mobile app showing gateway is paired") 
    
    After Azure Stack Edge is connected, you can [connect your cameras](mobile-app-add-cameras.md) and [add camera skill zones](mobile-app-add-camera-skill-zones.md). 

## Get more information about a gateway created in the mobile app

To get more information about a gateway:

1.	On the **Gateways** page, tap the **Actions** button, and then tap **Info** at the bottom of the screen.

    ![Info button](media/gateway-info.PNG "Info button")
 
2.	Review the info.

    ![Gateway fields](media/gateway-fields.PNG "Gateway fields")
 
    > [!IMPORTANT]
    > The gateways paired to your store can’t be shared between the different stores of your organization. To pair an available gateway, contact your account admin.
   
    The following table describes each field:

    |Field|Description|
    |--------------|------------------------------------------------------------|
    |**Name**|The friendly name of the gateway|
    |**IP Camera Range Scan**|- The **IP Start Range** and the **IP End Range** show the IP address range secured [when your network was prepared for Azure Stack Edge](ase-install.md)<br><br>- The **Port** field shows which Port your network is connected to.|
       
4.	When you’re finished, select the check mark in the upper-right corner of the screen.
  
## Sort the Gateways list

If you have a lot of gateways in your Gateways list, you might want to sort the list to find the gateway you're looking for. 

To sort the Gateways list:

- Select the **Sort** ![Filter button](media/filter-button.PNG "Filter button") button at the top of the **Gateways** page.

## Next steps

[Connect cameras to the gateway](mobile-app-add-cameras.md)

[Add camera skill zones](mobile-app-add-camera-skill-zones.md)