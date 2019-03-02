# Google Maps

When using addresses as a Data Subject data item, you will need to ensure that the address actually exists.  This can be done via the Google and Bing map apis.

## Setup

-   Open the [Google Maps Developer Portal](https://cloud.google.com/maps-platform)
-   Check the **Maps** checkbox
-   Click **CONTINUE**
-   Select your **GDPR** project
-   Click **Next**
-   In the dialog, click **Next**
-   Record the maps API key

## Configuration

-   Open the configuration file
-   Copy the following values:
    -   **GoogleMapsApiKey** as API key

## Tenant Level PayPal Settings

-   Sub tenants of the system can have their own map settings
-   You can access this from the [Settings](https://{prefix}gdprwebadmin.azurewebsites.net/Home/TenantSettings).