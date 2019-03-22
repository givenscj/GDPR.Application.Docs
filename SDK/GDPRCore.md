# GDPR Core

GDPR Core is an abstracted way of calling various methods of the core product.  Because we want on-premises applications that run outside the core to behave in the same way, the interface provides you the ability to override how your applications runs locally.

##  IGDPRCore

The IGDPRCore interface allows your application to behave like it is running in the SaaS or hosted platform option.  This abstraction allows the SDK to function in the way it does such that an application can run either via SaaS or on-premises properly.  

Some examples of what an application will want to do with differing functionality is:

-   Logging - An application can call the Log methods and depending on its execution context, the log can go to where the application developer wants it to on-premises or it will be routed to the Application log in the platform.
-   Upload a Blob - When your appication exports a set of data subject records, it needs to put it somewhere and forward a link to the platform.
-   Getting and Saving Properties - When a property is retrieved or saved when running in the SaaS platform, the properties are persisted to the data store.  When running locally, you may want to persist to the configuration.json file or where ever your property bag data store is located

##  GDPRCore

The GDPRCore class must be instantiated at application load time via the "Current" property.  Failure to do so will cause runtime exceptions later in application execution.

### Application

GDPR.Common.Core.GDPRCore is the basic on-premises helper class to support your application IGDPRCore context.  You are free to modify this in your application designs, just be aware that some methods are used to communicate with the platform via sending of messages.