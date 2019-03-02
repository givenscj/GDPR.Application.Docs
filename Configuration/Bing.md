# Bing Maps API

Bing and Google are used to perform Address geocoding in the platform.  This helps to ensure that addresses are in a proper format for searching.  The database will cache results as needed so subsequent calls are not performed.  As one service fails, the other will serve as a backup.

-   Open the [Bing Maps Developer Portal](https://www.bingmapsportal.com/)
-   Click **Sign In**
-   Click **My Account**, then select **My keys**
-   Click the link to create a new key
-   Type a name, url
-   Select **Basic** as the key type
-   For the applicaiton type, select **Public website**
-   Click **Create**
-   Click **Show key**, record the

## Configuration

-   Open the configuration file
-   Copy the following values:
    -   **BingMapsApiKey** as API key

## Tenant Level PayPal Settings

-   Sub tenants of the system can have their own map settings
-   You can access this from the [Settings](https://{prefix}gdprwebadmin.azurewebsites.net/Home/TenantSettings).