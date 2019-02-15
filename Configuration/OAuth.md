# OAuth Applications

For user login, oauth based authentication to 3rd party platforms is the preferred method so as not to store any user password hashes.  The system support non-3rd party authentication, and utilizes strong, high-workfactor hashing mechanisms in doing so.

Due to the wide range of OAuth support of some 3rd party systems (such as allowing multiple redirect URIs or other obscure "features" such as not sending an email claim), not all 3rd party systems are supported for authentication.  

However, OAuth can be utilized to make the appropriate API calls in the event an API exists for a particular application.  You can Bring Your On Application (BYOA) or you can utilize the applications provided by the core privary platform.  

In the case of on-premises installs, you must setup all the applications using a corporate account.

## Supported Login Applications

### Microsoft Azure AD

### Microsoft Account

### Facebook

### LinkedIn

### Amazon

### Google