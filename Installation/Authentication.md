# 3rd Party Authentication (Login Only)

Only 3rd party OAuth applications that pass the email claim can be used for the login process.  It is best that you create an application specifically for login versus the actual GDPR actions that the application stub may perform.

## Supported 3rd Party Authentication

-   [Azure Active Directory](Azure.md)
-   [Microsoft Account](Microsoft.md)
-   [Facebook](Facebook.md)
-   [Google](Google.md)
-   [Amazon](Amazon.md)

## OWIN Login with MVC

The Privacy Platform supports OWIN as its login layer.  This means the login redirect will be similar to:

-   {wwwURL}/sign-in-{providerName}

Where provider names are:

-   Azure
-   Microsoft
-   Facebook
-   Google
-   Amazon

## Generic Redirect URL

When an access token on behalf of a user is required, the login endpoign will not be used and instead a common endpoint will be:

-   {wwwURL}/Home/OAuthAuthorize

## Other Redirect URL considerations

In most cases, 3rd party applications will support multiple or wildcard redirect urls.  However, in some cases, you may find you will have to create both a login application for the consumer web and a login application for the admin web.  Since most installation will utilize Microsoft Azure AD (which supports multiple root domain redirect urls), you likely will not have to deal with this lack of true OAuth support.