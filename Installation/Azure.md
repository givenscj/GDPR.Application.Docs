# Azure Setup

An Azure application can be used for many different things.  Due to the configuration of permissions with Azure AD applications, you will need to create several to support the various application stubs in the privacy platform:

-   Login Application
-   Dynamics Application
-   Office 365 Application
-   Exchange Application

## Configure Login Application

-   Open the [Azure Portal](https://portal.azure.com)
-   Click **Azure Active Directory**
-   Click **App registrations**
-   Click **New application registration**
-   For the name, type **Privacy Central Login**
-   For the sign-on URL, type **https://localhost:12345**
-   Click **Create**
-   Click **Settings**
-   Click **Required permissions**
-   Select **Windows Azure Active Directory**
-   Ensure that **Sign in and read user profile** is selected
-   If necessary, click **Save**
-   Click **Replay URLs**
-   In the empty textbox, type the URL of your deployed web applications.  You will have at least two:
    -   Admin - https://{prefix}gdprwebadmin.azurewebsites.net/signin-microsoft
    -   Subject - https://{prefix}gdprwebsubject.azurewebsites.net/signin-microsoft
    -   Subject - https://{prefix}gdprwebadmin.azurewebsites.net/Home/AzureAdAuthorize
    -   Subject - https://{prefix}gdprwebsubject.azurewebsites.net/Home/AzureAdAuthorize
-   Click **Keys**
-   In the **Passwords** section and the empty textbox, type **GDPRKey1**
-   For **Expires**, select **Never expires**
-   Click **Save**
-   Click **Properties**
-   Select **Yes** for the **Multi-tenanted** toggle
-   Click **Save**
-   Record the new application key
-   Record the application id
-   Open the configuration.production.json file, update the following values:
    -   For the **AzureClientSecret** value, copy the application key
    -   For the **AzureClientId** value, cope the application id

###Testing

-   Open a browser to your admin site.
-   Click **Login**, on the page you should see the **Microsoft** button
-   Click **Microsoft**, ensure that you are able to login and redirect back to the site

## Configure Dynamics Application

-   Open the [Azure Portal](https://portal.azure.com)
-   Click **Azure Active Directory**
-   Click **App registrations**
-   Click **New application registration**
-   For the name, type **Privacy Central Login**
-   For the sign-on URL, type **https://localhost:12345**
-   Click **Create**
-   Click **Settings**
-   Click **Required permissions**
-   Select **Windows Azure Active Directory**
-   Ensure that **Sign in and read user profile** is selected
-   Click **Save**

## Configure Office 365 Application

-   Open the [Azure Portal](https://portal.azure.com)
-   TODO

## Configure Exchange Applications

-   Open the [Azure Portal](https://portal.azure.com)
-   TODO