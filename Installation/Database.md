# Database Setup

A blank database will be installed that will require you to initalize it.  At a minimum, you will need an email address to be able to do the initalization and setup the first administrator of the system as well as the initial system encryption password.

## Open the Admin Web Application

-   Open your [Azure Management Portal](https://portal.azure.com)
-   Click **Resource Groups**
-   Select the resource group you or your install created
-   Select the **[prefix]gdprwebadmin** web application
-   Click **Custom domains**
-   Record the **[prefix]gdprwebadmin.azurewebsites.net** url
-   Open the URL to the admin site.  It may take a few moments for the application to load

## Setup Admin user and system encryption key

-   On the setup page, enter the following values:
    -   The admin email address
    -   The system password
    -   Your license key
    -   Check the checkbox if you would like to have all the [Redirect](../Applications/RedirectApplications.md) applications created
-   Click **Setup**
