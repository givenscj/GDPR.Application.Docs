# Amazon Setup

A Amazon application is only used for authentication. 

## Configure Amazon Login

-   Open the [Amazon Developers Portal](https://developer.amazon.com/home.html)
-   Click **Sign In**, if you do not have an account click "Create your Amazon Developer Account** link and follow the instructions
-   Click **Login with Amazon Console**
-   For the security profile, fill in the text areas similar too:
    -   Profile Name - **GDPR Login**
    -   Profile Description = **GDPR Login**
    -   Privacy Notice = **https://{prefix}gdprwebsubject.azurewebsites.net/Home/Privacy**
-   Click **Save**
-   Click **Show Client ID and Client Secret**
-   Record the values
-   Click the **Manage** icon, then select **Web Settings**
-   For the return urls, type:
    -   Admin - https://{prefix}gdprwebadmin.azurewebsites.net/signin-amazon
    -   Subject - https://{prefix}gdprwebsubject.azurewebsites.net/signin-amazon  
-   Click **Save**

##  Configuration File Update

Update the configuration file with the following values:

-   AmazonClientId : The value you recorded above
-   AmazonClientSecret : The value you recorded above

#Testing

-   Open a browser to your admin site.
-   Click **Login**, on the page you should see the **Amazon** button
-   Click **Amazon**, ensure that you are able to login and redirect back to the site