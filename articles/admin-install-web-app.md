---
author: alwinv
description: Learn how to install Dynamics 365 Connected Store (public preview)
ms.author: alwinv
ms.date: 10/15/2020
ms.service: crm-online
ms.topic: article
title: Install Dynamics 365 Connected Store (public preview)
ms.reviewer: v-brycho
---

# Install Dynamics 365 Connected Store (public preview) 

After you have [created an Azure Active Directory tenant](admin-create-new-tenant.md) for Microsoft Dynamics 365 Connected Store (public preview), you can 
install Dynamics 365 Connected Store.

>[!NOTE]
>To install Connected Store, you must sign in with the global adminstrator account for your [Azure Active Directory tenant](admin-create-new-tenant.md), or with an account that has the System Administrator security role.

1. [Go to the Connected Store setup page](https://go.microsoft.com/fwlink/?linkid=2128110).

2. Read through the [Terms of Use](https://go.microsoft.com/fwlink/?linkid=2128595), and then when you’re ready, select **Install**.

     ![Install button](media/install-connected-store.PNG "Install button")
    
    This step can take from 5-30 minutes. You’ll see a progress indicator showing where you are in the installation process. During this time, setup installs the Connected Store solutions in the selected environment. By default, setup creates a new trial (subscription-based) environment. If you want to install Connected Store in a different environment, select an environment from the **Choose environment** list. The list only shows environments that are enabled for installing Dynamics 365 applications. [Learn more about environments]().
    
    ![Drop-down list of enabled environments](media/enabled-environments.PNG "Drop-down list of enabled environments")
        
    If the setup process fails, you’ll see the following message:
   
    ![Installation failed message](media/install-failed-message.PNG "Installation failed message")
    
    If this happens, try installing again.
    
## Next step

[Order the Azure Stack Edge gateway](admin-request-ase.md)
