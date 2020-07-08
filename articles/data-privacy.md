---
author: alwinv
description: How Dynamics 365 Connected Store (public preview) protects data and privacy
ms.author: alwinv
ms.date: 07/08/2020
ms.service: crm-online
ms.topic: article
title: Data and Privacy for Dynamics 365 Connected Store (public preview)
ms.reviewer: v-brycho
---

# Data and privacy for Dynamics 365 Connected Store (public preview)

Microsoft Dynamics 365 Connected Store has three components, and each is designed with compliance, security, and privacy in mind. 

![Illustration of retail store, Azure cloud service and Power Platorm components](media/how-cs-works.PNG "Illustration of retail store, Azure cloud service and Power Platorm components")

- **Connected Store edge gateway** – A managed Azure Stack Edge gateway installed in the retail store that runs computer vision AI model(s) to convert camera streams from existing or new cameras into observational data sent to the cloud. The Connected Store edge gateway processes video data from the in-store camera locally on the device and makes AI data inferences without identifying or tracking individuals to generate observational data.

- **Connected Store cloud service and web app** – A  Software-as-a-service (SaaS) cloud service running on Azure and a Connected Store web app that provides insights and recommended actions for the retailer. The edge gateway sends the data inferences to the Connected Store cloud so that the observational data can be correlated with the retailer’s business data (for example, store business hours, camera zone name) to generate actionable insights regarding retail operations. Customers can then use the Connected Store web app to view this data stored in the Connected Store cloud for Shopping analytics, Display effectiveness, and Queue management insights. 

- **Connected Store mobile app** – A mobile app to provide retailers a consumer-class onboarding experience to set up the edge gateway and assist with customer configuration of cameras to deliver camera feed to the edge gateway. The mobile app provides a visual interface for the retailer to add, update, and view edge gateway and camera zone configuration (for example, zone name or AI skill to apply) via the Connected Store cloud service.


## What data does Connected Store process?  

In the retail store(s), the Connected Store edge gateway is used to process the following types of data:

- **Video stream** – The video stream from customers’ in-store cameras is processed in memory, in real time, on the Connected Store edge gateway to generate inference data. **The video data is not stored on the gateway, nor sent to Microsoft’s cloud.**

- **Inference data** – This is the event data output by AI skills (models) running on the edge gateway that describe an inferred event. Event data includes data such as a time stamp, notation about the type of event (for example "entry" or "exit" crossing line or zones), a rectangle “bounding box” that coordinates the area tracked within the camera frame, a confidence score that indicates confidence of the “bounding box” being a person, and a pseudonymous identifier associated with the “bounding box”. 

- **Camera snapshot image** – During setup and configuration, a snapshot image from an in-store camera is encoded and passed through to the Connected Store mobile app via the Connected Store cloud service. The base64 encoded image is only temporarily cached in memory (less than 2 minutes) on the Connected Store cloud so it can pass through to the Connected Store mobile app for zone configuration.
 
In the Connected Store cloud service on Azure, the following types of data are processed to provide the service:

- **Insights data** - The inference data described above is aggregated and correlated with other business data to turn into insights data that is stored in the Connected Store cloud for viewing via the Connected Store web app. Insights data includes: 

   - Time stamp - summarized by hour or other time interval

   - Value - the number over that hour

   - Measurement type - entries, exits, dwell time, occupancy

   - Aggregation type - total, average, maximum, minimum

   - Zone – such as Front Entrance, Aisle 1 display, and so on

- **Configuration data** – This is information about the retailer’s store and the Connected Store edge gateway configuration that is used for setup and configuration of camera zones (for example, store name, paired camera IP address, and zone skills). 

- **Telemetry data** – This is information about the health of the edge gateway, the Connected Store cloud service, and the Connected Store mobile app. 

- **Order data** – This is the information tied to the customer’s account and provides details around the edge hardware ordered and where it was shipped. This includes data points such as company name, shipping address, shipping status info, contact info, and device serial number.

The Connected Store mobile app and the Connected Store web app do not collect any additional information as both applications access and use data from the Connected Store cloud service. 

## How does Connected Store process data?

Dynamics 365 Connected Store processes data as instructed by the customer to provide the Connected Store solution.  

During setup, customers instruct the Connected Store mobile app to pair video streams from the customer’s in-store cameras to the Connected Store edge gateway for zone configuration of their store. After the configuration is completed, customers can stream video data from the paired cameras directly to the Connected Store edge gateway on the customers’ premises for AI inferencing using AI skills. The AI skills (models) running on customers’ premises are not trained with the video data unless a customer specifically instructs Microsoft to do so and grants Microsoft the right to access its video feed to enhance the underlying AI skill models.

The AI skills detect and track people’s movements in the video feed based on algorithms that identify the presence of one or more humans. The algorithms generate events when a person moves in or out of designated zones in the camera’s field of view and outputs the coordinates of the person’s body or head into a bounding box. For each bounding box movement detected in a camera zone, the AI skill output inference data includes the following:

- Bounding box coordinates of person’s body or head

- Event type (for example, zone entry or exit, directional line crossing)

- Pseudonymous identifier to track the bounding box 

- Confidence score for the detection 

The AI inferencing requires only images to be streamed from customers’ cameras. No video data leaves the premises and no video data is stored on the edge gateway or sent to the Connected Store cloud. The AI data inferencing is performed locally in memory on the Connected Store edge gateway without storing video footage. The data inferencing occurs near real-time. 

This inferenced data is then sent to the Connected Store cloud for further processing and aggregation with other customer business data and configuration data to deliver insights that are accessible via the Connected Store web app.  

Customer data processed in the Connected Store cloud is used to provide customers with the Connected Store service, including by providing insights about retail locations, and also to improve and troubleshoot the Connected Store cloud service and other operations incident to delivering the services (for example, managing your account, internal reporting, and improving core functionality such as privacy and accessibility). While Dynamics 365 Connected Store is still in a preview phase, some privacy measures may differ from controls in place for Microsoft commercial cloud services. However, for any personal data sent to the Connected Store cloud service, Microsoft provides the contractual commitments required by Article 28 of the GDPR.



