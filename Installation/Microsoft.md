# Microsoft Setup

A Microsoft application is only used for authentication. 

>NOTE:  You should use an Azure AD application rather than the older Microsoft Developer portal.  However, if you choose this path, it works as well.

## Configure Microsoft Login

-   Open the [Microsoft Developers Portal](https://apps.dev.microsoft.com/)
-   Click **Add an app**
-   Type a name, click **Create Application**
-   Record the Application ID
-   Click **Generate New Password**
-   Record the password

##  Configuration File Update

Update the configuration file with the following values:

-   AzureClientId : The value you recorded above
-   AzureClientSecret : The value you recorded above
