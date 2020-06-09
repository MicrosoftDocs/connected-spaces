

# Connect Azure Stack Edge to your network for use with Dynamics 365 Connected Store

After you've installed Azure Stack Edge, you're ready to connect it to your network. If you’re working with a system integrator to install the hardware and set up the network, you may want to contact them for support with this step. 

## Connect Azure Stack Edge and configure the network

1.	Use your laptop and the following documentation to connect Azure Stack Edge and configure the network: https://docs.microsoft.com/en-us/azure/databox-online/azure-stack-edge-deploy-connect-setup-activate

    After signing in to Azure Stack Edge, you’ll see the **Get started** screen.
    
    SCREEN SHOT GOES HERE
 
2.	Under **Set up as standalone**, select **Start**. 

3.	In the **Get started with standalone device setup** screen, select **Configure** next to **Network**.

   SCREEN SHOT GOES HERE
 
4.	In the **Network** screen:

    a.	Select the port that you connected your network to when you installed Azure Stack Edge (Port 2 if you have an RJ45 cable or Port 3 if you have an SFP cable).
    
    SCREEN SHOT GOES HERE
 
b.	In the **Network settings** pane on the right side of the screen, select the **Static** tab, and then enter the IP addresses for **Subnet mask**, **Gateway**, **Primary DNS**, and **Secondary DNS**. Select **Apply** when you’re done.

    SCREEN SHOT GOES HERE
 
   > [!NOTE]
   > This is the information you recorded when working with the Site preparation section of the Installation guide. 
    
c.	In the **Network** screen, under **Virtual IP settings**, select **Azure Consistent Services**.

    SCREEN SHOT GOES HERE
 
5.	In the **Virtual IP settings** pane, in the **Azure Consistent Services network** field, select the network (same as the static port configured earlier), select the **Static** tab, enter the IP address in the **Azure Consistent Services Virtual IP** field, and then select **Apply**.

6. In the left pane, select **Device**.

    SCREEN SHOT GOES HERE
 
7.	In the **Device** screen, select the **Apply settings** button. You don’t need to make any changes in the **Device** screen, but you must select **Apply settings**. Otherwise, the activation won’t work.
 
    > [!NOTE]
    > At this time, you can’t change the device name. 

8.	In the left pane, select **Update server**.

    SCREEN SHOT GOES HERE

9.	In the **Update server** screen, select **Apply** (you don’t need to make any changes in this screen).

    SCREEN SHOT GOES HERE
 
10.	In the left pane, select **Time**.

11.	In the **Time** screen, select the correct time zone, and then select **Apply**. 

12.	In the left pane, select **Get started**.

13.	In the **Get started with standalone device setup** screen, select **Activate**. 

    SCREEN SHOT GOES HERE
 
14.	Open the Connected Store mobile application, and then do the following:

    a. [Create a store](mobile-app-create-store.md).
    
    b. [Pair a gateway](mobile-app-pair-gateway.md).
