---
author: alwinv
description: Learn how to install Dynamics 365 Connected Store (public preview)
ms.author: alwinv
ms.date: 07/08/2020
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
    
    This step can take from 5-30 minutes. You’ll see a progress indicator showing where you are in the installation process. During this time, setup:
    
    - Creates a Microsoft Power Platform default environment for your Azure Active Directory tenant
    
    - Creates a Common Data Service instance and sets up a database
    
    - Installs the Connected Store solutions in the environment
    
    While Connected Store is being installed, you can watch a video demo and learn more about preparing for Connected Store.
    
    ![Welcome to Connected Store screen with video demo](media/demo-connected-store.PNG "Welcome to Connected Store screen with video demo")
    
    If the setup process fails, you’ll see the following message:
   
    ![Installation failed message](media/install-failed-message.PNG "Installation failed message")
    
    If this happens, try installing again.
    
## Next step

[Order the Azure Stack Edge gateway](admin-request-ase.md)
