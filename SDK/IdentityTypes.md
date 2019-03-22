# Identity Types

Anything that can uniquely identify data subjects is fair game for inclusion into making your applications privacy compliant.  Some identities are used more than others, and some have a higher verification ability than others.  

##  Name

Basic information like Firstname, Middle name, Lastname and other physical identifiying data (weight, height, eye color, etc).

In the absence of a privacy score, this data is the least reliable in terms of identification and should be assumed to be unverified in a majority of cases.

##  Email

Email is one of the most easily verified forms of identity.  And since it is used in a majority of applications as the username, it presents the fastest and easiest form of search and verification.

A user have have mulitple emails.

##  Phone

TODO

##  Address

TODO

##  Social

TODO

##  Government Identity

TODO

##  Biometrics

TODO

##  DNA

TODO

##  IP Addresses

TODO

##  Devices

TODO

#   Privacy Central Identity Score (Patent Pending)

##  Identity Expiration

By default, all idenitities expire after 6 months.  This is a saftely measure to ensure that users are still active and the identity is still valid.  

For example, people move many times over their lifetime, an address today, may not be an address in the future.  You should consider this in any automated search activities you perform.

Another example, users will switch their phone numbers frequently. Phone numbers can be virtually assigned or physically assigned entities.  Because they can move from device to device or reused after "death", it is important that you validate a user continues to have the same phone number.

You should also consider the fact that the identity may be "reused".  Again, this is a lower probability identity than email, but higher than a "name" search and should be considered in your search activities in the absense of Idnetity Score metrics.

##  Identity Verification

As you can see from above, it is very difficult to ensure that someone is who they say they are.  Only through a combination of multiple validation methods can you truely ensure that a person is that person.  

Knowing this, as an administrator, you can specify how many verified types of identity are required before you will accept a request.  You can also base your decisions based on the Privacy Central Identity Score.

##  Identity Score

As users add more information, the likely-ness that they are who they say they are increases.  If a user choose to pursue multiple layers of identity verification, we will generate a propritary score which you can base your automated request approval from.

The score ranges from 0 to 100.  Although the actual method and algorithm we use is secret, we can present you with a generic sense of what scores you could expect:

-   0:  Someone who has simply registered but not validated any form of identity
-   0-15:   Someone that has registerd, signed in and has validated themselves by at least one method
-   15-25:  Someone that has validated at least two identity types
-   25-50:  Someone that has validated at least three identity types
-   50-75:  Someone with four types, wich specific types being higher in value than others
-   75-100: A person that has taken every measure possible to verify their identity.  These individuals would be ones where you have a higher trust in the "Name" identity than any other score level.