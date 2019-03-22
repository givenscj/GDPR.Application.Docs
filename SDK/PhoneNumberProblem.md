# Phone Number Problem

Not all phone numbers are created equal.  Unfortunately, most developers were lazy and did not enforce standards based entry or parsing into phone number fields.  This presents a rather large problem when it comes to implement privacy legislation.

##  Phone Number Permutations

We have provided a method in the BasePhone class that will create all the permutations of a phone number.  We then use these permutations to execute searches in the target application to see if a users exists.

When a data subject has multiple phone numbers, this essentially mutiples the work load by the same factor.  This can cause considerable strain on the target system.

For example:

Phone number is entered as 206.555.1234 in the system with no normalization.  The standard phone format is +12065551234.  We now have to search for any of the following:

-   206 555 1234
-   206-555-1234
-   (206) 555-1234
-   (206) 555 1234
-   And so on...

##  Solving the problem

### Searching all Permutations

At the tenant level, an application can be enabled to perform the full permutation space of phone search.  This can cause a large load against your target system in terms of search queries and CPU processing.  

### Phone Normalization (Data Source)

Additionally, you can also implement the "PhoneNormalization" method that can parse and normalize the phone numbers in your data subject records.  

Once you have verified that all phone numbers are normalized, you can disable the permutation phone searching.

This is the perferred method of solving the phone number problem.

