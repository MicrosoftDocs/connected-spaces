

# Pair a gateway with the Dynamics 365 Connected Store mobile app

Before you can pair a gateway with the Microsoft Dynamics 365 Connected Store mobile app, you need to:

1. [Install Azure Stack Edge](ase-install.md).

2. [Connect Azure Stack Edge to your network](ase-connect.md).

3. [Create a store with the mobile app](mobile-app-create-store.md).

## Pair a gateway

To complete this procedure, you'll use the mobile app and your laptop, which should be connected to Azure Stack Edge as described in [Connect Azure Stack Edge to your network](ase-connect.md).

1.	On the **Stores** page, tap a store in the Stores list. This opens the **Gateways** page. 

   SCREEN SHOT GOES HERE
 
2.	Tap the **+** sign at the bottom of the page.

3.	Select the gateway you want to pair with, and then tap the **Add** button next to it. You’ll see the following message: 

   “Go to aka.ms/ConnectedStore on your laptop and enter the following <security number> to get the activation key of your gateway.”

  SCREEN SHOT GOES HERE

4.	Enter **aka.ms/activategateway** into your laptop web browser that’s connected to the gateway, and then select **Sign in**.
 
5.	Enter your Dynamics 365 Connected Store credentials.

   SCREEN SHOT GOES HERE
 
6.	Enter the security number from the mobile app.
 
   SCREEN SHOT GOES HERE
 
7.	Select the venue ID you created earlier in the mobile app, and then select **Submit**.

   SCREEN SHOT GOES HERE
 
8.	When the activation key is ready, copy the key (use **Copy to clipboard** to copy the full key), paste it into the **Activation** key field in the **Activate** pane, and then select **Activate**.

   SCREEN SHOT GOES HERE
 
   The activation process can take from one to ten minutes. When the device is activated, a notification will appear on your laptop to inform you that activation is complete. The Dynamics 365 Connected Store modules will begin downloading on the gateway. This can take up to 60 minutes. You’ll see a notification in the mobile app when downloading is complete.

   SCREEN SHOT GOES HERE
 
   After Azure Stack Edge is connected, you can [connect your cameras](mobile-app-add-cameras.md) and [add camera skill zones](mobile-app-add-camera-skill-zones.md). 



