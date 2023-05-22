---
title: Dynamics 365 Connected Spaces preview service discontinuation FAQ
description: This article answers frequently asked questions about the discontinuation of service for Dynamics 365 Connected Spaces preview.
ms.author: mhart
ms.date: 03/23/2023
ms.topic: conceptual
author: m-hartmann
ms.reviewer: mhart
---

# Dynamics 365 Connected Spaces preview service discontinuation FAQ

This article answers frequently asked questions about the discontinuation of service for Dynamics 365 Connected Spaces preview.

## General information

### What is being announced about Dynamics 365 Connected Spaces preview?

Effective April 4, 2023, Dynamics 365 Connected Spaces preview will be discontinued for all customers.

Current customers who have a trial license for Dynamics 365 Connected Spaces preview can continue to access the service and generate usage data until the trial expires on April 4, 2023.

### Why is Dynamics 365 Connected Spaces preview being discontinued?

Microsoft is consolidating efforts in computer vision services that are available on the Azure platform. We're also accelerating computer vision solutions from the Microsoft partner ecosystem across system integrators and integrated solution vendors.

### How are Dynamics 365 Connected Spaces preview customers notified?

The announcement is communicated through system emails and individual outreach to all Dynamics 365 Connected Spaces preview admins. The outreach began in February 2023.

### What is the recommended path for customers and prospects?

Azure Cognitive Services offers services for scenarios such as using video cameras for people counting or entrance counting through Custom Vision and Spatial Analysis.

## Subscription and billing information

### What customer subscriptions are affected by this announcement?

All licenses for Dynamics 365 Connected Spaces preview are affected.

### Who can customers contact about billing issues and concerns?

Review your [Dynamics 365 billing and subscription support options](/dynamics365/get-started/support/). For escalations, [send us an email](mailto:dcs-support@microsoft.com).

## Retrieving data

### How can customers delete their data?

You can delete your Connected Spaces environment before the retirement date. Deletion of an environment is permanent and can't be undone. All data and configurations associated with the environment will be permanently deleted.

1. Go to <https://admin.powerplatform.microsoft.com/environments>, and sign in as administrator.
1. Select the **Connected Spaces Trial** environment.
1. Select **Delete** on the toolbar, and confirm the deletion.

The Azure resources on the Connected Spaces managed application will remain operational until April 4, 2023. On that date, we'll delete the Dataverse environment, and all data will be removed permanently. If you plan to continue to use the data, export it before April 4. Deletion of the Dataverse environment for Connected Spaces has no impact on other Dataverse environments. For more clarification, contact [dcs-support@microsoft.com](mailto:dcs-support@microsoft.com).

### What options do customers have for their Azure Stack Edge devices?

To repurpose your Azure Stack Edge device for other workloads, [reset and reactivate the device](/azure/databox-online/azure-stack-edge-reset-reactivate-device) to remove the Connected Spaces application.

To return your Azure Stack Edge device, [reset the device, and return it to Microsoft](/azure/databox-online/azure-stack-edge-return-device?tabs=azure-edge-hardware-center).

## Additional resources

For questions related to transitioning, contact your Microsoft representative or partner, or [send us an email](mailto:dcs-support@microsoft.com).
