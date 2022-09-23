---
author: alwinv
description: Learn how to update expiring certificates for Dynamics 365 Connected Spaces Preview
ms.author: rapraj
ms.date: 09/30/2022
ms.topic: article
title: Update expiring certificates for Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Update expiring certificates for Dynamics 365 Connected Spaces Preview

To ensure that the Microsoft Dynamics 365 Connected Spaces Preview deployment in your network remains compliant and secure, the certificate used to authenticate to the Connected Spaces project must be updated regularly. Microsoft tracks the validity of the certificate through the Azure Key Vault as part of the Managed Application. 

To provide continual access to the Connected Spaces services so that they can propagate data, the Azure Service Principal admin should review and maintain the certificate to keep it from expiring. 

If you're the Service Principal admin, use the steps in this article to determine when the Connected Spaces Preview certificates expire. You need to collect data from two different places: Key Vault and App registrations. 

## Find certificate expiration dates

To identify when your Connected Spaces Preview certificates expire, you need to collect data from two different places: Key Vault and App registrations. 

### Key Vault

1. In Microsoft Azure, in the main Azure search box, enter **mrg-connected-spaces-** to go to the Managed App resource created during the deployment.

   ![Screenshot of Azure search box with mrg-connected-spaces entered.](media/setup-certificates-1.JPG "Screenshot of Azure search box with mrg-connected-spaces entered")
    
2. Select the **Key Vault** row. 

    ![Screenshot with Key vault row highlighted.](media/setup-certificates-2.JPG "Screenshot with Key vault row highlighted")

3. Go to the **Certificates** section for the Key Vault.

    ![Screenshot showing Certificates command highlighted.](media/setup-certificates-3.JPG "Screenshot showing Certificates command highlighted")

4. Find the certificate named **liveaiserviceprincipalprivatekey**. Note the expiration date. 

    ![Screenshot of liveaiserviceprincipalprivatekey and expiration date highlighted.](media/setup-certificates-4.JPG "creenshot of liveaiserviceprincipalprivatekey and expiration date highlighted")

5. Go to the **Secrets** section for the Key Vault. 

    ![Screenshot with Secrets command highlighted.](media/setup-certificates-5.JPG "Screenshot with Secrets command highlighted")

6. Find the secret used for the service principal called ServicePrincipalSecret. Note the expiration date. 

    ![Screenshot with ServicePrincipal Secret and expiration date highlighted.](media/setup-certificates-6.JPG "Screenshot with ServicePrincipal Secret and expiration date highlighted")

7. Find the secret that specifies the App registration used with Connected Spaces. It's called **ServicePrincipalId**. 

    ![Screenshot highlighting ServicePrincipalId.](media/setup-certificates-7.JPG "Screenshot highlighting ServicePrincipalId")
    
8. Copy the value of the secret to your Clipboard to look up the App registration.

### App registrations

1. Go to the Azure Active Directory Service.

    ![Screenshot of Azure search box with Azure Active Directory entered in the search box.](media/setup-certificates-8.JPG "Screenshot of Azure search box with Azure Active Directory entered in the search box")

2. On the **Overview** tab, look up the ID that you copied from the Key Vault.

    ![Screenshot of Overview tab.](media/setup-certificates-9.JPG "Screenshot of Overview tab")

3. In the App registration, go to the **Certificates & secrets** section. 

    ![Screenshot of Certificates & secrets command.](media/setup-certificates-10.JPG "Screenshot of Certificates & secrets command")

4. On the **Client secrets** tab, note the expiration date for your current secret. 

    ![Screenshot of Client secrets tab with expiration date highlighted.](media/setup-certificates-11.JPG "Screenshot of Client secrets tab with expiration date highlighted")

5. Go to the **Certificates** tab, and find the expiration date for the certificate set in the App registration. 

    ![Screenshot of Certificates tab with expiration date highlighted.](media/setup-certificates-12.JPG "Screenshot of Certificates tab with expiration date highlighted")

These are the expiration dates to keep in mind. 

## Renew service principal certificates and secrets

When Connected Spaces Preview is deployed, a service principal is created in your tenant along with the necessary credentials to authenticate to it. These credentials expire within two years for both the certificate and the secret. You'll receive an email message about six months before the certificate expires, indicating that you need to update the certificate manually. You must do this update before the credentials expire. **Otherwise, you will experience data loss.**

> [!IMPORTANT]
> After you update the secret and the certificate in the Key Vault, you must apply the same changes to the service principal as soon as possible. The device will update and use these new values within 10 minutes after you make the changes. 

### Prerequisites

You must be an owner of the service principal that you want to update.

### Find the credentials in the Key Vault

1. Go to [portalzaure.com](portalzaure.com). 

2. In the main Azure search bar, enter **mrg-connected-spaces-** to search for the resource group. 

    ![Screenshot of Azure search bar with mrg-connected-spaces- entered in search box.](media/setup-certificates-13.JPG "Screenshot of Azure search bar with mrg-connected-spaces- entered in search box")

3. After you find the resource group, locate the Key Vault for this deployment.

    ![Screenshot highlighting Key Vault row.](media/setup-certificates-14.JPG "Screenshot highlighting Key Vault row")

4. Go to **Certificates**.

    ![Screenshot of Certificates command.](media/setup-certificates-15.JPG "Screenshot of Certificates command")

5. Select the **liveaiserviceprincipalprivatekey** certificate. 

6. Select **New Version** at the top of the page to create a new version of the certificate. 

    ![Screenshot highlighting New Version command.](media/setup-certificates-16.JPG "Screenshot highlighting New Version command")

7. Select **Create** at the bottom of the page to create the new certificate. **You don't need to make any other changes on this page.** 

8. After the new version has been created, refresh the page. You'll see that a new version is available.

9. Select the newly created version and then download and save the PFX file. 

    ![Screenshot showing Download command highlighted.](media/setup-certificates-17.JPG "Screenshot showing Download command highlighted")

### Update the service principal

After completing the setup for the update, update the service principal with the new credentials.

1. In the main Azure search box at the top of the page, search for the **Azure Active Directory** service. 

    ![Screenshot of Azure search box with Azure Active Directory entered in the search box.](media/setup-certificates-18.JPG "XXX")

2. On the **Overview** tab, enter **cs-dbe** in the search box to find your App registration. 

    ![Screenshot of Overview tab.](media/setup-certificates-19.JPG "Screenshot of Overview tab")

3. Go to **Certificates & secrets** to view your credentials.

    ![Screenshot of Certificates & secrets command.](media/setup-certificates-20.JPG "Screenshot of Certificates & secrets command")

4. Select the **Client secrets** (default) tab, and then select **New client secret**.

    ![Screenshot of Client secrets tab and New client secret highlighted.](media/setup-certificates-21.JPG "Screenshot of Client secrets tab and New client secret highlighted")

5. In the dialog box that's displayed, enter a description and set the expiration to 24 months. Then select **Add**. 

    ![Screenshot of Description and Expiration fields.](media/setup-certificates-22.JPG "Screenshot of Description and Expiration fields")

6. You'll see a new exposed secret. This is the only time that the secret is visible. Copy the secret value to a text editor to update the secret in the Key Vault.

    ![Screenshot of the secret.](media/setup-certificates-23.JPG "Screenshot of the secret")

7. Select the **Trashcan** button to delete any old secrets to avoid any potential security risks.

    ![Screenshot showing Trashcan button highlighted.](media/setup-certificates-24.JPG "Screenshot showing Trashcan button highlighted")

8. Go to **Certificates**.

    ![Screenshot of Certificates command.](media/setup-certificates-25.JPG "Screenshot of Certificates command")

9. Select **Upload certificate**, and then go to the location where you saved the PFX certificate you downloaded from the Key Vault.

    ![Screenshot highlighting Upload certificate.](media/setup-certificates-26.JPG "Screenshot highlighting Upload certificate")

10. Delete any old certificates to avoid any potential security risks.

### Create a new secret

1. Go back to the Key Vault.

2. Go to **Secrets**.

    ![Screenshot of Secrets command.](media/setup-certificates-27.JPG "Screenshot of Secrets command")

3. Select **ServicePrinicpalSecret**.

    ![Screenshot showing ServicePrincipalSecret row highlighted.](media/setup-certificates-28.JPG "Screenshot showing ServicePrincipalSecret row highlighted")

4. Go into **Current** to copy the content type to use in the new secret version. Store it in a text editor to use for the next step.

    ![Screenshot showing Content type highlighted.](media/setup-certificates-29.JPG "Screenshot showing Content type highlighted")

5. Go back to the previous page and select **New Version** at the top of the page to create a new version of this secret.

    ![Screenshot showing New Version highlighted.](media/setup-certificates-30.JPG "Screenshot showing New Version highlighted")

6. Include the expiration date: leave the default (2 years)

7. Include the content type: Paste the value you saved in step 4.

8. Enter your new value. This is the secret you generated for the service principal. 

9. Select the **Create** button at the bottom of the page.

    ![Screenshot of Create a secret screen.](media/setup-certificates-31.JPG "Screenshot of Create a secret screen")




