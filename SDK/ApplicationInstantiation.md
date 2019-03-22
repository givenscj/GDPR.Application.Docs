# Application Instantiation

Once an application stub has been created, it can be packaged as an assembly and uploaded to the Privacy Central platform (any modality - SaaS, Hosted or On-premises).

##  Registration

Upon upload, the assembly will be checked for basis .NET Framework dependencies.  Anything that does not adhere to basic .NET classes will be automatically denied.  For the core SaaS platform, the application must be approved to be uploaded and utilized, which required a source code review and compilation by Privacy Central Architects.  

The platform is highly secure and sensitive so their are no exceptions to this policy.

In terms of hosted instances or on-premises, any administrator can upload an assembly and make it a part of the available set of application templates.

On upload, the applications will be interrogated for basic properties (shortname, longname, version, etc) and then be added to the backend database for selection by administrators.

##  Creation

Once an application stub has been registered, you may create instances from it.  Any custom application will be considered a "Tier 3" application and your subscription will be required to support its creation.

See [Licensing](Licensing.md)

##  Instantiation

### Administration Portal

When an application is viewed in the administrator portal, it will execute the following methods:

-   Constructor
-   Init

### Data Subject Portal

When an application is browsed for the possiblity of a data subject request, the following methods and properties are utilized: 

-   Constructor
-   Init
-   All *Supports* properties
-   Class inheritance is evaluated (Is it OAuth based)

##  Configuration



##  Validation

##  Execution

