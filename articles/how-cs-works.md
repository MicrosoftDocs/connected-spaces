---
author: rapraj
description: Learn about the different components required for Dynamics 365 Connected Spaces and how it works
ms.author: rapraj
ms.date: 10/05/2022
ms.topic: article
title: How Dynamics 365 Connected Spaces works
ms.reviewer: v-bholmes
ms.custom: "intro-internal"
---

# How Dynamics 365 Connected Spaces works

[!INCLUDE [end-of-life](includes/end-of-life.md)]

[Dynamics 365 Connected Spaces](index.md) consists of the Connected Spaces web app, an Azure cloud service, Microsoft Dataverse, and camera hardware that you install in your store.

![Illustration of retail store, Azure cloud service and Power Platorm components.](media/how-connected-spaces-works.jpg "Illustration of retail store, Azure cloud service and Power Platform components")
 
In each of your retail stores, you:

- Install and activate an Azure Stack Edge Pro (2 GPU) gateway. The gateway receives video from the cameras connected to it, analyzes it, and transforms your customer activity into pseudonymous datapoints.

- Create a store, pair the gateway to the store, and configure your store’s cameras to track activity in the store.

The cloud service:

- Receives and stores the stream of datapoints.

- Processes the datapoints into aggregated observational data.

- Sends the processed data on a regular basis to Microsoft Dataverse in your Microsoft Power Platform environment.

- Processes and sends video streams and video stream metadata to Microsoft Dataverse in your Microsoft Power Platform environment. Customers can choose to have their video data streamed to Microsoft Dataverse.  

The Power Platform environment:

- Stores the incoming data and makes it available for Connected Spaces, where you can view analytics reports about activity in your stores.

## Next steps

- [Sign up for a free trial](trial-signup.md)
- [Trial FAQ](trial-faq.md)


