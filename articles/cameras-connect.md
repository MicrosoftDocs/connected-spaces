---
author: alissapolucha
description: Learn how to connect an LP camera to a gateway in Dynamics 365 Connected Spaces Preview
ms.author: alissag
ms.date: 11/06/2020
ms.topic: article
title: Connect your cameras to a gateway in Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Connect your cameras to a gateway in Dynamics 365 Connected Spaces Preview 

[!INCLUDE[banner](includes/banner.md)]

After you've paired a gateway to your store, you can connect your cameras to the gateway. Keep in mind that cameras are connected to a specific gateway. You can connect any camera approved for Connected Spaces on the same network as your gateway.

## Prerequisites

You need to do the following before you can connect your cameras to a gateway:

- [Install the cameras](install-cameras.md).

- Gather the RTSP URLs and credentials for all the cameras you want to connect.

- Have access to a previously configured gateway.

- Connect your computer to the same network as your gateway.

## Connect cameras

1. On the **Devices** page, select **Add cameras**. 

    ![Add camera button highlighted.](media/add-camera-command.jpg "Add camera button highlighted")
    
2. On the **Add camera** page, you'll see the list of prerequisites that you must do before you can connect cameras. If you've already completed these steps, select **Start** to begin connecting cameras. 

    ![Screenshot of Get started page showing prerequisites.](media/add-camera-prerequisites.jpg "Screenshot of Get started page showing prerequisites")    
 
3. In the **Connecting cameras** section, fill in the fields in the **Connect camera** pane on the right side of the page for each camera that you want to connect.

    ![Screenshot of Connecting cameras page.](media/connecting-cameras-page.jpg "Screenshot of Connecting cameras page")

    Use the following information to fill in the fields:

    1. In the **RTSP URL** field, enter the RTSP URL for your camera.

    2. In the **Username** and **Password** fields, enter the username and password for the camera supplied by your IT administrator.

    3. In the **Camera name** field, enter a friendly name for your camera to help identify it by location. 

    4. In the **Camera view image** field, select **Upload image** to upload an image of the camera's field of view.
    
     > [!NOTE]
     > An uploaded image is used to define where you want the AI skill to collect data. We recommend uploading an image that doesn't capture any personal data in the field of view. The image is compressed if it's larger than 2 MB.

    5. Select **Connect** to add the camera. The camera will appear in the middle of the screen under **All cameras**. 

       ![Screenshot showing two cameras added under All cameras heading.](media/cameras-added.jpg "Screenshot showing two cameras added under All cameras heading")

    6. Repeat the above steps for each camera that you want to add.

4. When you're finished adding cameras, under **All cameras**, select the button next to each camera you want to connect, and then select **Next** at the bottom of the page. 

    ![Screenshot showing two cameras selected.](media/selected-camera.jpg "Screenshot showing two cameras selected")
    
5. On the **Review and finish** page, review the details, and then select **Add** to add the cameras.

     ![Screenshot of Review and finish page.](media/cameras-review-finish.jpg "Screenshot of Review and finish page")
     
 6. Select **Finish** to complete the camera connection process.

    ![Screenshot of Finish page.](media/cameras-finish.jpg "Screenshot of Finish page")
    
## Edit camera details

You can edit the details for any camera from the **Devices** page. 

1. Select the button for the Action menu (...), and then select **Camera details**. 

    ![Screenshot of Action button and Camera details command.](media/camera-details.jpg "Screenshot of Action button and Camera details command")
    
2. Make any changes in the pane on the right side of the screen, and then select **Save**.

     ![Screenshot of pane on right side of the screen.](media/camera-details-edit.jpg "Screenshot of pane on right side of the screen")
     
## Remove a camera

1. Select the button for the Action menu (...), and then select **Remove**. 

    ![Screenshot of Action button and Remove command.](media/camera-details.jpg "Screenshot of Action button and Remove command")
    
    > [!NOTE]
    > This will permanently remove the camera. To add the camera back again, on the **Devices** page, select **Add cameras** as described earlier in this article. 

## Next step

[Add camera skills](mobile-app-add-camera-skill-zones.md)
