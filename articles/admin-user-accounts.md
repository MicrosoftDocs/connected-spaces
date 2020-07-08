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

1. In the Connected Store web app, select **Settings**, and then select a store from the list.

     ![Store in list selected](media/select-store-add-users.PNG "Store in list selected")

    > [!NOTE]
    > If no store is available in the list, use the mobile app to create a store first.
    
2. Switch to the **Users** tab, and then select **Assign security roles**.

    ![Assign security roles command selected](media/assign-security-roles.PNG "Assign security roles command selected")
    
3. Select the check box next to the appropriate user account.

    ![Check box next to use account highlighted](media/select-user-add-users.PNG "Check box next to use account highlighted")
    
4. Select **MANAGE ROLES**. 

   ![Manage roles command selected](media/manage-roles.PNG "Manage roles command selected")

5. Select the **Connected Store Admin** or **Connected Store Viewer** security role, and then select **OK**. 

   ![Two Connected Store security roles highlighted](media/manage-user-roles.PNG "Two Connected Store security roles highlighted")


[Learn more about creating users and assigning security roles](https://go.microsoft.com/fwlink/?linkid=2128632) for Dynamics 365 applications.

## Next step

[Start planning camera placement](camera-placement-checklist.md)


