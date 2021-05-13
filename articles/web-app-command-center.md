---
author: lkbryant-MSFT
description: Learn how to use the Command Center in Dynamics 365 Connected Store Preview to set up an email notification when maximum store occupancy thresholds are exceeded.
ms.author: labryan
ms.date: 11/06/2020
ms.topic: article
title: Use the Command Center in the Dynamics 365 Connected Store Preview web app to set up a maximum store occupancy notification
ms.reviewer: v-brycho
---

# Use the Command Center in the Dynamics 365 Connected Store Preview web app to set up a maximum store occupancy notification 

You can set the maximum occupancy threshold for a store in the Microsoft Dynamics 365 Connected Store Preview mobile app. When you set the **Maximum Occupancy** value, 
you'll see the following items on the [**Shopper Analytics Summary** page](shopper-analytics-summary-page.md):

- **Over capacity** card

- **Over capacity instances** graph

- **Footfall power hours** heatmap

You can use the Command Center if you also want to send an email notification when maximum occupancy thresholds are exceeded. You do this by customizing a 
Power Automate flow template. After customizing the template, the designated user(s) will receive reminders at the frequency you set while the store occupancy 
remains above the maximum occupancy threshold.

> [!IMPORTANT]
> You must allow pop-ups (pop-up blockers must be disabled) in your browser to receive the email notifications.

## Customize a Power Automate flow to send email notifications when the maximum occupancy threshold is exceeded

1. In the Command Center, under **Set new flow**, select **Flow Templates**.

    ![Flow Templates button in Command Center](media/command-center-set-new-flow.PNG "Flow Templates button in Command Center")
    
2. If this is the first flow that you've created, you'll see the **Welcome to Power Automate** dialog box. Select the appropriate country in the list, and then select **Get started**.
    
3. In the pop-up dialog box, enter your credentials so you can access Power Automate.
    
4. Look for the Connected Store widget that looks like this. 

    ![Connected Store widget](media/command-center-connected-store-widget.PNG "Connected Store widget")

    If you don't see the widget on your screen, select **See more templates**.

    ![See more templates button in the Command Center](media/command-center-see-more-templates.PNG "See more templates button in the Command Center")
    
    If there are issues loading the template in the web page, and pop-up blockers for your web browser are already disabled, select the **Trouble loading** link to go to the external Power Automate website. You may also have to enter your credentials again.
    
    ![Trouble loading link in the Command Center](media/command-center-trouble-loading-link.PNG "Trouble loading link in the Command Center")
    
    At this point, you'll see the Connected Store widget in the Power Automate website page.
    
    ![Power Automate website page with Connected Store widget](media/command-center-power-automate-website.PNG "Power Automate website page with Connected Store widget")
    
5. Select the Connected Store widget to load the template, and then select **Continue**.

    ![Continue button for Connected Store flow](media/command-center-continue-button.PNG "Continue button for Connected Store flow")

7. At this point, you'll see all the components included in the **Send alert** flow. There are many components, but you only need to set the following two items:

    - In the **Set Email Address** section, in the **Value** field, enter an email address. **Do not edit the Name and Type fields in this section.** If you want the email to be sent to more than one recipient, separate each email address with a semi-colon. 

    ![Set Email Address section of Send alert flow](media/command-center-set-email-address.PNG "Set Email Address section of Send alert flow")

    > [!TIP]
    > You can also choose to have alerts sent to a specific Microsoft Teams channel. To do this, locate the desired channel in Teams, select the **More options** (...) button to the right of the channel name, select **Get email address**, copy the email address, and then paste it into the **Value** field. 
    >
    > ![Get email address command in Microsoft Teams](media/command-center-teams-email-link.PNG "Get email address command in Microsoft Teams")
    
    - In the **Set Reminder Frequency** section, in the **Value** field, enter how often you want to send the email notification. For example, enter **15** if you want to send an email notification every 15 minutes while the maximum occupancy threshold is exceeded. **Do not edit the Name and Type fields in this section.**

    ![Set Reminder Frequency section of Send alert flow](media/command-center-set-reminder-frequency.PNG "Set Reminder Frequency section of Send alert flow")
    
8. Select **Save** in the upper-right corner of the page.

    ![Save button in the Command Center](media/command-center-save-button.PNG "Save button in the Command Center")
    
That's all you need to do to set up alerts for maximum occupancy. 

## Edit an existing Power Automate flow

1. In the Command Center, under **Manage flows**, select **My flows**.

    ![Command Center window showing Manage flows and My flows button](media/command-center-edit-flow.PNG "Command Center window showing Manage flows and My flows button")
    
2. Select the flow you want to edit, and then select **Edit**.

    ![Edit button to edit a specific flow in Command Center](media/command-center-edit-button.PNG "Edit button to edit a specific flow in Command Center")
    
    The flow appears in a collapsed format.
    
    ![Command Center window showing a collapsed flow](media/command-center-collapsed-flow.PNG "Command Center window showing a collapsed flow")
    
3. Select the module you want to edit to expand it, and then make your edits.

    ![Command Center window showing an expanded flow](media/command-center-expanded-flow.PNG "Command Center window showing an expanded flow")
    
4. Select **Save** in the upper-right corner when you're done.
    

    
## Next step

[Learn about the Shopper Analytics Summary page](shopper-analytics-summary-page.md)
    
    


