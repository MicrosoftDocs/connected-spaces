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

- **Connected Store Edge Gateway** – A managed Azure Stack Edge gateway installed in the retail store that runs computer vision AI model(s) to convert camera streams from existing or new cameras into observational data sent to the cloud. The Connected Store Edge gateway processes video data from the in-store camera locally on the device and makes AI data inferences without identifying or tracking individuals to generate observational data.

- **Connected Store Cloud Service and Web application** – A  Software-as-a-service (SaaS) cloud service running on Azure and a Connected Store web application that  provides insights and recommended actions for the retailer. The Edge Gateway sends the data inferences to the Connected Store Cloud so that the observational data can be correlated with the retailer’s business data (e.g. store business hours, camera zone name) to generate actionable insights regarding retail operations.  Customers can then use the Connected Store Web application to view this data stored in the Connected Store Cloud for shopping analytics, display effectiveness and queue management insights. 

- **Connected Store Mobile application** – A mobile app to provide retailers a consumer-class onboarding experience to setup the edge gateway and  assist customers’ configuration of cameras to deliver camera feed to the edge gateway. The mobile app provides a visual interface for the retailer to add, update and view Edge Gateway and camera zone configuration (e.g. zone name or AI skill to apply) via accessing the Connected Store Cloud service.


## What data does Connected Store process?  

In the retail store(s), the Connected Store Edge Gateway is used to process the following types of data:

- **Video stream** – The video stream from customers’ in-store cameras is processed in memory, in real time, on the Connected Store Edge Gateway to generate Inference data. **The video data is not stored on the gateway, nor sent to Microsoft’s cloud.**

- **Inference data** – This is the event data output by AI skills (models) running on the Edge Gateway that describe an inferred event. Event data includes data such as a time stamp, notation about the type of event (e.g. "entry" or "exit" crossing line or zones), a rectangle “bounding box” that coordinates the area tracked within the camera frame, a confidence score that indicates confidence of the “bounding box” being a person, and a pseudonymous identifier associated with the “bounding box”. 

- **Camera snapshot image** – During set up and configuration, a snapshot image from an in-store camera is passed through to the Connected Store Mobile app  via [IoT Hub direct invoke method](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods) on Connected Store Cloud service. No image(s) are cached on the mobile app or Edge Gateway or sent to the cloud. 
 
In the Connected Store Cloud service on Azure, the following types of data are processed to provide the service:

- **Insights data** - The inference data described above is aggregated and correlated with other business data to turn into insights data that is stored in the Connected Store Cloud for viewing via the Connected Store web app. Insights data includes: 

   - Time stamp - summarized by hour or other time interval

   - Value - the number over that hour

   - Measurement type - entries, exists, dwell time, occupancy

   - Aggregation Type - total, average, maximum, minimum

   - Zone – such as Front Entrance, Isle 1 display, etc.

- **Configuration data** – This is information about the retailer’s store and the Connected Store Edge Gateway configuration that is used for setup and configuration of camera zones (e.g. store name, paired camera IP address and zone skills). 

- **Telemetry data** – This is information about the health of the Edge Gateway, the Connected Store Cloud Service, and the Connected Store mobile application. 

- **Order data** – This is the information tied to the customer’s account and provides details around the Edge hardware ordered and where it was shipped.  This includes data points such as company name, shipping address, shipping status info, contact info, and device serial number.

The Connected Store Mobile app and the Connected Store Web application do not collect any additional information as both applications access and use data from the Connected Store Cloud service. 

## How does Connected Store process data?

Microsoft Dynamics 365 Connected Store processes data as instructed by the customer to provide the Connected Store solution.  

During setup, customers instruct the Connected Store Mobile app to pair video streams from the customer’s in-store cameras to the Connected Store Edge Gateway for zone configuration of their store. After the configuration is completed, customers can stream video data from the paired cameras  directly to the Connected Store Edge Gateway on customers’ premises for AI inferencing using AI skills. The AI skills (models) running on customers’ premises are not trained with the video data unless a customer specifically instructs Microsoft to do so and grants Microsoft the right to access its video feed to enhance the underlying AI skill models.

The AI skills detect and track people’s movements in the video feed based on algorithms that identify the presence of one or more humans. The algorithms generate events when a person moves in or out of designated zones in the camera’s field of view and outputs the coordinates of the person’s body into a bounding box. For each bounding box movement detected in a camera zone, the AI skill output inference data including the following:

- Bounding box coordinates of person’s body

- Event type (e.g. zone entry or exit, directional line crossing)

- Pseudonymous identifier to track bounding box 

- Confidence score for the detection 

The AI inferencing requires only images to be streamed from customers’ cameras.  No video data leaves the premises and no video data is stored on the Edge Gateway  or sent to the Connected Store Cloud. The AI data inferencing is performed locally in-memory on the Connected Store Edge Gateway without storing video footage. The data inferencing occurs near real-time. 

This inferenced data is then sent to the Connected Store Cloud for further processing and aggregation with other customer business data and configuration data to deliver insights that are accessible via the Connected Store Web application.  

Customer data processed in the Connected Store Cloud is used to provide customers with the Connected Store service, including by providing insights about retail locations, and also to improve and troubleshoot the Connected Store Cloud service and other operations incident to delivering the services (for example, managing your account, internal reporting, and improving core functionality such as privacy and accessibility). While Dynamics 365 Connected Store is still in a preview phase some privacy measures may differ from controls in place for Microsoft commercial cloud services. However, for any personal data sent to the Connected Store cloud service, Microsoft provides the contractual commitments required by Article 28 of the GDPR.



