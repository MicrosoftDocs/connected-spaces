---
author: alissapolucha
description: Learn how to add camera skill zones (Display effectiveness, Queue management, or Shopper analytics) to Dynamics 365 Connected Store Preview by using the mobile app.
ms.author: alissag
ms.date: 10/15/2020
ms.service: crm-online
ms.topic: article
title: Add skill zones to a camera using the Dynamics 365 Connected Store Preview mobile app
ms.reviewer: v-brycho
---

# Add skill zones to a camera using the Dynamics 365 Connected Store Preview mobile app

You can use customizable skill zones in Microsoft Dynamics 365 Connected Store Preview to have your camera collect physical data based on the needs of your store. You can add or update your skill zones at any time using the mobile app.

Skill zones let you specify the types of data to collect, and exactly which areas within your camera view to collect those data. You can use the mobile app to set up custom zones with one of three available skills.

|Skill|Description|Examples|
|-------------------------|-------------------------------------------------|-------------------------------------------------|
|**Display effectiveness**|	Track how your displays perform	|End caps, displays, promotions|
|**Queue management**| 	Monitor queue wait time, length, and abandonment rate|	Queues, checkouts, returns|
|**Shopper analytics**|	Understand traffic patterns into and around the store|	Store entry/exit|

For the preview, each gateway supports up to 10 zones with a maximum of 1 skill zone for each camera view. Your skill zones can have custom names and shapes (limited to four sides).

> [!NOTE]
> Skill zones don't change what your camera sees at any time. After you create a skill zone, the camera will continue to see the entire field of view but will only track and collect data from the zones that you add. You can add or update your skill zones at any time using the mobile app.

## Create a skill zone

1.	On the **Cameras** page, select the camera you want to add a skill zone to by tapping it, and then tap the + button.

    ![Plus sign](media/skill-zone-add.png "Plus sign")
 
2.	Select one of the three available skills.

    ![Skill zone choices](media/skill-zone-choices.PNG "Skill zone choices")
 
    The zone is added to the Zone list. It shows the skill zone name, type of skill zone, and whether it's active.

3.	Rotate your phone to Landscape mode so you have a larger screen to work with. (You may need to change your screen rotation setting to allow Landscape mode.)    
 
4.	Do the following, depending on the type of skill zone you want to add:

    - If you're adding a **Shopper analytics** skill zone, move and extend the line to align with your store entrance. Select **Flip Direction** to make sure that the blue arrow points in the direction that people walk when they are entering the store, and white arrow points in the direction people walk when exiting the store. This is important for data analytics to work correctly. If you need to start over at any point, select **Reset**.
    
    ![Rotated screen showing Shopper analytics camera view](media/add-shopper-analytics-skill.png "Rotated screen showing Shopper analytics camera view")
    
    - If you're adding a **Display effectiveness** skill zone, tap and drag the zone endpoints to resize the zone and move it where you want it. If you need to start over at any point, select **Reset**. See [Tips for drawing skill zones](mobile-app-add-camera-skill-zones.md#tips-for-drawing-skill-zones).
    
    ![Rotated screen showing Display effectiveness camera view](media/add-display-effectiveness-zone.png "Rotated screen showing Display effectiveness camera view")
    
    - If you're adding a **Queue management** skill zone, tap and drag the zone endpoints to resize the zone and move it where you want it. If you need to start over at any point, select **Reset**. See [Tips for drawing skill zones](mobile-app-add-camera-skill-zones.md#tips-for-drawing-skill-zones).
    
    ![Rotated screen showing Queue management camera view](media/add-queue-management-zone.png "Rotated screen showing Queue management camera view")

5.	When you're done, tap **Done** at the bottom of the screen. When you see a pop-up message saying that your zone has been set, select **Continue**.

6.	In the next screen, make any changes to the fields to customize the skill for your store's needs.

    ![Skill zone fields](media/skill-zone-fields1.PNG "Skill zone fields")
 
    The fields change depending on which skill you choose in step 2. The following table describes the fields for each skill zone.

    |Field|	Description|	Applies to (skills)|
    |----------------|------------------------------------------------|-------------------------------------------------------|
    |**Active**/**Inactive** slider|Use the **Active**/**Inactive** slider to turn the skill on or off. The skill will only collect data when the slider is in the **Active** position. |- Display effectiveness<br>- Queue management<br>- Shopper analytics| 
    |**Skill Name**|Give your zone a name to easily identify it in the dashboard (for example, **Holiday promotion**).|- Display effectiveness<br>- Queue management<br>- Shopper analytics|       
    |**Direction Names**|Personalize the names of the sides of your zone to give context to the people count data.|- Display effectiveness<br>- Queue management<br>|
    |**Advanced Features > People Count**|The number of people crossing into and/or out of a zone.|- Display effectiveness<br>- Queue management<br>- Shopper analytics|
    |**Advanced Features > Dwell Time**|The average time spent by people in a selected zone.|- Display effectiveness|
    |**Advanced Features > Direction**|Associate the people count with the direction name of a zone side.|- Display effectiveness<br>- Queue management|    

7.	When you're finished editing the skills, tap the check mark in the upper-right corner of the page.

    > [!TIP]
    > You can edit, duplicate, or delete a skill at any time by tapping the **Actions** button for the skill you want to update.<br><br>**Duplicating** a skill copies the skill type, drawing, and details to a new record. You can then make edits to the skill and save.<br><br>**Deleting** a skill will permanently remove it from Azure Stack Edge Pro (2 GPU), the mobile app, and all collected data in the dashboards. This information cannot be recovered. If you're unsure about deleting a skill, change the skill status to **Inactive** instead.
    
    ![Actions button](media/skill-zone-action-button-2.PNG "Actions button")
 
## Sort the Skills list

If you have a lot of skills on your camera, you might want to sort the list to find the skill you're looking for. To sort the Skills list:

- Select the **Sort Filter** button at the top of the skills page.

## Tips for drawing skill zones

Remember that every store is different; you'll need to update the position or size depending on your needs.

If you want to see a specific section of your camera view, create the largest zone that you can, covering the specific floor area that you're interested in but not including other areas that you're not interested in. This increases the accuracy of the data collected and prevents false positives from areas you don't want to track. Be careful when placing the corners of your polygon, to make sure they're not outside the area you want to track.
 
### Example of a well-shaped Display effectiveness skill zone

The zone should be big enough to accommodate three people standing along each edge and focused on the area of interest. When drawing zones on the 2D image, imagine you're drawing them as if they lie on the store floor.

![Well-shaped Display effectiveness skill zone](media/skill-zone-de-good-example.png "Well-shaped Display effectiveness skill zone")
 
### Examples of Display effectiveness skill zones that aren't well-shaped

The following examples show poorly shaped **Display effectiveness** skill zones. In these examples, the display of interest is the **It's Game Time** display.

![Poorly shaped Display effectiveness skill zone](media/skill-zone-de-bad-example-1.png "Poorly shaped Display effectiveness skill zone")
 
> [!TIP]
> For **Display effectiveness** zones, make sure to extend the zone at least three feet (one meter) in front of the areas of interest.

**Skill zone is too small.**

![Skill zone is too small](media/skill-zone-de-bad-example-2.png "Skill zone is too small")

**Skill zone doesn't fully capture the area around the end cap.**

![Skill zone doesn't fully capture the area around end cap](media/skill-zone-de-bad-example-3.png "Skill zone doesn't fully capture the area around end cap")

**Skill zone is too close to the edge of the camera image and doesn't capture the right display.**

![Skill zone is too close to the edge of the camera image and doesn't capture the right display](media/skill-zone-de-bad-example-4.png "Skill zone is too close to the edge of the camera image and doesn't capture the right display")

**Skill zone is partially blocked, so people aren't fully visible.**

![Skill zone is partially blocked, so people aren't fully visible](media/skill-zone-de-bad-example-5.png "Skill zone is partially blocked, so people aren't fully visible")

### Example of a well-shaped Shopper analytics skill line

The line should be long enough to accommodate the entire entrance. When drawing lines on the 2D image, imagine you're drawing them as if they lie on the store floor.

![Well-shaped Shopper analytics skill line](media/skill-zone-sa-good-example.png "Well-shaped Shopper analytics skill line")

### Examples of Shopper analytics skill lines that aren't well-shaped

The following examples show poorly defined **Shopper analytics** skill lines.

**Line doesn't cover the entire entry way on the floor.**

![Line doesn't cover the entire entry way on the floor](media/skill-zone-sa-bad-example-1.png "Line doesn't cover the entire entry way on the floor")

**Line is too high and doesn't cover the entirety of the door.**

![Line is too high and doesn't cover the entirety of the door](media/skill-zone-sa-bad-example-2.png "Line is too high and doesn't cover the entirety of the door")

### Example of well-shaped Queue management skill zone

The zone should be big enough to accommodate three people standing along each edge and focused on the area of interest. When drawing zones on a 2D image, imagine you're drawing them as if they lie on the store floor.

![Well-shaped Queue management skill zone](media/skill-zone-qm-good-example.png "Well-shaped Queue management skill zone")

### Examples of Queue management skill zones that aren't well-shaped

The following examples show poorly defined **Queue management** skill zones.

**Queue defined is too thin.**

![Queue defined is too thin](media/skill-zone-qm-bad-example-1.png "Queue defined is too thin")

**Queue is extended too long.**

![Queue is extended too long](media/skill-zone-qm-bad-example-2.png "Queue is extended too long")

## Next step

[Get insights with the web app](web-app-get-insights.md)
