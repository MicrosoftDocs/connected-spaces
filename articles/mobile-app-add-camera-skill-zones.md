

# Add camera skill zones to a store by using the Dynamics 365 Connected Store mobile app

You can use customizable skill zones to have your camera collect physical data based on the needs of your store. You can set up 
custom zones with one of three available skills:

|Skill|Description|Examples|
|-------------------------|-------------------------------------------------|-------------------------------------------------|
|Display effectiveness|	Track how your displays perform	|End caps, displays, promotions|
|Shopper analytics| 	Monitor queue wait time, length, and abandonment rate|	Queues, checkouts, returns|
|Queue management|	Understand traffic patterns into and around the store|	Store entry/exit, aisles|

You can add one skill zone per camera view. Your skill zones can have custom names and shapes (limited to four sides).

> [!NOTE]
> Skill zones don’t change what your camera sees at any time. After you create a skill zone, the camera will continue to see the entire field of view but will only track and collect data from the zones that you add. You can add or update your skill zones at any time using the mobile app.

## Create a skill zone

1.	On the **Cameras** page, select the camera you want to add a skill zone to by tapping it, and then tap the + button.

    ![xxx](media/xxx.PNG "xxx")
 
2.	Select one of the three available skills.

    ![xxx](media/xxx.PNG "xxx")
 
    The zone is added to the Zone list. It shows the skill zone name, type of skill zone, and whether it’s active or not.

3.	Rotate your phone to Landscape mode so you have a larger screen to work with. (You may need to change your screen rotation setting allow Landscape mode.)

    ![xxx](media/xxx.PNG "xxx")
 
4.	The new zone appears in the middle of the screen. Tap and drag the zone to move it where you want it.

5.	To change the size of the zone, tap and drag the corners.

6.	When you’re done, tap the screen, and then tap **Edit Skills Details** at the bottom of the screen. 

7.	Make changes to the fields to customize the skill for your store’s needs.

    ![xxx](media/xxx.PNG "xxx")
 
    The fields change depending on which skill you choose in step 2. The following table describes the fields for each skill zone.

    |Field|	Description|	Applies to (skills)|
    |----------------|------------------------------------------------|-------------------------------------------------------|
    |**Zone Name**|Give your zone a name to easily identify it in the dashboard (for example, Holiday promotion).|- Display effectiveness<br>- Queue management<br>- Store traffic|
    |**Active Date Range**|Set the time frame for collecting data in the selected zone.<br><br>For the display effectiveness skill, this is especially useful for zones where the physical location of the zone may not change but the product changes.|- Display effectiveness<br>- Queue management<br>- Store traffic|
    |**Engagement Threshold**|Set a dwell time threshold over which you consider people engaged in the zone.|- Display effectiveness|
    |**Direction Names**|Personalize the names of the sides of your zone to give context to the people count data.|- Display effectiveness<br>- Queue management<br>- Store traffic|
    |**People Count**|The number of people crossing into and/or out of a zone.|- Display effectiveness<br>- Queue management<br>- Store traffic|
    |**Dwell Time**|The average time spent by people in a selected zone.|- Display effectiveness|
    |**Direction**|Associates people count with the direction name of a zone side.|- Display effectiveness<br>- Queue management<br>- Store traffic|
    |**Direction Names**|Personalize the names of the sides of your zone to give context to the people count data.|- Store traffic|

8.	When you’re finished editing the skills, tap the check mark in the upper-right corner of the page.

    > [!TIP]
    > You can edit skills details or zone placement anytime by tapping the Actions  button for the zone you want to update.
    
    ![xxx](media/xxx.PNG "xxx")
 
## Tips for drawing skill zones

Remember that every store is different; you’ll need to update the position or size depending on your needs.

If you want to see a specific section of your camera view, create a small, selective zone for it. This increases the accuracy of the data collected and prevents false positives from areas you don’t want to track. Be careful placing the corners of your polygon to make sure they’re not outside the area you want to track.
 
### Example of a well-shaped zone

This zone is small and focused on the area of interest:

![xxx](media/xxx.PNG "xxx")
 
### Example of a zone that isn’t well-shaped

The corners of this zone will capture data from the side aisles instead of the focus area—the display.

![xxx](media/xxx.PNG "xxx")
 
> [!TIP]
> For display effectiveness zones, make sure to extend the zone at least three feet (one meter) in front of the areas of interest.

