﻿[![OTPless](https://d1j61bbz9a40n6.cloudfront.net/website/home/v4/logo/white_logo.svg)](https://otpless.com/platforms/javascript)

# Javascript Demo

## Steps to add OTPless SDK to your Website
1. **Create an App in [OTPless dashboard](https://otpless.com/dashboard/app) and copy the APP ID**
2. **Add OTPLESS Sign in**

    > Add the following code to your sign up/ sign in page where you want to embed your sign in functionality.

    ```html
    <div id="otpless-login-page"></div>
    <script type="text/javascript" src="https://otpless.com/auth.js" data-appid="PASTE_YOUR_APPID_HERE"></script>
    // Replace with your cid
    ```

3. **Retrieve User's Information**

    > Implement the following function to retrive the **user data** upon successful authentication of the user.

    ```html
    <script type="text/javascript">
        function otpless(otplessUser) {
            alert(JSON.stringify(otplessUser));
        }
    </script>
    ```

### Codes of Interest

- [OTPless-login-page](loginpage.html#L11) - login page
- [OTPless-script](loginpage.html#L13) - script to integrate OTPless SDK
- [Callback function](loginpage.html#L17) - callback function to retrieve user data

> Received User Data Format

```js
// otpless user Format
{
    "token": "xxxxxxxxxxxxxxxxxxxxxxxxxxxx",
    "timestamp": "YYYY-MM-DD HH:MM:SS",
    "timezone": "+XX:XX",
    "mobile": {
        "name": "User Name",
        "number": "User Mobile Number"
    },
    "email": {
        "name": "User Name ",
        "email": "User Email"
    }
}
```
## Usage
> Prerequisites **Any Code Editor**
  - Clone this repository
  - Open the code in any code editorand run on localhost
  - Switch branches to check out available options to integrate OTPless SDK in your project.
