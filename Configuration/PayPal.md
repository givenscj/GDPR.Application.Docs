# Payment Processing

PayPal is the preferred payment processing engine for the privacy platform.  It is possible others will be supported in the future depending on customer requests.  The system is designed for plug and play as long as an appropriate API is available from the payment processor.

## Sign up for a PayPal Business Account

-   Open the [PayPal Website](https://www.paypal.com)
-   Click **Create Account**
-   Select **Business Account**

>NOTE: You will need a federal EIN in order to do this

-   Follow the remainder of the steps to create the account

## Setup PayPal IPN Url

-   Click **Profile and Settings**
-   Click **My Selling tools**
-   For **Instanct Payment Notifications**, click **Update**
-   Click **Choose IPN Settings**
-   Set your url to:
    -   https://{prefix}gdpradminweb.azurewebsites.net/Payment/IPN
-   Click **Receive IPN messages (Enabled)**
-   Click **Save**



## Setup PayPal Application

-   Open the [PayPal Developer Portal]()
-   Click **My apps & Credentials**
-   Scroll down the page, to the **REST API apps** section
-   Click **Create App**
-   For the name, type **GDPR**
-   Click **Create App**
-   Click the **Live** tab
-   Record the application client id and application secret

## Configuration

-   Open the configuration.production.json file
-   Update the following:
    -   Set the **PayPalClientId** to the value above
    -   Set the **PayPalClientSecret** to the value above
    -   For the mode, set to **production**

## Tenant Level PayPal Settings

-   Sub tenants of the system can have their own payment settings
-   You can access this from the [Settings](https://{prefix}gdprwebadmin.azurewebsites.net/Home/TenantSettings).