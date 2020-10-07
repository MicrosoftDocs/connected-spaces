

# Use the Command Center in the Dynamics 365 Connected Store web app to set up a maximum store occupancy notification 

You can set the maximum occupancy threshold for a store in the Microsoft Dynamics 365 Connected Store mobile app. When you set the **Maximum occupancy** value, 
you'll see the following items on the [**Shopper Analytics Summary** page](shopper-analytics-summary-page.md):

- **Over capacity** card

- **Over capacity instances** graph

- **Footfall power hours** heatmap

You can use the Command Center if you want to also get an email notification of any violation of maximum occupancy thresholds. You do this by customizing a 
Power Automate flow template. After setting up the template, the designated user(s) will receive reminders at the frequency you set while the store occupancy 
remains above the maximum occupancy threshold.

> [!IMPORTANT]
> You must allow pop-ups in your browser to receive the email notifications (pop-up blockers must be disabled).

## Customize a Power Automate flow to send email notifications when the maximum occupancy threshold is exceeded

1. In the Command Center, under **Set new flow**, select **Flow Templates**.

    SCREEN SHOT GOES HERE
    
2. In the pop-up dialog box, enter your credentials so you can access Power Automate.

    After entering your credentials, you'll see the Power Automate flow widgets
   
    SCREEN SHOT GOES HERE
    
3. Look for the Connected Store widget. If you don't see it on your screen, select **See more templates**.

    SCREEN SHOT GOES HERE
    
    If there are issues loading the template in the web page and pop-up blockers for your web browser are disabled, select the **Trouble loading** link to go to an external Power Automate website. You may also have to enter your credentials again.
    
    SCREEN SHOT GOES HERE
    
4. Select the Connected Store widget to load the template.

    SCREEN SHOT GOES HERE

5. Select **Continue**.

    SCREEN SHOT GOES HERE

6. In the **Set Email Address** section, in the **Value** field, enter an email address. If you want the email to be sent to more than one recipient, separate each email address with a semi-colon. 

    SCREEN SHOT GOES HERE

    > [!IMPORTANT]
    > Do not edit the **Name** and **Type** fields.
    
7. In the **Set Reminder Frequency** section, in the **Value** field, enter how often you want to send email. For example, enter **15** if you want to send an email notification every 15 minutes while the maximum occupancy threshold is exceeded.

    SCREEN SHOT GOES HERE
    
    > [!IMPORTANT]
    > Do not edit the **Name** and **Type** fields.
    
8. Select ** Save** in the upper-right corner of the page.

    SCREEN SHOT GOES HERE
    
    


