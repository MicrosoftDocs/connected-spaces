# Find certificate expiration dates

When trying to identify when your Connected Spaces Preview certificatrs expire, there are two different places you need to collect from.

## Key vault

1. In Microsoft Azure, go to the Managed App resource created during the deployment.

    SCREENSHOT GOES HERE
    
2. Select the **Key vault** row. 

    SCREENSHOT GOES HERE

3. Go to the **Certificates** section for the key vault.

    SCREENSHOT GOES HERE

4. Find the certificate named **liveaiserviceprincipalprivatekey**. Note the expiration date. 

    SCREENSHOT GOES HERE

5. Go to the **Secrets** section for the Key vault. 

    SCREENSHOT GOES HERE

6. Find the secret used for the service principal called ServicePrincipalSecret. Note the expiration date. 

    SCREENSHOT GOES HERE

7. Find the secret that specifies the App Registration used with Connected Spaces. It's called **ServicePrincipalId**. 

    SCREENSHOT GOES HERE
    
8. Copy the value of the secret to your Clipboard to look up the App Registration.

## App Registrations

1. Go to the Azure Directory Service.

    SCREENSHOT GOES HERE

2. On the **Overview** tab, look up the ID that you copied from the Key vault.

    SCREENSHOT GOES HERE

3. In the App Registration, go to the **Certificates & secrets** section. 

    SCREENSHOT GOES HERE

4. On the **Client secrets** tab, note the expiration date for your current secret. 

    SCREENSHOT GOES HERE

5. Go to the **Certificates** tab, and find the expiration date for the certificate set in the App Registration. 

    SCREENSHOT GOES HERE

These are the valuable expiration dates to keep in mind. 





