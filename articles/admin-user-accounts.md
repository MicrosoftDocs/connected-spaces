---
author: alwinv
description: Learn how giver users permissions to use Dynamics 365 Connected Store (public preview).
ms.author: alwinv
ms.date: 07/08/2020
ms.service: crm-online
ms.topic: article
title: Give users permissions to use Dynamics 365 Connected Store (public preview)
ms.reviewer: v-brycho
---

# Give users permissions to use Dynamics 365 Connected Store (public preview)

As an Azure Active Directory global admin, you can assign security roles to user accounts to enable users to do different tasks in Microsoft Dynamics 365 Connected Store (public preview).

## Connected Store security roles

To give users permissions to use Connected Store, you must first assign either the **Connected Store Viewer** or **Connected Store Admin** role to any user accounts. 

> [!NOTE]
> The **Connected Store Admin** role is a superset of the **Connected Store Viewer** role.

The following table describes the privileges that each role grants.

|Role|	Description|
|--------------------------------|----------------------------------------------------------------------------------------------|
|**Connected Store Viewer**|	Use the Connected Store web app to:<br><br>- View the analytics dashboard, which provides insights on Shopper analytics, Display effectiveness, and Queue management camera skill zones<br>- View the health status of gateway devices <br>- View store settings, such as operating hours, time zone, and address<br>
|**Connected Store Admin**|	Use the Connected Store mobile app to:<br><br>- Create stores and edit store information<br>- Pair gateways and edit gateway information<br>- Connect cameras to a gateway and edit camera information<br>- Create and modify camera skill zones<br><br>Use the Connected Store web app to:<br><br>- View the analytics dashboard, which provides insights on Shopper analytics, Display effectiveness, and Queue management camera skill zones<br>- View the health status of gateway devices<br>- View and modify store settings, such as operating hours, time zone, and address|

## Assign a Connected Store security role to a user account

1. Open the [Power Platform admin center](https://admin.powerplatform.com/). 
        
2. Select the default environment.

    ![XXX](media/XXX.PNG "XXX")
    
3. Select **Settings**.

    ![XXX](media/XXX.PNG "XXX")
    
4. Expand the **Users and Permissions** heading, and then select **Users**.

    ![XXX](media/XXX.PNG "XXX")

5. Review the list of users. If the users are already in the list, select **Manage users in Dynamics 365**.

    ![XXX](media/XXX.PNG "XXX")
   
    > [!NOTE]
    > It may take a few minutes for the list to refresh with new users. To update the list immediately, select **Add user**, type the account name or email address, and then select **Add**.<br>![XXX](media/XXX.PNG "XXX")
    
6. Select the check box next to the appropriate user account.    

    ![XXX](media/XXX.PNG "XXX")
   
    >[!NOTE]
    > If you recently added a new user account to your Azure Active Directory tenant, it may take a few minutes for it to appear in this list. Select the **Refresh** button to refresh the list.
   
7. Select **MANAGE ROLES**. 

    ![XXX](media/XXX.PNG "XXX")

8. Select the **Connected Store Admin** or **Connected Store Viewer** security role, and then select **OK**. 

    ![XXX](media/XXX.PNG "XXX")

[Learn more about creating users and assigning security roles](https://go.microsoft.com/fwlink/?linkid=2128632) for Dynamics 365 applications.

## Next step

[Start planning camera placement](camera-placement-checklist.md)


