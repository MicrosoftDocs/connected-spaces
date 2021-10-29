---
author: alwinv
description: How Microsoft Dynamics 365 Connected Spaces Preview uses artificial intelligence technology to provide insights.
ms.author: alwinv
ms.date: 03/09/2021
ms.topic: article
title: AI and Insights for Dynamics 365 Connected Spaces Preview
ms.reviewer: v-brycho
---

# AI and insights for Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

Microsoft Dynamics 365 Connected Spaces leverages industry-leading computer vision Artificial intelligence (AI) and machine learning to provide data-driven stored-based analytics (referred to as "insights") to optimize retail operations. Connected Spaces provides retailers with: (i) simple analytics and trends on observational data generated in the retail environment; (ii) actionable insights based on multiple sources of data through machine learning and AI; and (iii) easy ways to create and manage manual and automated tasks across the retail environment.  

## How AI works to produce insights

The edge device includes computer vision skills (AI models) that detect human presence and movement from in-store camera video footage to derive data such as people count and dwell time. The derived data (or inference data) is sent to the Connected Spaces cloud to generate insights. The Connected Spaces service and web app is a multi-tenant software as a service (SaaS) that processes the data from Connected Spaces edge gateway, and correlates with other business data to generate aggregate and actionable insights for each customer.

- The computer vision AI skills goal is exclusively to detect and locate human presence in video footage and outputs a bounding box around a human body. Connected Spaces AI skills that detect people and their dwell or wait times in certain zones of the store do not attempt to detect faces or discover the identities or demographics of shoppers and other individuals at your retail location. 

- For each bounding box movement detected in a camera zone, the AI model outputs event data, including the following:

   - Bounding box coordinates of a person’s body

   - Event type (for example, zone entry or exit and directional line crossing) 

   - Pseudonymous identifier to track the bounding box 

   - Confidence score for the detection

- All of the inferencing by the AI skills are depersonalized and processed in memory on the edge gateway. This inference data is stored in Microsoft Dataverse in the customer's Microsoft Power Platform environment for the customer to manage themselves. Customers also have the option to store their video data on the Power Platform.

- The inferenced data output from the AI skills are sent to the Connected Spaces cloud. This output does not include data that could identify individuals. Data sent to the cloud includes event data and pseudonymous identifiers that are then aggregated to deliver insights from the Connected Spaces cloud service through the Connected Spaces web app. Customers also have the option to have video data sent to the cloud for QA and extensibility purposes.

The following list shows the insights that retail customers can retrieve from the above components of Connected Spaces. The insights are aggregated, and no individual shoppers are identified or tracked.

> **1. Shopper analytics.** Includes insights around footfalls and occupancy such as total footfall across the store or busiest day of the week. 

> **2. Display effectiveness.** Includes insights around shopper engagement for endcap or promotion display such as the display with longest average dwell time or total footfall across displays. 

> **3. Queue management.**  Includes insights around queue wait time and lengths such as longest queue across the store or average wait time across all queues. 


