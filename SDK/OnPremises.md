# On-Premises Applications

If you have an on-premises application (which most organizations will), you will want to integrate this into the privacy platform.  You can achieve this using the basic application stub wrapper, which will then run in the context of the downloadable windows service proxy application.

This windows service will wrap your application stub using the settings provided in the privacy central platform portal (event hub endpoint and PGP private key/password).

Messages will be automatically processed (abstracted from your application logic) by the windows service and sent to your application based on the configuration.json and the settings within that drives that specific application.

You can have any number of these services running at any time.  But your tenant subscription must be licensed for the number of applications that you will be supporting.  See [Licensing](Licensing.md).

## Windows Service Proxy

The windows service proxy will monitor the platform application event hub and send messages to your application, additionally it will send responses to the platform via the same event hub.  Configuration of the windows service is as simply as downloading the PGP key and adding configuration.json file settings.

##  Event Hub Architecture

Each time you create a new Windows Service based application in the portal, a new public/private PGP key will be created.  It is your responsiblity to save the private key with its password such that you can send encrypted and signed messages via the windows service proxy application.

##  Message Security

Messages between the platform and your on-premises applications are secured using PGP public/private keys.  These keys ensure that the messages are encrypted and signed such that your application and the platform can ensure the validity of the messages for processing.

These keys can be "rolled" at any time using the privacy application admin/tenant portal.  The ability to "roll" a keey is important if you think that your application keys have been compromised.

Application level keys that are rolled take effect immediately.  This means any messages that are recieved by the core will be dropped as invalid.  Be sure that all messages have been processed before rolling your key, otherwise you may need to re-execute incoming and outgoing messages that did not process.  

See [Error Logging](ErrorLogging.md) for more information.