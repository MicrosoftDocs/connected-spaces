---
author: alissapolucha
description: Learn how to create a store by using the Dynamics 365 Connected Store (public preview) mobile app
ms.author: alissag
ms.date: 07/01/2020
ms.service: crm-online
ms.topic: article
title: Create a store with the Dynamics 365 Connected Store (public preview) mobile app 
ms.reviewer: v-brycho
---

# Create a store with the Dynamics 365 Connected Store (public preview) mobile app

After you [prepare your network and install Azure Stack Edge](ase-install.md), you’re ready to create a store with the 
Microsoft Dynamics 365 Connected Store (public preview) mobile app. 

## Create a store

1. On the **Stores** page, tap the **+** sign.

     ![Create store + sign](media/create-store.PNG "Create store + sign")
  
2. On the **Create Store** page:

   a. In the **Store Name** field, enter a friendly name for the store.

   b. In the **Allow Location Access** field, move the slider to the On position if you want to detect the location from your 
mobile device. You can also enter your location manually, but make sure to enter the information carefully since this field doesn't autofill.

   c. Tap the **Add Store Image** field, and then do one of the following:

      - Select a photo from your phone files.

      - Take a picture with your phone camera.
    
   ![Add Store Image field](media/store-add-field-image.PNG "Add Store Image field")
 
3. When you’re done, tap the check mark in the upper-right corner of the page.

    On the **Stores** page, you’ll see your new store in the Stores list. The Stores list shows at a glance the name of the store, 
    how many gateways are set up for the store, and the store location.
    
    ![Stores list](media/stores-list.PNG "Stores list")
    
If this is the first store that you're creating in the mobile app, the next step is to learn how to [pair a gateway](mobile-app-pair-gateway.md) so you can add cameras and camera skill zones.
    
 ## Get more information about a store
 
In the Stores list, you can see at a glance how many gateways each store has and the location of the store. To get more information 
about a store, including the creation date, number of cameras, and zones:

1. Tap the **Actions** button in the upper-right corner of the page.

2. Tap **Info** at the bottom of the page.

    ![Info button](media/store-info.PNG "Info button")
 
3. Review the info. 

    ![List of store fields](media/store-fields.PNG "List of store fields")
    
    The following table describes each field and specifies whether the field is editable from the **Store Info** page:

    |Field|Description|
    |----------------------|--------------------------------------------|
    |**Store Name**|The friendly name of the store|
    |**Allow Location Access**|Allow your device to determine your location|
    |**Set Time Zone**|Set the time zone for the store|
    |**Add Store Image**|Select a photo from your files or take a picture with your phone camera|

4. When you’re finished, tap the check mark in the upper-right corner of the page to go back to the **Stores** page.

## Rename a store

1. Tap the **Actions** button in the upper-right corner of the page.

2. Tap **Rename** at the bottom of the page.

    ![Rename button](media/store-rename.PNG "Rename button")
    
## Sort the Stores list

If you have a lot of stores in your Stores list, you might want to sort the list to find the store you're looking for. 

To sort or filter the Stores list:

- Select the **Sort** ![Filter button](media/filter-button.PNG "Filter button") button at the top of the **Stores** page.

 
## What's next?

[Pair a gateway](mobile-app-pair-gateway.md)

[Connect cameras to the gateway](mobile-app-add-cameras.md)

[Add camera skill zones](mobile-app-add-camera-skill-zones.md)
 
