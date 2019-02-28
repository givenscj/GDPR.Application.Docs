# Email Setup

Before you start, you should setup and SMTP service for outgoing emails.  You can utilize any SMTP system, but it is preferred that you utilize SendGrid to prevent the desenimation of authorization codes for MFA and error logging.  There should be two accounts, one for error logging messages and one for tracking data subject communications.  Since error tracking is done in the database and emails don't need to be tracked, you should configure a less expensive email solution (such as an O365 account).

##  Office 365 SMTP

You can utilize Office 365 as your SMTP server, but it will require that you setup an email account to do so.

### Create accounts for Data Subject and Error emails

-   Login to the [O365 Portal]()
-   Click **Users**
-   Click **Add User**

### Setup the configuration.production.json file

-   Open the configuration file, update the following settings for the Data Subject sending:
    -   MailService = **GDPR.Common.Services.SmtpService**
    -   MailServer = **smtp.office365.com**
    -   MailServerPort = **587**
    -   UseSecurity = **true**
    -   MailServerUsername = **Email from above gdpr user**
    -   MailServerPassword = **Password from above gdpr user**
    -   NoReplyEmailAddress = **Email address of above gdpr user**

For Errors email sending:

    -   ErrorMailService = **GDPR.Common.Services.SmtpService**
    -   ErrorMailServer = **smtp.office365.com**
    -   ErrorMailServerPort = **587**
    -   ErrorUseSecurity = **true**
    -   ErrorMailServerUsername = **Email from above error user**
    -   ErrorMailServerPassword = **Password from above error user**
    -   ErrorNoReplyEmailAddress = **Email address of above error user**

##  SendGrid SMTP

You can utilize SendGrid as your SMTP server, but it will require that you setup a SendGrid account to do so.

### Create an account

-   Create an account with [SendGrid](https://sendgrid.com/pricing)
-   Select the **Free** pricing model
-   Click **Try for Free**
-   Enter all your details to create an account
-   Login to the [SendGrid]()
-   Create a new API Key
    -   Click **Settings**
    -   Click *API Keys**
    -   Click **Create API key**
    -   For the name, type **GDPR SMTP**
    -   Click **Create & View**
-   Record the new API Key

### Setup the configuration.production.json file

-   Open the configuration file
-   Update the following settings for data subject email sending (it is not advised to use this account for your error email sending due to costs):
    -   MailService = **GDPR.Common.Services.SmtpService**
    -   MailServer = **smtp.sendgrid.net**
    -   MailServerPort = **587**
    -   UseSecurity = **true**
    -   MailServerUsername = **apikey** (literally the text **apikey**)
    -   MailServerPassword = **API Key from above**
    -   NoReplyEmailAddress = **Email address of above user**
