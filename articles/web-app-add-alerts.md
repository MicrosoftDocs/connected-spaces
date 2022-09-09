# Add alerts in the Dynamics 365 Connected Spaces Preview web app

You can add alerts in the Dynamics 365 Connected Spaces Preview web app to:

- Monitor trends and patterns across your physical space in near real time
- Improve customer engagement
- Optimize staffing
- Save time

You can create alerts for skills (pre-built AI models) after [adding those skills](cameras-add-skills.md) in the web app. Connected Spaces Preview includes alerts for two types of skills: queue and area

The following table shows which alerts are available for each skill.

|Skill|Image|Skill description|Alert type|
|-----------|--------------------------------|----------------------------------|--------------------------------|
|Queue|![Illustration of queue skill.](media/queue-skill.JPG "Illustration of queue skill")|Monitor queue wait time and queue lengths to improve the experience and provide informed insights for employee shift management.|- Queue wait time exceeds maximum<br>-Queue length exceeds maximum|
|Area|![Illustration of area skill.](media/area-skill.JPG "Illustration of area skill")|Create the real-world equivalent of the digital customer engagement funnel for areas and promotions. This capability allows space managers to measure the effectiveness of areas in their space.|Dwell time at display exceeds threshold|

> [!NOTE]
> You must have a Microsoft Teams and an Outlook license to use alerts in Connected Spaces Preview.

## Enable alerts

Connected Spaces uses Microsoft Power Automate as the alert delivery platform, which means that you must enable alerts in  Power Automate before you can add them in Connected Spaces. You can open Power Automate directly from Connected Spaces Preview.

> [!NOTE]
> You only need to enable alerts one time through Power Automate. After enabling alerts, all alert management happens in the Connected Spaces web app. 

1. In the web app, on the left side of the screen, select **Alerts**, and then select **Add alert**.

    ![Screenshot highlighting Alerts command and Add alert button.](media/alerts-add-alert.JPG "Screenshot highlighting Alerts command and Add alert button")

2. In the **Enable alerts** dialog box, select **Go to Power Automate**. 

    ![Screenshot highlighting Go to Power Automate button.](media/alerts-go-to-power-automate.JPG "Screenshot highlighting Go to Power Automate button")
    
3. Sign in with your work or organization account.

4. In the Power Automate screen, Microsoft Dataverse will automatically be connected for you. If you have Teams and Outlook licenses, those apps should also be connected for you. If you need to connect them manually, at the bottom of the screen, select the **More info** (three dots) button next to each source, and then sign into the apps to connect them. Select **Continue** when you're ready to move forward.

    ![Screenshot of Power Automate screen showing sources.](media/alerts-configure-sources.JPG "Screenshot of Power Automate screen showing sources")
    
5. In the next Power Automate screen, select the down arrow in the **Team** field. The Team ID will automatically be filled in when you do this. Select **Save** in the upper-right corner of the screen when you're done.

    ![Screenshot of Power Automate screen with Teams and Email fields.](media/alerts-configuration.JPG "Screenshot of Power Automate screen with Teams and Email fields")

## Add an alert

1. In the Connected Spaces web app, on the left side of the screen, select **Alerts**, and then on the right side of the screen, select the type of alert you want to create from the **Alert type** list.

    ![Screenshot highlighting Alert type list.](media/alerts-alert-type.JPG "Screenshot highlighting Alert type list")
    
2. In the **Add alert** section:

    1. Select the skill name.
    2. Select your threshold (people or minutes).
    3. Select the send location (Teams or Outlook).
    4. Enter your recipient information (Outlook email or Teams email address). If you want to add more than one email address, separate the addresses with a semi-colon.
    5. Select **Add**.

        ![Screenshot highlighting Add alert section.](media/alerts-fill-in-fields.JPG "Screenshot highlighting Add alert section")
        
## Edit an existing alert

1. In the web app, on the left side of the screen, select **Alerts**, and then under **Actions**, select the **Edit** (pencil) button. 

    ![Screenshot highlighting Edit button.](media/alerts-edit-button.JPG "Screenshot highlighting Edit button")

2. Under **Edit alert** on the right side of the screen, make your changes.

    ![Screenshot highlighting Edit alert section for changes.](media/alerts-edit-alert.JPG "Screenshot highlighting Edit alert section for changes")

3. Select **Save** when you're done.

## Delete an alert

1. In the web app, on the left side of the screen, select **Alerts**, and then under **Actions**, select the **More info** (three dots) button. 

    ![Screenshot highligting More info (three dots) button.](media/alerts-delete-alert.JPG "Screenshot highligting More info (three dots) button")
    
2. Select **Delete**. 

3. Confirm the deletion.
