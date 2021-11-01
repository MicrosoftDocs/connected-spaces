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

![Illustration of retail store, Azure cloud service and Power Platorm components.](media/how-connected-spaces-works.png "Illustration of retail store, Azure cloud service and Power Platorm components")

- **Edge device** – A customer-managed Azure Stack Edge Pro (2 GPU) gateway installed in the retail store that runs computer vision AI model(s) to convert video streams from existing or new cameras into inference data. The edge device processes video data from the in-store camera locally on the device (at the edge) and uses AI models to draw conclusions from that video footage ("inferences") without identifying individuals to generate inference data. 

- **Connected Spaces cloud service and app** – A  Software-as-a-service (SaaS) cloud service running on Azure and a Connected Spaces web app that provides insights for the retailer. The edge device sends the inference data to the Connected Spaces service so that it can be correlated with the retailer’s business data (for example, store business hours, camera zone name) and aggregated to generate actionable insights regarding retail operations. Customers can then use the Connected Spaces web app to view the resulting insights data stored in the Connected Spaces service for Shopping analytics, Display effectiveness, and Queue management insights. 

- **Microsoft Dataverse storage** – A database in the customer’s Power Platform environment. The customer’s inference data is stored in Microsoft Dataverse for easy access by the customer. The customer also has the option to store and manage their video data in Microsoft Dataverse.

## What data does Connected Spaces process?  

In the retail store(s), the Connected Spaces edge device is used to process the following types of data:

- **Video stream** – The video stream from customers’ in-store cameras is processed in memory, in real time, on the Connected Spaces edge device to generate inference data and is stored in Microsoft Dataverse in the customer's Microsoft Power Platform environment. **Every customer has the ability to choose if video data is stored in their cloud and to manage it. Go to Settings > Privacy Information to change where video is stored.**

- **Inference data** – This is the event data output by AI skills (models) running on the edge device that describe an inferred event. Event data includes data such as a time stamp, notation about the type of event (for example, "entry" or "exit" crossing line or zones), a rectangle “bounding box” that coordinates the area tracked within the camera frame, a confidence score that indicates confidence of the “bounding box” being a person, and a pseudonymous identifier associated with the “bounding box”. 
 
In the Connected Spaces cloud service on Azure, the following types of data are processed at the instructions of the customer to provide the service:

- **Insight data** - The inference data described above is aggregated, depersonalized, and correlated with other business data to turn into insights data that is stored in the Connected Spaces cloud for viewing via the Connected Spaces web app. The customer may delete the data at any time and must delete the data in accordance with applicable legal obligations. Insight data includes: 

   - Time stamp - summarized by hour or other time interval

   - Value - the number over that hour

   - Measurement type - entries, exits, dwell time, occupancy

   - Aggregation type - total, average, maximum, minimum

   - Zone – such as Front Entrance, Aisle 1 display, and so on

- **Configuration data** – This is information about the retailer’s store and the Connected Spaces edge device configuration that is used for setup and configuration of camera zones (for example, store name, paired camera IP address, camera view snapshot image, and zone skills). 

- **Telemetry data** – This is information about the health of the edge device, the Connected Spaces cloud service, and the Connected Spaces mobile app. 

## How does Connected Spaces process data?

Dynamics 365 Connected Spaces processes data as instructed by the customer to provide the Connected Spaces solution.  

Customers use the Connected Spaces web app to configure their store. They connect cameras, draw skills, and configure their store settings with the web app. After the configuration is completed, video footage from the paired cameras is streamed directly to the Connected Spaces edge device, installed on the customers’ premises, to create inference data using AI skills. The AI skills (models) running on customers’ premises are pre-trained "out of the box" and not trained with the customer's specific video data unless a customer specifically instructs Microsoft to do so and grants Microsoft the right to access its video feed to enhance the underlying AI skill models.

The AI skills running locally on the edge device detect and track unidentified people’s movements in the video feed based on algorithms that identify the presence of one or more humans. The algorithms generate events when a person moves in or out of designated zones in the camera’s field of view and outputs the coordinates of the person’s body into a bounding box. For each bounding box movement detected in a camera zone, the AI skill output inference data includes the following:

- Bounding box coordinates of person’s body

- Event type (for example, zone entry or exit, directional line crossing)

- Pseudonymous identifier to track the bounding box 

- Confidence score for the detection 

The AI data inferencing is performed locally in memory on the Connected Spaces edge device near real time. This inferenced data is then sent to the Connected Spaces service for further processing and aggregation with other customer business data and configuration data to deliver insights that are accessible through the Connected Spaces web app.  

Customer data processed in the Connected Spaces cloud is used to provide customers with the Connected Spaces service, including by providing insights about retail locations, and also to improve and troubleshoot the Connected Spaces cloud service and other operations incident to delivering the services (for example, managing your account, internal reporting, and improving core functionality such as privacy and accessibility). The customer may delete the data at any time in their Microsoft Dataverse instance. While Dynamics 365 Connected Spaces is still in a preview phase, some privacy measures may differ from controls in place for Microsoft commercial cloud services. However, for any personal data sent to the Connected Spaces cloud service, Microsoft provides the contractual commitments required by Article 28 of the GDPR. For more information, see [Privacy and Personal Data for Microsoft Dynamics 365 and GDPR Overview](https://docs.microsoft.com/dynamics365/get-started/gdpr/).

Shoppers and employees may have privacy questions related to data collected and processed by retail stores. Connected Spaces customers can refer to the best practices outlined in our guides ([Communicate with shoppers](communication-plan.md) and [Communicate with employees](employee-plan.md)) as they consider how to effectively communicate about data used by Connected Spaces. 



