---
author: alwinv
description: Learn how to get started with Dynamics 365 Connected Spaces Preview by signing up for the preview, installing the software, and ordering Azure Stack Edge
ms.author: alwinv
ms.date: 11/02/2021
ms.topic: article
title: Get started with Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
ms.custom: "intro-internal"
---

# Get started with Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

Welcome to the Microsoft Dynamics 365 Connected Spaces Preview! This article describes how Connected Spaces works, and the overall process for acquiring, installing, configuring, and using Connected Spaces. 

## How Dynamics 365 Connected Spaces works

Connected Spaces consists of the Connected Spaces website, an Azure cloud service, Microsoft Dataverse, and camera hardware that you install at your store.

![Illustration of retail store, Azure cloud service and Power Platorm components.](media/how-connected-spaces-works.jpg "Illustration of retail store, Azure cloud service and Power Platform components")
 
In each of your retail stores, you’ll:

- Install and activate an Azure Stack Edge Pro (2 GPU) gateway. The gateway will receive video from the cameras connected to it, analyze it, and transform your customer activity into pseudonymous datapoints.

- Create a store, pair the gateway to the store, and configure your store’s cameras to track activity in the store.

The cloud service:

- Receives and stores the stream of datapoints.

- Processes the datapoints into aggregated observational data.

- Sends the processed data on a regular basis to Microsoft Dataverse in your Microsoft Power Platform environment.

- Processes and sends video streams and video stream metadata to Microsoft Dataverse in your Microsoft Power Platform environment. Customers can choose to have their video data streamed to Microsoft Dataverse.  

The Power Platform environment:

- Stores the incoming data and makes it available for the Connected Spaces, where you can view analytics reports about activity in your stores.

## How Connected Spaces documentation is organized

The Connected Spaces table of contents is organized to make it easy to get up and running quickly with the hardware and software described above. When you're ready to sign up for the preview and install the software, start with the first article in the Setup section and then proceed in order through the articles in the table of contents.

At the end of each article, you'll see a **Next step** heading that includes a link for the suggested next step to take.

