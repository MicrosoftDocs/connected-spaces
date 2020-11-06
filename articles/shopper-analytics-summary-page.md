---
author: lkbryant-MSFT
description: Learn how to view the Shopper analytics summary page in the Dynamics 365 Connected Store Preview web app to get insights on your store
ms.author: labryan
ms.date: 11/06/2020
ms.service: crm-online
ms.topic: article
title: View the Shopper analytics summary page in the Dynamics 365 Connected Store Preview web app
ms.reviewer: v-brycho
---

# View the Shopper analytics summary page in the Dynamics 365 Connected Store Preview web app

You can use the [**Analytics** page](web-app-get-insights.md) in the Microsoft Dynamics 365 Connected Store Preview web app to get insights on your retail store. The **Analytics** page includes insights for the Shopper analytics, Display effectiveness, and Queue management camera skill zones. This article focuses on the summary page for the Shopper analytics skill zone. 

## View the Shopper analytics summary page

To view the **Shopper analytics summary** page, select the blue arrow to the right of the skill in the **Analytics** page. 

![Blue arrow to select to see a summary page](media/analytics-45.PNG "Blue arrow to select to see a summary page")

To go back to the **Analytics** page from the summary page, select from the breadcrumb at the top of the page.

![Breadcrumb to select to go back to the Analytics page](media/analytics-46.PNG "Breadcrumb to select to go back to the Analytics page")

## The Shopper analytics summary page

The **Shopper analytics summary** page includes insights related to entry trends, patterns, changes, anomalies at store 
entries/exits, and over capacity (determined by the [**Maximum Occupancy** setting in the mobile app](mobile-app-create-store.md)). This page shows a view of the performance of all Shopper analytics zones. You can explore how many people visited the store during a given timeframe, categorized by entrance.

![Shopper analytics summary page](media/analytics-18.PNG "Shopper analytics summary page")

## Highlights banner

The banner at the top of the page highlights the key takeaways and comparisons. The first two cards, **Store entries** and **Busiest day**, are carried over from the [**Analytics** page](web-app-get-insights.md). 

**Least busy day**. This card highlights the day and date within the selected time frame that had the least number of people, 
along with the people count. 

![Least busy day card](media/analytics-19.PNG "Least busy day card")

The subscript in the card describes the absolute change in this value for the current time frame compared to average entries across all 
displays during the selected time frame. The triangle to the left of the subscript indicates the difference in entries for the 
highlighted day, compared to the daily average entries during the selected time frame. 

**Busiest entrance.** This card highlights the name and corresponding value of the Shopper analytics zone that received the greatest 
entries for the selected time frame. 

![Busest entrance card](media/analytics-20.PNG "Busiest entrance card")

The subscript in the card describes the absolute change in this value for the current time frame compared to the previous time frame of equal duration. The triangle to the left of the subscript indicates whether this change was positive or negative. 

**Least busy entrance.** This card highlights the name and corresponding value of the Shopper analytics zone that received the least 
entries for the selected time frame. 

![Least busy entrance card](media/analytics-21.PNG "Least busy entrance card")

The subscript in the card describes the absolute change in this value for the current time frame compared to the previous time frame of equal duration. The triangle to the left of the subscript indicates whether this change was positive or negative. 

**Over capacity.** This card highlights the number of instances for which the store occupancy exceeds the **Maximum Occupancy** value. The **Maximum Occupancy** value is set in the mobile app during store configuration. For example, if the **Maximum Occupancy** value for the store is set to 320 people (shown in the subscript in the card), the card reports the number of instances during the selected time frame for which the store occupancy was greater than 320 people. In the following example, there were 18 such instances.

![Over capacity card](media/analytics-over-capacity-card.PNG "Over capacity card")

> [!NOTE]
> If you haven't [set a **Maximum Occupancy** value in the mobile app](mobile-app-create-store.md), you'll see a placeholder instead of the **Over capacity** card. The placeholder prompts you to download or go to the mobile app to set a **Maximum Occupancy** value. After you configure the **Maximum Occupancy** value, you'll see a tool tip in the web app that prompts you to [set up alerts and notifications in the Command Center](web-app-command-center.md). 

## Graphs

There are several graphs on this page:

- **Total store entries per entrance by [time slice (day, hour)]**. This graph shows total store entries according to the Shopper analytics zone. 

    ![Total store entries per entrance graph](media/analytics-total-footfall-entrances.PNG "Total store entries per entrance graph")

- **Over capacity instances by [time slice (day, hour)]**. This graph shows trends in instances of over capacity across time for the selected time frame. In the example shown in the screen shot below, most instances of over capacity occurred on Friday. The gray dotted line reflects the average number of over-capacity instances for the selected time frame. 

    ![Over capacity instances graph](media/analytics-over-capacity-instances.PNG "Over capacity instances graph")

    > [!NOTE]
    > If you haven't [set a **Maximum Occupancy** value in the mobile app](mobile-app-create-store.md), you'll see a placeholder instead of the **Over capacity instances** graph. The placeholder prompts you to download or go to the mobile app to set a value. After you configure the **Maximum Occupancy** value, you'll see a tool tip in the web app that prompts you to [set up alerts and notifications in the Command Center](web-app-command-center.md). 

    You can hover over data to reveal more details.

    ![Over capacity instances details](media/analytics-over-capacity-instances-details.PNG "Over capacity instances details")

- **Footfall power hours**. This heat map identifies patterns in over-capacity instances across day and time. In the following example, using a weekly time frame view (set in the date picker), you can identify which hours exceeded the maximum occupancy threshold, and then make any necessary adjustmens to schedule and staffing.

    ![Footfall power hours](media/analytics-footfall-power-hours.PNG "Footfall power hours")

    > [!NOTE]
    > If you haven't [set a **Maximum Occupancy** value in the mobile app](mobile-app-create-store.md), you'll see a placeholder instead of the **Footfall power hours** heatmap. The placeholder prompts you to download or go to the mobile app to set a value. After you configure the **Maximum Occupancy** value, you'll see a tool tip in the web app that prompts you to [set up alerts and notifications in the Command Center](web-app-command-center.md). 
    
    You can hover over data to reveal more details.

    ![Footfall power hours details](media/analytics-footfall-power-hours-details.PNG "Footfall power hours details")

- **Total entries at *Entrance x* - enters**. You can view trends for individual zones in these line graphs (for example, **Total entries at North - enters**).

    ![Total entries at Entrance x example](media/analytics-footfall-entrance-x.PNG "Total entries at Entrance x example")

    To see data for each individual entrance, hover over the desired data in the graph.

    ![Data for individual entrance](media/analytics-23.PNG "Data for individual entrance")

## Next steps

Learn about these web app pages:

[Analytics page](web-app-get-insights.md)<br>
[Display effectiveness summary page](display-effectiveness-summary-page.md)<br>
[Display effectiveness details page](display-effectiveness-details-page.md)<br>
[Queue management summary page](queue-management-summary-page.md)<br>
[Queue management details page](queue-management-details-page.md)
