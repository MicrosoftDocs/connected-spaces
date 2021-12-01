---
author: alwinv
description: Learn how to create a new Azure Active Directory tenant to use with Dynamics 365 Connected Spaces Preview
ms.author: alwinv
ms.date: 12/02/2021
ms.topic: article
title: Create a new Azure Active Directory tenant for Dynamics 365 Connected Spaces Preview
ms.reviewer: v-bholmes
---

# Create a new Azure Active Directory tenant for the Dynamics 365 Connected Spaces Preview

[!INCLUDE[banner](includes/banner.md)]

For Microsoft Dynamics 365 Connected Spaces Preview, we recommend signing up with a new test Azure Active Directory tenant to simplify account management 
during the preview.

To set up a new test Azure Active Directory tenant, you’ll:

- Create a test tenant under a new domain of onmicrosoft.com

- Create a global administrator account for yourself

- Assign a 6-month trial license to Connected Spaces

## Sign up by creating a new tenant

1. [Go to the Dynamics 365 Connected Spaces sign-up page](https://go.microsoft.com/fwlink/?linkid=2128173).

2. Under **Let’s set up your account**, enter your company email address, and then select **Next**.

    ![Company email address field.](media/email-address.PNG "Company email address field")

3. Select **Create a new account instead**.

    > [!IMPORTANT]
    > Create a new account to test Connected Spaces instead of signing in with your company’s existing Azure Active Directory tenant admin account. 
    This simplifies management of Connected Spaces and ensures your testing doesn’t impact any of your company’s existing business processes.
    
    ![Create new account instead link.](media/create-new-account.PNG "Create new account instead link")
    
4. Fill in your account information, and then select **Next** to verify your new account.

    > [!NOTE]
    > For the preview, you can only select **United Kingdom** or **United States** in the **Country or region** field. This selection determines the country or region in which your Connected Spaces application will be installed and where your data will reside. 
    
    ![Account information fields.](media/account-info.PNG "Account information fields")  
    
5. Enter a phone number for verification purposes, and then select **Send Verification Code**.

    ![Send Verification Code button.](media/send-verification-code.PNG "Send Verification Code button")
    
6. Under **Create your business identity**, enter a temporary domain name (for example, "Contoso"), and then select **Check availability**. 

    > [!NOTE]
    > Connected Spaces uses the Azure Active Directory tenant to manage permissions. The user accounts you’ll create later will be in the domain 
    you create in this step. For example, if you choose “Contoso” as your domain, a user account for “someone” would be: someone@contoso.onmicrosoft.com.
    
    ![Domain name field.](media/business-identity.PNG "Domain name field")
    
7. When you have confirmed that the name is available to use, select **Next**.

8. Enter a user account name and password for the global admin account.
  
   ![Global admin credentials fields.](media/credentials.PNG "Global admin credentials fields")
   
9. Select **Sign up** to agree to the terms for the new test tenant. 

    At this point, the Setup program will: 
    
    - Create the new Azure Active Directory tenant account
    
    - Create your new admin user account
    
    - Sign you in to your new admin account
    
    - Assign the Dynamics 365 Connected Spaces Preview trial license to the tenant
    
    - Assign a client license for this trial to the admin user account    
    
10. Under **You’re all set**, select **Let’s go**, and then go to the next step: [Install Connected Spaces Preview](admin-install-web-app.md).  

    ![Let's go button.](media/lets-go.PNG "Let's go button")

## Next step

[Install Connected Spaces Preview](admin-install-web-app.md)



