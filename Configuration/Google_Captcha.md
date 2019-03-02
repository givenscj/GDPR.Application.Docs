# Google Captcha

Some operations can be highly sensitive or prone to abuse.  To prevent automated create of data or requests, captcha is used in various parts of the privacy platform

## Setup

-   Open the [Google reCAPTCHA Portal](https://www.google.com/recaptcha/intro/v3.html)
-   Click **Admin console**
-   Click the **+** sign to create a new key set
-   Select **reCAPTCHA v2**
-   Select **I'm not a robot** checkbox
-   For domains, type your domains
-   Check the **Accept the reCAPTCHA Terms of Service** checkbox
-   Click **Submit**
-   Record the site key and secret

## Configuration

-   Open the configuration file
-   Copy the following values:
    -   **recaptchaPublicKey** as site key
    -   **recaptchaPrivateKey** as site secret
    -   **recaptchaApiVersion** as **2**