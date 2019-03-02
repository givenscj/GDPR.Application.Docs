# Applications

The Privacy Platform supports many different applications out of the box.  A tenant may choose to create any number of applications or upload new application templates provided their subscription level will allow them to do so.

## Types of Applications

There are two types of applications in the system:

-   Redirect:  These applications simply redirect a user to an application page where they will send a request to that application directly.
-   Non-redirect:  These are applications that will handle the requests via the platform via automated means.

### Out of Box

There are severl types of applications provided out of the box.  Depending on your subscription level, you will be allowed to create one or more of these applications.

### Importing and Exporting

If you need to backup an application before you make major changes to the settings, you can export the application.  If something doesn't work, you can reimport the application again.

## Creating a new Application

Depending on your subscription or license level, you will be able to create any numerous types of supported applications.  Some applications are more complex than others and the time it took to develop and get it to work was signifcant costs.  Applications are broken into tiers based on this complexity of development:

-   Tier 1
    -   All Redirect applications
-   Tier 2
    -   All applications that are not redirect or specifically called out as Tier 3
-   Tier 3
    -   Custom Applications (REST and Windows Service)
    -   Office 365
    -   Dynamics
    -   SalesForce

## Exporting and Importing Applications

For backup and restore purposes, you can export and import applications.  This can also be used to ensure you can get back to a good state in case you change the properties and break something.

## Basic Properties

Basic properties are properties that all applications have.  The include:

-   TODO

## Specific Properties

Each application can have specific properties that guide its function.  In some cases, an application may ask for a username/password, in other cases, a simple API key.

## Actions

Each application supports a variety of actions.  

## Reports

## Uploading Application Templates

You can upload new application templates based on your own custom internal applications.  These application stubs are created using the Privacy Central SDK.  Unfortunately, these applications can only be designed using basic .NET Framework classes for security reasons and must go through a verification process with Privacy Central developers and architects to ensure system stability.

A more flexible way of connecting your applications to the platform is to utilize the windows service application type to send message to on-premises services for processing.

# Next Step ([Operation](../Operation/readme.md))

Now that you have some applications created and configured, you can now start inviting users to make requests.  As part of this process, you will need to handle and montior the requests to ensure that the system is functioning properly.