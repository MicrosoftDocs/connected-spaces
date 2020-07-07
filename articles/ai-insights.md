---
author: alwinv
description: AI and Insights
ms.author: alwinv
ms.date: 07/08/2020
ms.service: crm-online
ms.topic: article
title: AI and Insights
ms.reviewer: v-brycho
---

# AI and Insights

Microsoft Dynamics 365 Connected Store leverages the industry-leading computer vision Artificial intelligence (AI) technology for people detection to provide actionable insights regarding retail operations.  Connected Store provides retailers with: (i) simple analytics and trends on observational data generated in the retail environment; (ii) actionable insights based on multiple sources of data through machine learning and AI; and (iii) easy ways to create and manage manual and automated tasks across the retail environment.  

## How AI works to produce insights

The Connected Store Edge  Gateway includes computer vision AI skills (models) that detect human presence and movement from in-store camera video footage to derive data such as people count and dwell time. The derived data is sent to the Connected Store Cloud to generate observational data and insights. The Connected Store cloud service and web app is a multi-tenant SaaS that processes the observational data from Connected Store Edge gateway, and correlates with other business data to generate aggregate and actionable insights for each tenant.

- The computer vision AI skills goal is exclusively to detect and locate human presence in video footage and outputs a bounding box around a human body. Connected Store AI skills do not attempt to detect faces or discover the identities or demographics of shoppers and other individuals at your retail location. 

- For each bounding box movement detected in a camera zone, the AI model outputs event data including the following:

   - Bounding box coordinates of a person’s body

   - Event type (for example, zone entry or exit and directional line crossing) 

   - Pseudonymous identifier to track the bounding box 

   - Confidence score for the detection

- All the inferencing by the AI skills are processed in memory on the Edge Gateway without writing to disks so that no video footage is stored or sent to the cloud.

- The inferenced data output from the AI skills are sent to the Connected Store Cloud. This output does not include data that directly identifies individuals. Data sent to the cloud includes event data and pseudonymous identifiers that are then aggregated to deliver insights from the Connected Store Cloud service through the Connected Store web app.

The following list shows the insights that retail customers can retrieve from the above components of Connected Store. The insights are aggregated, and no individual shoppers are identified or tracked.

> **1. Shopper analytics.** Includes insights around footfalls and occupancy such as total footfall across the store or busiest day of the week. 

> **2. Display effectiveness.** Includes insights around shopper engagement for endcap or promotion display such as most engaging display, and total footfall across displays. 

> **3. Queue management.**  Includes insights around queue wait time and lengths such as longest queue across the store, and average wait time across all queues. 


