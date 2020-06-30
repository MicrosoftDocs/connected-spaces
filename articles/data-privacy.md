---
author: alwinv
description: Data and Privacy
ms.author: alwinv
ms.date: 07/01/2020
ms.service: crm-online
ms.topic: article
title: Data and Privacy
ms.reviewer: v-brycho
---

# Data and Privacy

Microsoft Dynamic 365 Connected Store has three components, and each is designed with compliance, security, and privacy in mind. 

SCREEN SHOT GOES HERE
￼
- **Connected Store Edge Gateway** – A managed Azure Stack Edge gateway installed in the retail store that runs computer vision AI model(s) to convert camera streams from existing or new cameras into observational data sent to the cloud.

- **Connected Store Cloud Service and Web application** – A  Software-as-a-service (SaaS) cloud service running on Azure and a Connected Store web application that correlates observational data from the Connected Store Edge  gateway with business data to provide insights and recommended actions for the retailer.

- **Connected Store Mobile application** – A mobile app to provide retailers a consumer-class onboarding experience to setup the edge gateway,  assist customers’ configuration of cameras to deliver camera feed to the edge gateway, and view insights.

The Connected Store Edge Gateway processes video data from the in-store camera locally on the device, makes AI data inferences without identifying or tracking individuals to generate inferenced (observational) data, and sends the inferenced data to the Connected Store Cloud.

## What data does Connected Store process?  

In the retail store(s), the Connected Store Edge Gateway processes the following types of data:
 
- **Video stream** – The video stream from customers’ in-store cameras is processed in memory, in real time, on the Connected Store Edge Gateway to generate Inference data. **This data is not stored on the gateway, nor sent to Microsoft’s cloud.**

- **Inference data** – This is the event data output by containerized AI skills (models) that describe an inferred event. Event data includes data such as a time stamp, notation about the type of event (e.g. "entry" or "exit" crossing line or zones), a rectangle “bounding box” that coordinates the area tracked within the camera frame, a confidence score that indicates confident of the “bounding box” being a person, and a pseudonymous Identifier to track the “bounding box”. 

- **Camera snapshot image** – A snapshot image from in-store camera is passed through to the Connected Store Mobile app during set up and configuration via [IoT Hub direct invoke method](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods) on Connected Store Cloud service. No image is cached on the mobile app or Edge Gateway or sent to the cloud. 
 
In the Connected Store Cloud service on Azure, the following types of data are processed to provide the service:

- **Insights data** - The inference data described above is aggregated and correlated with other business data to turn into insights data that is stored in the Connected Store Cloud for viewing on the Connected Store Mobile app. Insights data includes: 

   - Time stamp - summarized by hour or other time interval

   - Value - the number over that hour

   - Measurement type - entries, exists, dwell time, occupancy

   - Aggregation Type - total, average, maximum, minimum

   - Zone - Front Entrance, Isle 1 display, etc.

- **Configuration data** – This is information about Connected Store and Edge Gateway configuration that is used for setup and configuration of camera zone (e.g. store name, paired camera IP address and zone skills). 

- **Telemetry data** – This is information about the health of the Edge Gateway, the Connected Store Cloud Service, and the Connected Store mobile application. 

- **Order data** – This is the information tied to the customer’s account and provides details around the Edge hardware ordered and where it was shipped.  This includes data points such as Company name, Shipping address, Shipping status info, Contact info, and Device serial number.

The Connected Store Mobile app and the Connected Store Web application do not collect any additional information as both applications access and use data from the Connected Store Cloud service. 

## How does Connected Store process data?

Microsoft Dynamics 365 Connected Store processes data as instructed by the customer to provide the Connected Store solution.  

During setup, customers instruct the Connected Store Mobile app to pair video streams from the customer’s in store camera to the Connected Store Edge Gateway for zone configuration of their store. After the configuration is completed, the paired cameras are streaming video directly to the Connected Store Edge Gateway on customers’ premises for AI inferencing using AI skills. The AI skills (models) running on customers’ premises are not trained with the video data unless a customer specifically instructs Microsoft to do so and grants Microsoft the right to access its video feed to enhance the underlying AI skill models.

The AI skills detect and track people’s movements in the video feed based on algorithms that identify the presence of one or more humans and generates events when a person moves in or out of designated zones in the camera’s field of view and outputs the coordinates of the person’s body into a bounding box. For each bounding box movement detected in a camera zone, the AI skill outputs inference data including the following:

- Bounding box coordinates of person’s body

- Event type (e.g. zone entry or exit, directional line crossing)

- Pseudonymous identifier to track bounding box 

- Confidence score for the detection 

The AI inferencing does not require any sound recording and the video feed from customers’ cameras only includes image data. No video data leaves the premises and no video data is stored on the Edge Gateway  or sent to the Connected Store Cloud. The AI data inferencing is performed locally in-memory on the Connected Store Edge Gateway without storing video footage. The data inferencing occurs near real-time. 

This inferenced data is then sent to the Connected Store Cloud for further processing and aggregation with other customer business data and configuration data to deliver insights that are accessible via the Connected Store Web application.  

Customer data processed in the Connected Store Cloud is used to provide customers with the Connected Store service, including by providing insights about retail locations, and also to improve and troubleshoot the Connected Store Cloud  service and other operations incident to delivering the services (for example, managing your account, internal reporting, and improving core functionality such as privacy and accessibility).



