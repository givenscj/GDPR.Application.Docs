# Installation

The Privacy Platform installer requires a simple Azure AD Application and Secret in order to create all the necessary resources a new instance will need.

## Pre-requisities

-   Azure AD Application
-   Azure Management Permissions
-   Setup configuration.json
-   3rd Party Login Applications

## Setup Azure Subscriptions

In order to run the Install utility you will need to do some setup in yoru Azure tenant. 

-   [Configure your Azure tenant](AzureSetup.md)

## Running the Install Utility

-   Update the configuration file
-   Run the [InstallUtil.exe](InstallUtil.md) command line tool

## Setup the database

- [Initialize the database](Database.md)

## Configure 3rd Party Authentication

In most cases, you will find it easier and more secure to not managed user password hashes.  In order to do this, you must use 3rd party authentication that passes email claims.  Certain providers have stopped sending the email claim (such as Twitter) and cannot be used for authentication.  These providers are subject to change in the future.

- [Configure 3rd Party Auth](Authentication.md)