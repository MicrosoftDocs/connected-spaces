---
author: kfrankc-ms
description: Learn how to connect Azure Stack Edge to your network to use with Dynamics 365 Connected Store Preview
ms.author: frch
ms.date: 12/07/2020
ms.service: crm-online
ms.topic: article
title: Connect Azure Stack Edge to your network for use with Dynamics 365 Connected Store Preview
ms.reviewer: v-brycho
---

# Connect Azure Stack Edge Pro (2 GPU) to your network for use with Dynamics 365 Connected Store Preview

After you've [installed Azure Stack Edge Pro (2 GPU)](ase-install.md), you're ready to connect it to your network and configure the network for use with Microsoft Dynamics 365 Connected Store Preview. If you're working with a system integrator to install the hardware and set up the network, you may want to contact them for support with this step. 

## Connect Azure Stack Edge and configure the network

1. Use your laptop and the following documentation to connect Azure Stack Edge Pro and configure the network: https://docs.microsoft.com/azure/databox-online/azure-stack-edge-deploy-connect-setup-activate

    After signing in to Azure Stack Edge Pro, next to **Network**, select **Not configured** to start the configuration process.

    ![Configure command](media/ase-configure-network.PNG "Configure command")

2. In the **Network** screen:

    1. Select the port that you connected your network to when you [installed Azure Stack Edge](ase-install.md) (Port 2 if you have an RJ45 cable or Port 3 if you have an SFP cable).

        ![Network screen](media/ase-network.PNG "Network screen")

    2. In the **Network settings** pane on the right of the screen, **DHCP** should be selected by default. If Dynamic Host Configuration Protocol (DHCP) is enabled in your environment, network interfaces are automatically configured. These interfaces include an Internet Protocol (IP) address, subnet, gateway, and Domain Name Service (DNS).

        If DHCP isn't enabled in your environment, you can assign static IP addresses as required. On the **Static** tab, enter the IP addresses in the **Subnet mask**, **Gateway**, **Primary DNS**, and **Secondary DNS** fields. When you've finished, select **Apply**. [See the Azure Stack Edge Pro GPU setup documentation to learn more](https://docs.microsoft.com/azure/databox-online/azure-stack-edge-gpu-deploy-configure-network-compute-web-proxy#configure-network).

        ![Network settings pane](media/ase-network-settings.PNG "Network settings pane")

        > [!NOTE]
        > This is the information you recorded when you [installed Azure Stack Edge Pro](ase-install.md).

3. In the left pane, select **Compute**.

    ![Compute command selected in the left pane](media/ase-compute.PNG "Compute command selected in the left pane")

    In the **Compute** screen:

    1. Select the port that you want to open to the Compute networks. This port will probably be Port 2, which is the outward-facing IP address for the device.

        ![Port 2 highlighted in the Compute screen](media/ase-compute-port-2.PNG "Port 2 highlighted in the Compute screen")

    2. On the right side of the screen, under **Enabled for compute**, select **Yes**.

    3. In the **Network settings (Port 2)** screen, in the **Kubernetes node IPs** field, assign static IP addresses for the compute virtual machine (VM) on the device. For a one-node device, provide a contiguous range of at least two contiguous IPV4 addresses.

        ![Network settings (Port 2) screen](media/ase-compute-apply.PNG "Network settings (Port 2) screen")

        > [!NOTE]
        > Make sure that the IP addresses are available. If the compute VMs must compete for an IP address, you will receive an error because of the inconsistent connection.

    4. In the **Kubernetes external service IPs** field, assign the external service IP addresses. These contiguous IP addresses are for services that you want to expose outside the Kubernetes cluster. Specify the static IP range, depending on the number of services that are exposed. At a minimum, you must allocate at least one external IP address to configure the Connected Store service. In the screenshot example above, one IP address is allocated. 

    5. Select **Apply**.

4. In the left pane, select **Web proxy**. By default, the **Web proxy** tab is set to **Disable**. If you require a proxy address to establish a consistent connection between Azure resources and the device:

    1. Switch the tab to **Enable**.

        ![Web proxy tab set to Enable](media/ase-web-proxy-authentication-address.PNG "Web proxy tab set to Enable")

    2. In the **Web proxy URL** field, enter a URL.

    3. Optional: Include an authentication address to handle secure proxy communications.

    > [!NOTE]
    > If you plan to use a web proxy, contact the Connected Store team so that we can prepare your deployment.

5. In the left pane, select **Device**, and then select **Apply**. You don't have to make any changes in the **Device** screen, but you must select **Apply**. Otherwise, the activation won't work.

    ![Device screen](media/ase-device.PNG "Device screen")

    > [!NOTE]
    > At this time, you can't change the device name.

6. In the left pane, select **Update server**, and then select **Apply**. (You don't have to make any changes in this screen.)

    ![Update server screen](media/ase-update-server.PNG "Update server screen")

7. In the left pane, select **Time**, select the correct time zone, and then select **Apply**.

    ![Time screen](media/ase-select-time-zone.PNG "Time screen")

## Next step

[Install your cameras](install-cameras.md)
