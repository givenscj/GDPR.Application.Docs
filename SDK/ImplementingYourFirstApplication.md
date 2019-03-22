# Implementing your First Application

This is a high-level of steps you need to implement in order to create your first application stub.  You can also reference the example CRM application in the SDK to see how many of these methods are implemented.

##  Set Basic Properties

-   ShortName
-   LongName
-   Version
-   Template ID

##  Set Search Support Properties

TODO

##  Set GDPR Support Properties

TODO

##  Set export mode

Applications can export records or a link to an export.  If your application supports record export, it can be fed to the approver of a data subject request such that they can modify the data that will be sent back to a user.  

If your application returns a link to an export, an approver can also click the link to review the exported data before it is sent to the data subject.

##  Implement Privacy Methods

The three most important patterns to implement for a privacy application are Query, Consents, Delete and Anonymize.

### Query

The most important aspect of an application.  The ability to find a data subject in your application.  A request may include any of the various types of data that can identify a data subject.  See [Identity Types](IdentityTypes.md).

It is up to you to write the logic that will take the various identities that are sent and determine if a data subject exists in the application or not.

This tends to be where most of the development work will reside.

####    Discovery

Discovery is the process of searching for all data subjects in an application and importing them into the platform.

####    Get Changes

Rather than continually discovering all data subjects each time (which could potentiall be in the 100K, 1M range), you can specific a Change Date.  This date is stored at the application instance level (in the platform) and can be used to make delta queries to the application.

### Consents

Every data subject from which you have data must consent to you having that data.  They must also be presented the opportunity to un-consent to your usage.  This must be an explicit action.  

As part of the import/discovery process, you can specifiy if the data subject has already consented.  

Administrators can later send notifications to those that have not consented to get them to consent.

### Delete

If a data subject requests to be deleted, you must process that request.  As part of processing it, you must determine if you can delete based on the legal requirements of the data records (see Record Types and Policy below).

If all logic passes, then you can successfully delete the user from your application.  If not, then you should respond with the the reasons why which will then be passed to the user for their information.

### Anonymize

Deletion is not the recommnded path in most cases.  The best path for handling a request is to anonymize it.  The justification for this is based on the fact that most applications having reporting tied to them that will be adversly affected.  Consider:

-   Current year reporting
-   Year to year growth metrics
-   Other historical based reporting focused on counts

##  Define Record Types and Record Policy

Record types are logical sets of data types that can have retention or functions applied.  Examples include:

-   User
-   Contact
-   Company
-   Contract
-   etc

Each of these can have a settings that determine if they can be deleted or not.  

##  Application Properties

In most cases, the core application properties should be enough to support your SaaS based application needs, however, for custom applications, you may find you need to add properties to support pointing to multiple instances of that application type.  For example, if you have a MongoDB, you might want to have a connection string, or support development vs production settings for testing purposes.

### Core Application Properties

The following properties are part of the core of which every application will have:

-   TODO

### OAuth Application Properties

When an application implements the OAuth protocol (V2 is preferred), you can implement from the OAuthApplication class.  This class adds additional properties that are required in order for the platform to enable administrators to authorize your application using the core platform client id and secret (FallbackOAuth), or an administrator specifying their own client id and secret.

-   TODO

### Set and Get Properties

Properties can be persisted using the inherited SetProperty and GetProperty methods. 

### Entity Property Definitions

You can control how your properties are displayed in the platform by defining them in the "GetEntityPropertyDefinitions" method.  This will create the definition in the system and then allow users to set and get those properties in the privacy platform UI.

## Authorization

It is likely that every application you build will require some kind of authorization.  Whether that is username/password over Basic HTTP Auth, NTLM, or other application specific means (SQL, OAuth, etc).

### Authorize Method

The implementation of your application authentication happens here.  

### HasValidCredential

TODO

### HasValidOAuthCredentials

TODO

### OAuth

TODO

## TestAPI Method

TODO