---
author: alwinv
description: How Dynamics 365 Connected Spaces Preview protects data and privacy
ms.author: alwinv
ms.date: 11/02/2021
ms.topic: article
title: Data and Privacy for Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Data and privacy for Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

> [!NOTE]
> This article is provided for informational purposes only and not for the purpose of providing legal advice. We strongly recommend seeking specialist legal advice when implementing Microsoft Dynamics 365 Connected Spaces. [See Compliance and responsible use](compliance.md).

Dynamics 365 Connected Spaces Preview has three components, and each has been designed with privacy, security, and compliance in mind. 

![Illustration of retail store, Azure cloud service and Power Platorm components.](media/how-connected-spaces-works.jpg "Illustration of retail store, Azure cloud service and Power Platorm components")

- **Edge gateway** – A customer-managed Azure Stack Edge Pro (2 GPU) gateway computing device installed in the retail store that runs computer vision AI model(s) to convert video streams from existing or new cameras into inference data. The edge gateway processes video data from the in-store camera locally on the device (at the edge) and uses AI models to draw conclusions from that video footage ("inferences") without identifying individuals to generate inference data. 

- **Connected Spaces cloud service and app** – A  Software-as-a-service (SaaS) cloud service running on Azure and a Connected Spaces web app that provides insights for the retailer. The edge gateway sends the inference data to the Connected Spaces service so that it can be correlated with the retailer’s business data (for example, store business hours, camera zone name) and aggregated to generate actionable insights regarding retail operations. The Connected Spaces service saves the inference data and insight data to the Customer's Dataverse storage. Customers can then use the Connected Spaces web app to view the resulting insights data for shopper analytics, display effectiveness, and queue management insights.

- **Microsoft Dataverse storage** – Database and file storage in the customer’s Power Platform environment. All of the customer’s data is stored in Microsoft Dataverse for easy access and management.

## What data does Connected Spaces process?  

In the retail store(s), the edge gateway is used to process the following types of data:

- **Video stream** – The video stream from customers’ in-store cameras is processed in memory, in real time, on the customer's Azure Stack Edge gateway to generate inference data and is stored in the local file system temporarily while it's being processed.

- **Inference data** – This is the event data output by AI skills (models) running on the edge gateway that describe an inferred person event. Event data includes:

   - Time stamp
   
   - Event type - line crossing, zone enter or exit, zone dwell

   - Values - Crossing direction, Dwell time, Dwell frames, Orientation, Speed, Frame
   
   - Rectangle “bounding box” points, width & height - area tracked within the camera frame
   
   - Confidence score - confidence of the “bounding box” being a person

   - Camera orientation angles - ground and mapped image
   
   - Pseudonymous identifier - associated with the “bounding box”

   - Identifiers - Camera, Zone, Inference

- **Insight data** - The inference data described above is depersonalized and aggregated into event counts for every 30 seconds of time. Insight data includes:
 
   - Time stamps - for the start and end of the 30 second time window
   
   - Values over that time - entries, exits, dwells, dwell time, visits, visit time, peak occupancy, occupancy change
   
   - AI skill type - Store Traffic, Display Effectiveness, Queue Managment

   - Zone – such as "Front Entrance", "Aisle 1 display", and so on

   - Identifiers - Store, Camera, Customer AAD Tenant, Insight

> [!NOTE]
> **Every customer has the ability to choose if Video data and Inference data is uploaded to their Microsoft Dataverse cloud storage and to manage it. Go to Settings > Privacy Information to change where video is stored.**

In the Connected Spaces cloud service on Azure, the following types of data are processed at the instructions of the customer to provide the service:

- **Video data** - The Video stream data sent from the edge gateway is saved to the customer's Microsoft Dataverse cloud storage.

- **Inference data** – The Inference data sent from the edge gateway is saved to the customer's Microsoft Dataverse cloud storage.

- **Insight data** - The insight data described above is aggregated further into hourly summaries and correlated with other business data (for example, total enter events during the 9AM hour for the entire store) and then stored in the customer's Microsoft Dataverse cloud storage for viewing via the Connected Spaces web app. The customer may delete the data at any time and must delete the data in accordance with applicable legal obligations. Insight data includes: 

   - Time stamp - summarized by hour or other time interval

   - Type - Entrance, Display, Queue, Venue

   - Value sums, averages and maximums over the hour - Dwell time, Dwells, Enters, Exits, Visits, Visit time, Occupancy, Occupancy change, Over capacity

   - AI skill type - Store Traffic, Display Effectiveness, Queue Managment

   - Zone – such as "Front Entrance", "Aisle 1 display", and so on

   - Time zone info - day of year, hour of day

   - Store name - such as "Redmond store", "Seattle store", and so on

   - Identifiers - Store, Skill, Insight
 
- **Configuration data** – This is information about the retailer’s store and the edge gateway configuration used for setup and configuration of camera zones (for example, store name, paired camera IP address, camera view snapshot image, and zone skills). 

- **Telemetry data** – This is information about the health of the edge gateway, the Connected Spaces cloud service, and the Connected Spaces app. 

In Microsoft Dataverse cloud storage, the customer data is stored and can be managed by the customer. These Dataverse tables are created to store the customer data:

HyperStore - Uses Dataverse File Capacity storage, to archive copies of the data sent from the edge gateway:
- Video data (rows with names containing "1-video")
- Inference data (rows with names containing "1403-metadata")
- Insight data with 30 sec summaries (rows with names containing "1405-metadata")

> To manage retention of the archive data stored in the HyperStore table, see this article on how to [Free up storage space](https://docs.microsoft.com/en-us/power-platform/admin/free-storage-space) in Dataverse. It shows examples of how to manage file capacity using advanced queries and how to automate retention using a bulk deletion job.

HyperDocument - Uses Dataverse Database Capacity, to store the data used by the app for configuration, for analytics dashboards and for HyperStore data indexes:
- Configuration data
- Insight data (hourly summaries)
- Index data to access the HyperStore table (rows with PK value of HyperAsset or HyperTrack)

## How does Connected Spaces process data?

Dynamics 365 Connected Spaces processes data as instructed by the customer to provide the Connected Spaces solution.  

Customers use the Connected Spaces web app to configure their store. They connect cameras, draw skill zones, and configure their store settings in the web app. After the configuration is completed, video footage from the paired cameras is streamed directly to the edge gateway, installed on the customers’ premises, to create inference data using AI skills. The AI skills (models) running on customers’ premises are pre-trained "out of the box" and not trained with the customer's specific video data unless a customer specifically instructs Microsoft to do so and grants Microsoft the right to access its video feed to enhance the underlying AI skill models.

The AI skills running locally on the edge device detect and track unidentified people’s movements in the video feed based on algorithms that identify the presence of one or more humans. The algorithms generate events when a person moves in or out of designated zones in the camera’s field of view and outputs the coordinates of the person’s body into a bounding box. For each bounding box movement detected in a camera zone, the AI skills output "Inference data".

The AI data inferencing is performed locally in memory on the edge gateway near real time. This inferenced data is then sent to the Connected Spaces service for further processing and aggregation with other customer business data and configuration data to deliver insights that are accessible through the Connected Spaces web app. All of the customer data is saved to the customer's Microsoft Dataverse cloud storage. The customer's data stays in the customer's geographic region when processed by the Connected Spaces service and when stored in Microsoft Dataverse. During preview, Connected Spaces is only available to customers with AAD tenants in the UK or US geographic regions.

Customer data processed in the Connected Spaces cloud is used to provide customers with the Connected Spaces service, including by providing insights about retail locations, and also to improve and troubleshoot the Connected Spaces cloud service and other operations incident to delivering the services (for example, managing your account, internal reporting, and improving core functionality such as privacy and accessibility). The customer may delete the data at any time in their Microsoft Dataverse instance. While Dynamics 365 Connected Spaces is still in a preview phase, some privacy measures may differ from controls in place for Microsoft commercial cloud services. However, for any personal data sent to the Connected Spaces cloud service, Microsoft provides the contractual commitments required by Article 28 of the GDPR. For more information, see [Privacy and Personal Data for Microsoft Dynamics 365 and GDPR Overview](https://docs.microsoft.com/dynamics365/get-started/gdpr/).

Shoppers and employees may have privacy questions related to data collected and processed by retail stores. Connected Spaces customers can refer to the best practices outlined in our guides ([Communicate with shoppers](communication-plan.md) and [Communicate with employees](employee-plan.md)) as they consider how to effectively communicate about data used by Connected Spaces. 



