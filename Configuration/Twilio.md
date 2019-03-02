# Twilio Phone and Voice

Not all privacy regulations are created or desigend equally.  In some cases such as California AB-375, you are required to have an IVR to respond to phone based requests.  The privacy platform utilzied Twilio to provide these services.

## Create a Twilio Account

-   Open the [Twilio Portal](https://www.twilio.com)
-   Click **Sign Up** and follow the steps to create a Twilio Account
-   You can utilize the Free tier to start

## Create a Phone Number (IVR)

-   On the dashboard, click **Get a trial number**
-   Search for a number, then click **Choose this number**
-   Record the number

## Create a Phone Number (FAX)

For verification purposes, individuals can fax their documents to a twilio fax phone number that will then scan and verify the information data subjects add to the platform (such as Social Security Number, Passport, etc).

>NOTE:  In order to have more than one number you must upgrade your twilio account.

-   On the dashboard, click **Get a trial number**
-   Search for a number, then click **Choose this number**
-   Record the number

## Setup Configuration file

-   On the dashboard, record your Account SID and Auth token
-   Copy the values to the following:
    -   Set the **TwilioAccountID** to the sid
    -   Set the **TwilioAuthToken** to the auth token
    -   Set the **TwilioNumber** to the IVR phone number
    -   Set the **TwilioFaxNumber** to the FAX phone number

## Set Tenant Settings

-   Open the admin portal web.
-   Click **System**
-   Search for the target tenant
-   Click **Switch**
-   Click **System**, then click **Settings**
-   Set the Twilio properties