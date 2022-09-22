---
author: alissapolucha
description: Learn how to use Dynamics 365 Connected Spaces Preview to get insights on your store
ms.author: alissag
ms.date: 09/30/2022
ms.topic: article
title: Use Dynamics 365 Connected Spaces Preview to get insights on your store
ms.reviewer: v-bholmes
---

# Use the Analytics page in Dynamics 365 Connected Spaces Preview to get insights on your store

Microsoft Dynamics 365 Connected Spaces Preview serves as a platform to view, explore, and act on the diversity of data captured in your store. This article describes how to get insights from your store using the **Analytics** page. 

Connected Spaces supports the following camera skills: 

- Entries
- Area
- Queue
 
For a quick overview of how to get insights, scan the screens in this and other articles. 

> [!IMPORTANT]
> To use Connected Spaces, you must use a supported browser and the browser must have the most up-to-date version installed. Connected Spaces supports Chromium-based browsers (Chrome, Opera, and Edge), Firefox, and Safari. Internet Explorer is not supported. 

## Analytics page overview

The **Analytics** page, which is organized by skill (Entries, Queue, and Area), provides a sense of the store’s overall performance for configured skills. Each skill type has small cards on the left that highlight key takeaways for the configured skill and graphs on the right for each skill instance. 

![Analytics page.](media/analytics-screen-overview.JPG "Analytics page")

## Filter by date

By default, the **Analytics** page shows the last 7 days, but you can select a custom date range or choose from other pre-selected ranges by using the **Date** filter. 

![Screenshot of filter by date.](media/analytics-filter-by-date.jpg "Screenshot of filter by date")

## Filter by skill type

By default, the skill type filter shows all skill types, but you can select a skill type (Entries, Queue, or Area) in the **Skill** filter.

![Screenshot of filter by skill type.](media/analytics-filter-by-skill-type.jpg "Screenshot of filter by skill type")

## Highlight cards

Each skill type includes highlight cards with information buttons that you can hover over to get additional details.

![Information buttons.](media/analytics-information-buttons.jpg "Information buttons")

**Change in space entries.** This card highlights the sum of people that entered the space for the selected time frame. 

![Change in space entries card.](media/analytics-screen-change-store-entries.JPG "Change in space entries card")

>[!NOTE]
> If there’s insufficient data, no information is displayed in the card. This is true for all cards on the **Analytics** and other pages.

**Busiest day.** This card highlights the day of the week and date within the selected time frame that had the greatest number of people, along with the people count. 

![Busiest day card.](media/analytics-screen-busiest-day.JPG "Busiest day card")

**Largest increase in area traffic.** This card highlights the area with the largest increase in area traffic as compared to all other areas over the previous time period.  

![Largest increase in area traffic card.](media/analytics-screen-largest-increase-display-traffic.JPG "Largest increase in area traffic card")

**Largest decrease in area traffic.** This card highlights the area with the largest decrease in area traffic as compared to all other areas over the previous time period.   

![Largest decrease in area traffic card.](media/analytics-screen-largest-decrease-display-traffic.JPG "Largest decrease in area traffic card")

**Largest increase in visit time.** This card highlights the area with the largest increase in visit time as compared to all other areas over the previous time period. 

![Largest increase in visit time card.](media/analytics-screen-largest-increase-visit-time.JPG "Largest increase in visit time card")

**Largest decrease in visit time.** This card highlights the area with the largest decrease in visit time as compared to all other areas over the previous time period. 

![Largest decrease in visit time card.](media/analytics-screen-largest-decrease-visit-time.JPG "Largest decrease in visit time card")

**Change in queue traffic.** This card shows the percentage increase or decrease for queue traffic as compared to the previous time period.

![Change in queue traffic card.](media/analytics-screen-change-queue-traffic.JPG "Change in queue traffic card")

**Change in queue wait time.** This card shows the percentage increase or decrease for the queue wait time as compared to the previous time period. 

![Change in queue wait time card.](media/analytics-screen-change-queue-wait-time.JPG "Change in queue wait time card")

## Graphs on the Analytics page

To the right of the highlight cards are graphs for each skill, starting with Entries.

### Entries graphs

![Entries graphs section of Analytics page.](media/analytics-screen-overview.JPG "Entries graphs section of Analytics page")

> [!TIP]
> You can hover over the information button for any graph to get more information about the graph. You can also hover over a point in a graph to reveal details.

**Total entries across store [by time slice (day, hour)].** This graph shows the total number of people that entered the store, across all Entries zones. 

**Footfall entries power hours [by time slice (day, hour)].**  This graph shows the hourly breakdown of space entries per day.

**Footfall at each entrance [by time slice (day, hour)].** This graph shows the total number of people that entered the space, across each Entries skill, individually. 

### Area graphs

![Area graphs section of Analytics page.](media/analytics-screen-area-graphs.JPG "Area graphs section of Analytics page")

**Enters [by time slice (day, hour)].** This graph shows the number of people entering the skill zone over the time period selected.

**Visit time [by time slice (day, hour)].** This graph shows the average dwell time of the people who entered the skill zone over the time period selected.

### Queue graphs

![Queue graphs section of Analytics page.](media/analytics-screen-queue-graphs.JPG "Queue graphs section of Analytics page")

**Total enters across all queues [by time slice (day, hour)].** The total number of people who entered all queues, by day.

**Hourly queue wait time [by time slice (day, hour)].** The hourly breakdown of average queue wait times, by day for all queues.

**Queue enters by individual queues time [by time slice (day, hour)].** The total number of queue entries for each specific queue.

## Compare two sets of data for a skill type

It's helpful to be able to compare skill data from the current period to a previous period to determine trends in your space. Connected Spaces automatically does this comparison for you when you select a date range in a chart. For example, in the following chart, the blue line shows the user-selected date range, and the gray dotted line shows the previous equivalent date range.

![Screenshot showing the Current period range and the Previous period range.](media/current-previous-period.JPG "Screenshot showing the Current period range and the Previous period range")

To view just the data for the current period or the previous period, select the label (**Current period** or **Previous period**) for the data that you want to remove.

![Animation showing the current period data and the previous period data being removed from the chart.](media/compareline.gif "Animation showing current period data and the previous period data being removed from the chart")

### How is the previous period calculated?

The previous date range is the range of equivalent length in the week or weeks that immediately precede the currently selected date range. It always starts and ends on the same days of the week as the selected range. For example, if the selected range is Tuesday, February 22 through Friday, February 25, the previous date range for the comparison will be Tuesday, February 15 through Friday, February 18.

![Screenshot of a calendar showing two date ranges.](media/previous-period-calculation.JPG "Screenshot of a calendar showing two date ranges")
