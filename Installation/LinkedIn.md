# LinkedIn Setup

A LinkedIn application is only used for authentication. 

## Configure LinkedIn Login

-   Open the [LinkedIn](https://www.linkedin.com/developers/)
-   Click **Sign In**, if you do not have an account click **Join Now** link and follow the instructions
-   Type your username and password, click **Sign In**
-   Click **Create app**
-   Fill in all your information
-   Click **Create app**
-   Record the Client ID
-   In the header, click **Auth**
-   Click the eye icon, then record the client secret
-   Scroll to the bottom of the page, for the return urls, type:
    -   Admin - https://{prefix}gdprwebadmin.azurewebsites.net/signin-linkedin
    -   Subject - https://{prefix}gdprwebsubject.azurewebsites.net/signin-linkedin
-   Click **Update**

##  Configuration File Update

Update the configuration file with the following values:

-   LinkedInClientId : The value you recorded above
-   LinkedInClientSecret : The value you recorded above

#Testing

-   Open a browser to your admin site.
-   Click **Login**, on the page you should see the **LinkedIn** button
-   Click **LinkedIn**, ensure that you are able to login and redirect back to the site