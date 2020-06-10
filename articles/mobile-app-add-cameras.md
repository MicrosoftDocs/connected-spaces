

# Connect a camera to a gateway with the Dynamics 365 Connected Store mobile app

After you've paired a gateway to your store in Microsoft Dynamics 365 Connected Store, you can connect your cameras to the gateway. Keep in mind that cameras are connected to a specific gateway. You won’t be able to find or add a camera if it isn’t available on the gateway network. You can connect any camera on the same network as your gateway.

If your store has multiple gateways you’ll need to access them one by one to see all the connected or available cameras. You can pair up to 10 cameras per gateway. If you need more cameras for your store, contact your account manager to request an additional gateway.

If you haven't already installed your cameras, see: 

- [Plan camera placement](camera-placement-checklist.md)

- [Install your cameras](install-cameras.md)

## Connect a camera to a gateway

1. On the **Gateways** page, tap the gateway you want to add a camera to. This opens the **Cameras** page.   

2. On the **Cameras** page, tap the **+** button. 

    SCREEN SHOT GOES HERE
 
3. Select an available camera, and then tap the **+** sign  next to it. (You’ll see the camera feed after you sign in).

   > [!TIP]
   > To add multiple cameras that use the same sign-in credentials, tap a camera image, tap the button to the left of each camera you want to add, and then tap the **+** button in the upper-right corner of the page.
    
    SCREEN SHOT GOES HERE
 
4.	Enter the current username and password for the camera (supplied by your IT administrator), and then select **Apply** (or **Apply All** if you selected multiple cameras).
 
    SCREEN SHOT GOES HERE
    
After connecting a camera to a gateway, you can [add a camera skill zone](mobile-app-add-camera-skill-zone.md)

## Get more information about a camera

On the **Cameras** page, you can get quick information about the camera from the Camera View list. For example, you can see the name of the camera, the IP address, a still image, the date the image was last updated, and whether the camera is connected or not. To get more information about a camera, including the camera description, camera credentials, network properties, firmware, and device model:

1. On the **Cameras** page, tap the **Actions** button.

2. Tap **Info** at the bottom of the page.

    SCREEN SHOT GOES HERE
 
3. Review and/or edit the information.

    SCREEN SHOT GOES HERE
 
The following table describes each field and specifies whether the field is editable from the **Camera Info** page:

|Field|Description|Editable?|
|-------------------|----------------------------------------------------|------|
|Name|The friendly name of the camera|Yes|
|Description|Brief description about the camera|Yes|
|Network Details|The IP Address and MAC Address. For more information, see [prepare your network and install Azure Stack Edge](ase-install.md)|No|
|Credentials|The username and password for the camera|Yes|
|Device info|The firmware and camera model|No|

4.	When you’re finished, select the check mark in the upper-right corner of the page to go back to the **Cameras** page.

## Rename a camera

1. On the **Cameras** page, select the **Actions** button.

2. Select **Rename** at the bottom of the page.

    SCREEN SHOT GOES HERE

## Remove a camera

1. On the **Cameras** page, select the **Actions** button.

2. Select **Remove** at the bottom of the page.

    SCREEN SHOT GOES HERE
 
## What's next?

[Add camera skill zones](mobile-app-add-camera-skill-zones.md)

