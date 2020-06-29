

# Give users permissions to use Dynamics 365 Connected Store

As an Azure Active Directory global admin, you can assign security roles to user accounts, to enable them to do different tasks in Dynamics 365 applications.

## Connected Store security roles

To give users permissions to use the Connected Store, you must first assign either the **Connected Store Viewer** or **Connected Store Admin** role to any user accounts. 

> [!NOTE]
> The **Connected Store Admin** role is a superset of the **Connected Store Viewer** role.

The following table describes the privileges that each role grants.

|Role|	Description|
|--------------------------------|----------------------------------------------------------------------------------------------|
|
Connected Store Viewer|	Use the Connected Store web appl to:<br><br>
- View the analytics dashboard, which provides insights on Shopper analytics, Display effectiveness, and Queue management camera skill zones<br>
- View the health status of gateway devices <br>
- View store settings<br>
|Connected Store Admin|	Use the Connected Store mobile app to:<br><br>
- Create stores and edit store information<br>
- Pair gateways and edit gateway information<br>
- Connect cameras to a gateway and edit camera information<br>
- Create and modify camera skill zones<br><br>
Use the Connected Store web app to:<br><br>
- View the analytics dashboard, which provides insights on Shopper analytics, Display effectiveness, and Queue management camera skill zones<br>
- View the health status of gateway devices<br>
- View and modify store settings, such as operating hours, time zone, and address|

## Assign a Connected Store security role to a user account

1. In the Connected Store web app, select Settings, and then, select a store from the list.

    SCREEN SHOT GOES HERE

    > [!NOTE]
    > If no store is available in the list, use the mobile app to create a store first.
    
2. Switch to the **Users** tab and then select **Assign security roles**.

    SCREEN SHOT GOES HERE
    
3. Select the check box next to the appropriate user account.

    SCREEN SHOT GOES HERE
    
4. Select **MANAGE ROLES**. 

   SCREEN SHOT GOES HERE

5.Select the **Connected Store Admin** or **Connected Store Viewer** security role, and select **OK**. 

   SCREEN SHOT GOES HERE

## Learn more

[Learn more about creating users and assigning security roles](https://go.microsoft.com/fwlink/?linkid=2128632) for Dynamics 365 applications.

## What's next?


