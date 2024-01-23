[![OTPless](https://d1j61bbz9a40n6.cloudfront.net/website/home/v4/logo/white_logo.svg)](https://otpless.com/platforms/javascript)

# Javascript Demo

## Steps to add OTPless SDK to your Website

1. **Add OTPLESS Sign in**

    > Add the following code to your sign up/ sign in page where you want to embed your sign in functionality.

    ```html
    <div id="otpless-login-page"></div>
    <script type="text/javascript" src="https://otpless.com/auth.js" cid="YOUR_CID_HERE"></script>
    // Replace with your cid
    ```

2. **Retrieve User's Information**

    > Implement the following function to retrive the **user data** upon successful authentication of the user.

    ```html
    <script type="text/javascript">
        function otpless(otplessUser) {
            alert(JSON.stringify(otplessUser));
        }
    </script>
    ```

### Codes of Interest

- [OTPless-login-page](onclickbutton.html#L14) - login page
- [OTPless-script](onclickbutton.html#L29) - script to integrate OTPless SDK
- [Onclick-button](onclickbutton.html#L19) - button to open otpless login page as modal
- [Open-modal-function](onclickbutton.html#L27) - function to open otpless login page as modal
- [close-modal-function](onclickbutton.html#L39) - function to close otpless login page modal
- [Callback function](onclickbutton.html#L50) - callback function to retrieve user data

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
