

# Pair a gateway to a store by using the Dynamics 365 Connected Store mobile app

Next, you need to pair a gateway to your store. A gateway serves as a device aggregator, where your input devices are connected and paired. You must have at least one gateway to successfully create a connected store. If you’re working with a system integrator to install the hardware and set up the network, you may want to contact them for support with this step. 

Connect Azure Stack Edge and configure the network
1.	Use your laptop and the following documentation to connect Azure Stack Edge and configure the network: https://docs.microsoft.com/en-us/azure/databox-online/azure-stack-edge-deploy-connect-setup-activate
After signing in to Azure Stack Edge, you’ll see the Get started screen.
 
2.	Under Set up as standalone, select Start. 
3.	In the Get started with standalone device setup screen, select Configure next to Network.
 
4.	In the Network screen:
a.	Select the port that you connected your network to when you installed Azure Stack Edge (Port 2 if you have an RJ45 cable or Port 3 if you have an SFP cable).
 
b.	In the Network settings pane on the right side of the screen, select the Static tab, and then enter the IP addresses for Subnet mask, Gateway, Primary DNS, and Secondary DNS. Select Apply when you’re done.
 
Note: This is the information you recorded when working with the Site preparation section of the Installation guide. 
c.	In the Network screen, under Virtual IP settings, select Azure Consistent Services.
 
5.	In the Virtual IP settings pane, in the Azure Consistent Services network field, select the network (same as the static port configured earlier), select the Static tab, enter the IP address in the Azure Consistent Services Virtual IP field, and select Apply.In the left pane, select Device.
 
6.	In the Device screen, select the Apply settings button. You don’t need to make any changes in the Device screen, but you must select Apply settings. Otherwise the activation won’t work.
 
Note: At this time, you can’t change the device name. 
7.	In the left pane, select Update server.
8.	In the Update server screen, select Apply (you don’t need to make any changes in this screen).
 
9.	In the left pane, select Time.
10.	In the Time screen, select the correct time zone, and then select Apply. 
11.	In the left pane, select Get started.
12.	In the Get started with standalone device setup screen, select Activate. 
 
13.	Open the Connected Store mobile application (if it’s not already open).
Pair a gateway
1.	In the mobile app, on the Stores page, tap the store you just added in the Stores list. This opens the Gateways page. 
 
4.	Tap the + sign at the bottom of the page.
5.	Select the gateway you want to pair with, and then tap the Add button next to it. You’ll see the following message: 

“Go to aka.ms/ConnectedStore on your laptop and enter the following <security number> to get the activation key of your gateway.”

 

6.	Enter aka.ms/activategateway into your laptop web browser that’s connected to the gateway, and then select Sign in.
 
7.	Enter your Dynamics 365 Connected Store credentials.
 
8.	Enter the security number from the mobile app.
 
9.	Select the venue ID you created earlier in the mobile app, and then select Submit.
 
10.	When the activation key is ready, copy the key (use Copy to clipboard to copy the full key), paste it into the Activation key field in the Activate pane, and then select Activate.
 
The activation process can take from one to ten minutes. When the device is activated, a notification will appear on your laptop to inform you that activation is complete. The Dynamics 365 Connected Store modules will begin downloading on the gateway. This can take up to 60 minutes. You’ll see a notification in the mobile app when downloading is complete.
 
After Azure Stack Edge is connected, you can connect and configure the cameras as described in the next section of this guide.
Learn more about other actions you can do with gateways.

