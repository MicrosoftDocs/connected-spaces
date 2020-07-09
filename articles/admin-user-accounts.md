---
author: alwinv
description: Learn how to give users permissions to use Dynamics 365 Connected Store (public preview).
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

    ![Select default environment](media/select-default-environment-placeholder.PNG "Select default environment")
    
3. Select **Settings**.

    ![Select Settings command](media/select-settings-placeholder.PNG "Select Settings command")
    
4. Expand the **Users + permissions** heading, and then select **Users**.

    ![Select Users command](media/select-users-placeholder.PNG "Select Users command")

5. Do one of the following:

   - If the users are already in the list, skip to step 6 to assign user roles.       
   
   - If you need to add one or more users, select **Add user**, enter the account details, and then select **Add**. 

    ![Select Add user command](media/select-add-user-placeholder.PNG "Selected Add user command")    
    
6. In the **Enabled Users** screen, select the check box next to the appropriate user account.    

   ![Select check box for user account](media/select-user-placeholder.PNG "Select check box for user account")
   
    >[!NOTE]
    > If you recently added a new user account to your Azure Active Directory tenant, it may take a few minutes for it to appear in this list. Select the **Refresh** button to refresh the list.
   
7. Select **MANAGE ROLES**. 

    ![Select Manage Roles command](media/select-manage-roles-placeholder.PNG "Select Manage Roles command")

8. Select the **Connected Store Admin** or **Connected Store Viewer** security role, and then select **OK**. 

    ![Select specific role check box](media/select-role-placeholder.PNG "Select specific role check box")

[Learn more about creating users and assigning security roles](https://go.microsoft.com/fwlink/?linkid=2128632) for Dynamics 365 applications.

## Next step

[Start planning camera placement](camera-placement-checklist.md)


