# Install Utility

The Install Utility will create all the needed resources in your Azure tenant.  This includes deploying the Azure Web Apps and database.

## Download the Install Utility

Ask your partner or privacy platform representative for access to the platform download utility.  For a list of ceritied partners, reference this [list](./Partners.md).

## Update the Configuration File

All privacy platform services utlize the same basic configuration file.  This file is a json file that contains the basic information about your Azure services.  At a minimum you will need to add the following items:

-   Azure Application Client Id
-   Azure Application Client Secret
-   Azure Subscription
-   Azure Resource Group

Once you have preformed the install, all configuration values will be stored in the Azure Key Vault.  The Configuration file can then be fully deleted unless you would like to override your key vault settings.

## Run the InstallUtil

After you have updated your configuration file, run the InstallUtil.exe utility in the same directory as your configuration file.

## Verify the Following

A succesful installation will be verified by doing the following:

-   Open your [Azure Portal](https://portal.azure.com)
-   Your should see something similar to the following:

TODO

## Items created during Installation

-   Resource Group
-   Azure Application(s)
-   Azure Storage Account
-   Event Namespace
-   Event Hub(s)
-   SQL Server
-   SQL Database
-   Key Vault
-   Web Apps (Admin, IVR, Consumer)
-   Congnitive Services (Face, Translation, OCR)
-   Search

