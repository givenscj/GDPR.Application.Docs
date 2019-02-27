# Azure Setup

Perform the following steps to get the information you need to setup your Install Utility configuration file.

## Open Azure Portal

-   Open your [Azure Management Portal](https://portal.azure.com)
-   CLick **All resources**
-   Search for **Subscription**, then select **Subscriptions**
-   Record your Subscription ID
-   In the right hand menu, click **Azure Active Directory**
-   Click **Properties**
-   Record your Directory Id (also called your TenantID)

## Create an application registration

-   Click **App registrations**
-   Click **New application registration**
-   Type a name for your application, something like **Privacy Central Admin App**
-   For the sign-on URL, type **https://localhost:12345**
-   Click **Create**

## Copy the Application Id and create a secret

-   Record the **Application ID** from the blade dialog
-   Click **Settings**
-   Click **Keys**
-   In the **Passwords** section, type a name for your key such as **GDPRKey1**
-   For the duraction, select **2 years**
-   Click **Save**
-   Record the newly created application password

## Setup application permissions

-   Click **All resources**
-   Search for **Subscription**, then select **Subscriptions**
-   Select your subscription
-   Click **Access control (IAM)**
-   Click **Add**, then select **Add role assignment**
-   For the role, select **Owner**
-   In the **Select** textbox, search for your new application, select it
-   Click **Save**

    >NOTE: It is likely you may want to configure the application to only be the owner of a specific resource group.  In that case, pre-create your resource group and then assign it **Owner** permissions to it

## Configure your InstallUtil configuration file

-   Copy the **Tenant Id** to the **TenantID** json value
-   Copy the **Subscription Id** to the **SubscriptionID** json value
-   Copy the **Resource Group Name** to the **ResourceGroup** json value
-   Copy the region your resource group will be in (or has already been created in) to the **Region** json value
    - These will be the same enumeration values as [here]()
-   Copy the **Azure Client Id** to the **AdminAzureClientId** json value
-   Copy the **Azure Client Secret/Key** to the **AdminAzureClientSecret** json value