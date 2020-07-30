---
author: alissapolucha
description: Learn how to add camera skill zones (Display effectiveness, Queue management, or Shopper analytics) to Dynamics 365 Connected Store (public preview) by using the mobile app
ms.author: alissag
ms.date: 07/28/2020
ms.service: crm-online
ms.topic: article
title: Add skill zones to a camera using the Dynamics 365 Connected Store (public preview) mobile app
ms.reviewer: v-brycho
---

# Add skill zones to a camera using the Dynamics 365 Connected Store (public preview) mobile app

You can use customizable skill zones in Microsoft Dynamics 365 Connected Store (public preview) to have your camera collect physical data based on the needs of your store. You can add or update your skill zones at any time using the mobile app.

Skill zones let you specify the types of data to collect, and exactly which areas within your camera view to collect those data. You can use the mobile app to set up custom zones with one of three available skills.

|Skill|Description|Examples|
|-------------------------|-------------------------------------------------|-------------------------------------------------|
|**Display effectiveness**|	Track how your displays perform	|End caps, displays, promotions|
|**Queue management**| 	Monitor queue wait time, length, and abandonment rate|	Queues, checkouts, returns|
|**Shopper analytics**|	Understand traffic patterns into and around the store|	Store entry/exit|

For public preview, each gateway supports up to 10 zones with a maximum of 1 skill zone for each camera view. Your skill zones can have custom names and shapes (limited to four sides).

> [!NOTE]
> Skill zones don’t change what your camera sees at any time. After you create a skill zone, the camera will continue to see the entire field of view but will only track and collect data from the zones that you add. You can add or update your skill zones at any time using the mobile app.

## Create a skill zone

1.	On the **Cameras** page, select the camera you want to add a skill zone to by tapping it, and then tap the + button.

    ![Plus sign](media/skill-zone-add.png "Plus sign")
 
2.	Select one of the three available skills.

    ![Skill zone choices](media/skill-zone-choices.PNG "Skill zone choices")
 
    The zone is added to the Zone list. It shows the skill zone name, type of skill zone, and whether it’s active.

3.	Rotate your phone to Landscape mode so you have a larger screen to work with. (You may need to change your screen rotation setting to allow Landscape mode.)    
 
4.	Do the following, depending on the type of skill zone you want to add:

    - If you're adding a **Shopper analytics** skill zone, move and extend the line to align with your store entrance. Select **Flip Direction** to make sure that the blue arrow points in the direction that people walk when they are entering the store, and white arrow points in the direction people walk when exiting the store. This is important for data analytics to work correctly. If you need to start over at any point, select **Reset**.
    
    ![Rotated screen showing camera view](media/add-shopper-analytics-skill.png "Rotated screen showing camera view")
    
    - If you're adding a **Display effectiveness** skill zone, tap and drag the zone endpoints to resize the zone and move it where you want it to go. If you need to start over at any point, select **Reset**. Visit <link to another section> for tips on defining an optimal display effectiveness skill zone.
    
    ![Rotated screen showing camera view](media/add-display-effectiveness-zone.png "Rotated screen showing camera view")
    
    - If you're adding a **Queue management** skill zone, tap and drag the zone endpoints to resize the zone and move it where you want it to go, similar to what you would do for Display effectiveness. If you need to start over at any point, select **Reset**. Visit (example-of-well-shaped-queue-management-skill-zone) for tips on defining an optimal Queue management skill zone.
    
    ![Rotated screen showing camera view](media/add-queue-management-zone.png "Rotated screen showing camera view")

5.	When you’re done, tap **Done** at the bottom of the screen. When you see a pop-up message saying that your zone has been set, select **Continue**.

6.	In the next screen, make any changes to the fields to customize the skill for your store’s needs.

    ![Skill zone fields](media/skill-zone-fields.PNG "Skill zone fields")
 
    The fields change depending on which skill you choose in step 2. The following table describes the fields for each skill zone.

    |Field|	Description|	Applies to (skills)|
    |----------------|------------------------------------------------|-------------------------------------------------------|
    |**Zone Name**|Give your zone a name to easily identify it in the dashboard (for example, Holiday promotion).|- Display effectiveness<br>- Queue management<br>- Shopper analytics|
    |**Active Date Range**|Set the time frame for collecting data in the selected zone.<br><br> For the Display effectiveness skill, this is especially useful for zones where the physical location of the zone may not change but the product changes.|- Display effectiveness<br>- Queue management<br>- Shopper analytics|
    |**Engagement Threshold**|Set a dwell time threshold over which you consider people engaged in the zone.|- Display effectiveness|
    |**Direction Names**|Personalize the names of the sides of your zone to give context to the people count data.|- Display effectiveness<br>- Queue management<br>- Shopper analytics|
    |**People Count**|The number of people crossing into and/or out of a zone.|- Display effectiveness<br>- Queue management<br>- Shopper analytics|
    |**Dwell Time**|The average time spent by people in a selected zone.|- Display effectiveness|
    |**Direction**|Associates people count with the direction name of a zone side.|- Display effectiveness<br>- Queue management<br>- Shopper analytics|
    |**Direction Names**|Personalize the names of the sides of your zone to give context to the people count data.|- Shopper analytics|

7.	When you’re finished editing the skills, tap the check mark in the upper-right corner of the page.

    > [!TIP]
    > You can edit skills details or zone placement anytime by tapping the **Actions** button for the zone you want to update.
    
    ![Actions button](media/skill-zone-action-button.png "Actions button")
 
## Sort the Skills list

If you have a lot of skills on your camera, you might want to sort the list to find the skill you're looking for. To sort the Skills list:

- Select the **Sort Filter** button at the top of the skills page.

## Tips for drawing skill zones

Remember that every store is different; you’ll need to update the position or size depending on your needs.

If you want to see a specific section of your camera view, create the largest zone that you can covering the specific floor area that you are interested but not including other areas that you are not interested in. This increases the accuracy of the data collected and prevents false positives from areas you don’t want to track. Be careful placing the corners of your polygon to make sure they’re not outside the area you want to track.
 
### Example of a well-shaped Display effectiveness skill zone

The zone should be big enough to accommodate 3 people standing along each edge and focused on the area of interest. When drawing zones on the 2D image, imagine you are drawing them as if they lie on the store floor.

![Well-shaped Display effectiveness skill zone](media/skill-zone-de-good-example.png "Well-shaped Display effectiveness skill zone")
 
### Examples of Display effectiveness skill zones that aren't well-shaped

The following are some examples of poorly defined Display effectiveness skill zones as reference. In these examples, the display of interest is the ‘It’s Game Time’ display.

![Poorly shaped Display effectiveness skill zone](media/skill-zone-de-bad-example-1.png "Poorly shaped Display effectiveness skill zone")
 
> [!TIP]
> For Display effectiveness zones, make sure to extend the zone at least three feet (one meter) in front of the areas of interest.

Skill zone is too small
![Skill zone is too small](media/skill-zone-de-bad-example-2.png "Skill zone is too small")

Skill zone doesn’t fully capture area around endcap
![Skill zone doesn’t fully capture area around endcap](media/skill-zone-de-bad-example-3.png "Skill zone doesn’t fully capture area around endcap")

Skill zone too close to the edge of the camera image, doesn’t capture the right display
![Skill zone too close to the edge of the camera image, doesn’t capture the right display](media/skill-zone-de-bad-example-4.png "Skill zone too close to the edge of the camera image, doesn’t capture the right display")

Skill zone is partially blocked so people aren’t fully visible
![Skill zone is partially blocked so people aren’t fully visible](media/skill-zone-de-bad-example-5.png "Skill zone is partially blocked so people aren’t fully visible")

### Example of well-shaped Shopper analytics skill line
The line should be long enough to accommodate entire entrance. When drawing lines on the 2D image, imagine you are drawing them as if they lie on the store floor.
![Well-shaped Shopper analytics skill line](media/skill-zone-sa-good-example.png "Well-shaped Shopper analytics skill line")

### Examples of Shopper analytics skill line that isn’t well-shaped
The following are some examples of poorly defined Shopper analytics skill line.

Line not covering entire entryway on the floor
![Line not covering entire entryway on the floor](media/skill-zone-sa-bad-example-1.png "Line not covering entire entryway on the floor")

Line too high and not covering entirety of the door
![Line too high and not covering entirety of the door](media/skill-zone-sa-bad-example-2.png "Line too high and not covering entirety of the door")

### Example of well-shaped Queue management skill zone
The zone should be big enough to accommodate 3 people standing along each edge and focused on the area of interest. When drawing zones on the 2D image, imagine you are drawing them as if they lie on the store floor.

![Well-shaped Queue management skill zone](media/skill-zone-qm-good-example.png "Well-shaped Queue management skill zone")

### Examples of Queue management skill zones that isn’t well-shaped
The following are some examples of poorly defined Queue management skill zones.

Queue defined too thin
![Queue defined too thin](media/skill-zone-qm-bad-example-1.png "Queue defined too thin")

Queue extended too long
![Queue extended too long](media/skill-zone-qm-bad-example-2.png "Queue extended too long")

## Next step

[Get insights with the web app](web-app-get-insights.md)
