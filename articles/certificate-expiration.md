# Certificates

## Find certificate expiration dates

To identify when your Connected Spaces Preview certificates expire, you need to collect data from two different places.

### Key vault

1. In Microsoft Azure, in the main Azure search box, enter xxx to go to the Managed App resource created during the deployment.

   ![XXX.](media/setup-certificates-1.JPG "XXX")
    
2. Select the **Key vault** row. 

    ![XXX.](media/setup-certificates-2.JPG "XXX")

3. Go to the **Certificates** section for the key vault.

    ![XXX.](media/setup-certificates-3.JPG "XXX")

4. Find the certificate named **liveaiserviceprincipalprivatekey**. Note the expiration date. 

    ![XXX.](media/setup-certificates-4.JPG "XXX")

5. Go to the **Secrets** section for the Key vault. 

    ![XXX.](media/setup-certificates-5.JPG "XXX")

6. Find the secret used for the service principal called ServicePrincipalSecret. Note the expiration date. 

    ![XXX.](media/setup-certificates-6.JPG "XXX")

7. Find the secret that specifies the App Registration used with Connected Spaces. It's called **ServicePrincipalId**. 

    ![XXX.](media/setup-certificates-7.JPG "XXX")
    
8. Copy the value of the secret to your Clipboard to look up the App Registration.

### App Registrations

1. Go to the Azure Directory Service.

    ![XXX.](media/setup-certificates-8.JPG "XXX")

2. On the **Overview** tab, look up the ID that you copied from the Key vault.

    ![XXX.](media/setup-certificates-9.JPG "XXX")

3. In the App Registration, go to the **Certificates & secrets** section. 

    ![XXX.](media/setup-certificates-10.JPG "XXX")

4. On the **Client secrets** tab, note the expiration date for your current secret. 

    ![XXX.](media/setup-certificates-11.JPG "XXX")

5. Go to the **Certificates** tab, and find the expiration date for the certificate set in the App Registration. 

    ![XXX.](media/setup-certificates-12.JPG "XXX")

These are the expiration dates to keep in mind. 

## Renew Service Principal certificates and secrets

When Connected Spaces Preview is deployed, a Service Principal is created in your tenant along with the necessary credentials to authenticate to it. These credentials expire within two years for both the certificate and the secret. You'll receive an email message about six months before the certificate expires, indicating that you need to update the certificate manually. You must do this update before the credentials expire. **Otherwise, you will experience data loss.**

> [!IMPORTANT]
> After you update the secret and the certificate in the Key vault, you must apply the same changes to the Service Principal as soon as possible. The device will update and use these new values within 10 minutes after you make the changes. 

### Prerequisites

You must be an owner of the Service Principal that you want to update.

### Find the credentials in the Key vault

1. Go to [portalzaure.com](portalzaure.com). 

2. In the main the Azure search bar, enter **mrg-connected-spaces-** to search for the resource group. 

    ![XXX.](media/setup-certificates-13.JPG "XXX")

3. After you find the resource group, locate the Key vault for this deployment.

    ![XXX.](media/setup-certificates-14.JPG "XXX")

4. Go to the **Certificates** tab.

    ![XXX.](media/setup-certificates-15.JPG "XXX")

5. Select the **liveaiserviceprincipalprivatekey** certificate. 

6. Select **New Version** at the top of the page to create a new version of the certificate. 

    ![XXX.](media/setup-certificates-16.JPG "XXX")

7. Select **Create** at the bottom of the page to create the new certificate. You don't need to make any other changes on the page. 

8. After the new version has been created, refresh the page. You'll see that a new version is available.

9. Select the newly created version and then download and save the PFX file. 

    ![XXX.](media/setup-certificates-17.JPG "XXX")

### Update the Service Principal

After completing the setup for the update, update the Service Principal with the new credentials.

1. In the main Azure search bar at the top of the page, search for the **Azure Active Directory** service. 

    ![XXX.](media/setup-certificates-18.JPG "XXX")

2. On the Overview tab, enter **cs-dbe** in the search bar to find your App registration. 

    ![XXX.](media/setup-certificates-19.JPG "XXX")

3. Go to the **Certificates & secrets** tab to view your credentials.

    ![XXX.](media/setup-certificates-20.JPG "XXX")

4. Select the **Client secrets** (default) tab, and then select **New client secret**.

    ![XXX.](media/setup-certificates-21.JPG "XXX")

5. In the dialog box that's displayed, enter a description and set the expiration to 24 months. Then select **Add**. 

    ![XXX.](media/setup-certificates-22.JPG "XXX")

6. You'll see a new exposed secret. This is the only time that the secret is visible. Copy SCREENSHOT GOES HEREthe secret value to a text editor to update the secret in the Key vault.

    ![XXX.](media/setup-certificates-23.JPG "XXX")

7. Delete any old secrets to avoid any potential security risks.

    ![XXX.](media/setup-certificates-24.JPG "XXX")

8. Select the **Certificates** tab.

    ![XXX.](media/setup-certificates-25.JPG "XXX")

9. Select **Upload certificate**, and then go to the location where you saved the PFX certificate you downloaded from the Key vault.

    ![XXX.](media/setup-certificates-26.JPG "XXX")

10. Delete any old certifiates to avoid any potential security risks.

### Create a new secret

1. Go back to the Key vault.

2. Go to the **Secrets** tab.

    ![XXX.](media/setup-certificates-27.JPG "XXX")

3. Select **ServicePrinicpalSecret**.

    ![XXX.](media/setup-certificates-28.JPG "XXX")

4. Go into **Current** to copy the content type to use in the new secret version. Store it in a text editor to use for the next step.

    ![XXX.](media/setup-certificates-29.JPG "XXX")

5. Go back to the previous page and select **New Version** at the top of the page to create a new version of this secret.

    ![XXX.](media/setup-certificates-30.JPG "XXX")

6. Include the expiration date: leave the default (2 years)

7. Include the content type: Paste the value you saved in step 4.

8. Enter your new value. This is the secret you generated for the Service Principal. 

9. Select the **Create** button at the bottom of the page.

    ![XXX.](media/setup-certificates-31.JPG "XXX")




