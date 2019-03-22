# Privacy Platform SDK

The Privacy Platform SDK is a set of Visual Studio projects that allow you to get started developing appliation stubs very quickly.

##  SDK Projects

There are two main projects that drive the SDK.  One is the lower level "Common" project and the other is a sample project that includes some examples of how to build a privacy platform application.

-   GDPR.Common
-   GDPR.SDK

These project contain a plethora of helpful code when working with privacy-first applications.

##  Application Stubs (GDPRApplictionBase)

An "application stub" is an application class that inherits from "GDPR.Common.Application.GDPRApplictionBase".  Inheritance from this base class will provide you with the guided (aka forced) implmentation of methods and properties via abstract methods and interfaces to support the Privacy Central platform.

##  IDataSubjectActions Interface

There are a set of methods that your application should implement to achieve full privacy compliance.  They are:

-   Query (Single Subject)
-   Discover (All Subjects)
-   Update
-   Delete
-   Export (records or output of link to export)

In terms of "triggers", you should be able to handle the following events both into and out of the application:

-   Insert
-   Delete
-   Update

See [Data Subject Action Pattern](DataSubjectActionPattern.md)

##  Personal Data (Name) Searches

In general, we do not recommend that you do auto search on individuals names.  Due to the high level of uncertainty and fraud related to name based searchs, you should only use this as a reference point.  Items like email, phone and address have a much higher propbability of being valid.

See [Name Search Problem](NameSearch.md)

##  Phone Number Problem

One of the biggest challenges you will have with GDPR is the phone number problem.  Most SaaS and server based applications do not force a phone number format.  This means you will need to execute a search for all patterns of a phone number, which currenlty sits around 40 permutations.

See [Phone Number Problem](PhoneNumberProblem.md)

##  Search Support Parameters

An application must tell the platform what it supports in terms of search. An applications should be able to support at least email search at a minimum.  But it can also support search based on other verified (or unverified) data subject identities.  These can include:

-   Personal (First and Last names)
-   Email
-   Phone
-   Address
-   Social
-   Government or Employment Identity
-   Biometerics
-   Dna
-   IP Address
-   Device

Although not all applications can easily support biometric or dna searching, we anticipate this will be something people will do in the near future.

See [Idenitity Types](IdentityTypes.md).