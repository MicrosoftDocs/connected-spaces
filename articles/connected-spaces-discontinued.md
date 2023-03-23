---
title: Frequently asked questions about Dynamics 365 Connected Spaces preview service discontinuation 
description: Information related to the discontinuation of service for Dynamics 365 Connected Spaces preview.
ms.author: mhart
ms.date: 03/23/2023
ms.topic: conceptual
author: m-hartmann
ms.reviewer: mhart
---

# Frequently asked questions about Dynamics 365 Connected Spaces preview service discontinuation  

Information related to the discontinuation of service for Dynamics 365 Connected Spaces preview.

## General information

### What is being announced about Dynamics 365 Connected Spaces preview?

Effective April 4, 2023, Dynamics 365 Connected Spaces preview will be discontinued for all customers.  

Current customers with a trial license for Dynamics 365 Connected Spaces preview can access the service and generate usage data as needed, until the trial expires on April 4, 2023  

### Why is Dynamics 365 Connected Spaces being discontinued?

Microsoft is consolidating efforts in computer vision services available on the Azure platform. We're also accelerating computer vision solutions from the Microsoft partner ecosystem across system integrators and integrated solution vendors.

### How are Connected Spaces preview customers notified?

The announcement is communicated through system emails and individual outreach to all Connected Spaces preview admins. The outreach started in February 2023.

### What is the recommended path for customers and prospects?

Azure Cognitive Services offers services for scenarios like people counting or entrance counting using video cameras through Custom Vision and Spatial Analysis.

## Subscription and billing information

### What customer subscriptions are affected by this announcement?

All licenses for Dynamics 365 Connected Spaces preview will be impacted.

### Who can customers contact for billing issues and concerns?

Review your [Dynamics 365 billing and subscription support options](/dynamics365/get-started/support/). [Send us an email](mailto:dcs-support@microsoft.com) for escalations.

## Retrieving data

### How can customers delete their data?

You can delete your Connected Spaces environment before the retirement date. Deleting an environment is permanent and cannot be undone. All data and configurations associated with the environment will be permanently deleted.

1. Go to https://admin.powerplatform.microsoft.com/environments and sign in as administrator.

1. Select the *Connected Spaces Trial* environment.

1. Select **Delete** in the ribbon and confirm the deletion.

The Azure resources on the Connected Spaces managed application remain operational until April 4, 2023. We’ll delete the Dataverse environment on April 4 and all data will be removed permanently. Export the date before that date if you plan to keep using it. Deleting the Dataverse environment for Connected Spaces has no impact on other Dataverse environments. Contact [dcs-support@microsoft.com](mailto:dcs-support@microsoft.com) for additional clarifications.  

### What options do customers have regarding the Azure Stack Edge Devices?

To repurpose your Azure Stack Edge device for other workloads, you can [reset and reactivate your device](/azure/databox-online/azure-stack-edge-reset-reactivate-device) to remove the Connected Spaces application.  

To return your Azure Stack Edge device, you can [reset and return your device to Microsoft](/azure/databox-online/azure-stack-edge-return-device?tabs=azure-edge-hardware-center).

## Additional resources  

For questions related to transitioning, please contact your Microsoft representative, partner, or [send us an email](mailto:dcs-support@microsoft.com).
