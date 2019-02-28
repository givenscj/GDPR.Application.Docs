# Google Setup

A Google application is only used for authentication. 

## Configure Google Login

-   Open the [Google Developers Portal](https://developers.google.com/)
-   Click **Sign In**

>NOTE: if you do not have a google account, create one now

-   Once logged in, navigate to the [Google Console](https://console.cloud.google.com/?pli=1)
-   CLick **Select a project**
-   Click **NEW PROJECT**
-   For the name, type **GDPR Login**
-   Click **Create**
-   In the project drop down, select your new project
-   Click **Credentials**
-   Click **Create credentials**, then select **OAuth client ID**
-   Click **Configure consent screen**
-   For the name, type **GDPR Login**
-   Click **Save**
-   For the application type, select **Web application**
-   Click **Create**
-   For the application name, type **GDPR Webs**
-   Add your OAuth Redirect urls:
    -   Admin - https://{prefix}gdprwebadmin.azurewebsites.net/signin-facebook
    -   Subject - https://{prefix}gdprwebsubject.azurewebsites.net/signin-facebook  
-   Click **Create**
-   Record your client id and secret


