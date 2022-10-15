---
author: vhorvathms
description: How Microsoft Dynamics 365 Connected Spaces Preview uses artificial intelligence technology to provide insights.
ms.author: vhorvath
ms.date: 10/05/2022
ms.topic: article
title: AI and Insights for Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# AI and insights for Dynamics 365 Connected Spaces Preview

Microsoft Dynamics 365 Connected Spaces Preview leverages industry-leading computer vision Artificial intelligence (AI) and machine learning to provide data-driven stored-based analytics (referred to as "insights") to optimize your space operations. Connected Spaces Preview provides: (i) simple analytics and trends on observational data generated in the space environment; (ii) actionable insights based on multiple sources of data through machine learning and AI; and (iii) easy ways to create and manage manual and automated tasks across the retail environment.  

## How AI works to produce insights

The edge device includes computer vision skills (AI models) that detect human presence and movement from in-store camera video footage to derive data such as people count and dwell time. The derived data (or inference data) is sent to the Connected Spaces cloud to generate insights. The Connected Spaces service and web app is a multi-tenant software as a service (SaaS) that processes the data from the Connected Spaces edge gateway, and correlates with other business data to generate aggregate and actionable insights for each customer.

- The computer vision AI skills goal is exclusively to detect and locate human presence in video footage and outputs a bounding box around a human body. Connected Spaces AI skills that detect people and their dwell or wait times in certain zones of the store do not attempt to detect faces or discover the identities or demographics of shoppers and other individuals at your retail location. 

- For each bounding box movement detected in a camera zone, the AI model outputs event data, including the following:

   - Bounding box coordinates of a person’s body

   - Event type (for example, zone entry or exit and directional line crossing) 

   - Pseudonymous identifier to track the bounding box 

   - Confidence score for the detection

- Inferencing by the AI skills of video footage occurs locally in memory on the edge gateway. This inference data does not include data that could identify individuals. Customers have the option to store and manage their video data and derived inference data in Microsoft Dataverse in the customer's Power Platform environment.

- The inferenced data output from the AI skills is depersonalized and aggregated into insights data, which is sent to the Connected Spaces cloud service. In the cloud, insights data is aggregated further into hourly summaries and correlated with other business data and then stored in the customer's Microsoft Dataverse cloud storage for viewing via the Connected Spaces web app. 

The following list displays the insights that retail customers can retrieve from the above components of Connected Spaces. The insights are aggregated, so end users  are not identifiable or tracked. 

|Skill|Description|Examples|
|-----------------|-----------------------------------------------|-------------------------------------------------|
|Area|Track how your displays and areas of interest perform |End caps, displays, promotions, breakrooms, lobbies |
|Queue|Monitor queue wait time, length, and abandonment rate |Queues, checkouts, returns|
|Entries|Understand traffic patterns in your space |Space entry/exit |
