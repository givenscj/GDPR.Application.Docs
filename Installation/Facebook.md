# Facebook Setup

A Facebook app can be used for several differnt things, with the most common being to allow login to the privacy server.  Other actions include:

-   Login / Authentication
-   Sending Direct Messages for Application Notifications

## Configure Facebook Login

-   Open the [facebook developers portal](https://developers.facebook.com)
-   Click **Get Started**
-   For the app name, type **GDPR Login**
-   Enter your contact email
-   Click **Next**, follow the prompts to get to the application page
-   Once on the application page, select the **Facebook Login** product by clicking **Set Up**
-   For the platform, select **Web**
-   Enter the Site Url, click **Save**, then click **Continue**
-   On the right side navigation, click **Settings** under the **Facebook Login** product
-   Add your OAuth Redirect urls:
    -   Admin - https://{prefix}gdprwebadmin.azurewebsites.net/signin-facebook
    -   Subject - https://{prefix}gdprwebsubject.azurewebsites.net/signin-facebook  
-   Click **Save Changes**
-   Under the **Dashboard** area, click **Settings**, then select **Basic**
-   Record the **App ID**
-   Record the **App Secret**

##  Configuration File Update

Update the configuration file with the following values:

-   FacebookClientId : The value you recorded above
-   FacebookClientSecret : The value you recorded above

#Testing

-   Open a browser to your admin site.
-   Click **Login**, on the page you should see the **Facebook** button
-   Click **Facebook**, ensure that you are able to login and redirect back to the site