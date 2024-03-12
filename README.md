[![OTPless](https://d1j61bbz9a40n6.cloudfront.net/website/home/v4/logo/white_logo.svg)](https://otpless.com/platforms/javascript)

# Javascript Demo

## Steps to add OTPless SDK to your Website

1. **Create an App in [OTPless dashboard](https://otpless.com/dashboard/app) and copy the APP ID**

2. **Copy the HTML code provided below into your project's HTML file.**

    > Add the following code to your sign up/ sign in page where you want to embed your sign in functionality.

    ```html
    <!DOCTYPE html>
        <html lang="en">
            <head>
                <!-- Include meta tags and title -->
            </head>
            <body>
                <!-- button to load otpless login page -->
                <button type="button" id="otpless" custom="true">Login</button>
            
                <!-- Add sdk for JavaScript to embed the sign-in functionality where you want -->
                <script type="text/javascript" src="https://otpless.com/auth.js" data-appid="YOUR_APPID_HERE"></script>
            
                <script>
                  // JavaScript code
                </script>
            </body>
        </html>

    ```

3. **Replace the CID**

    > Replace "YOUR_APPID_HERE" in the script with your actual APP ID provided by OTPless.
    ```html
       <script type="text/javascript" src="https://otpless.com/auth.js" data-appid="YOUR_APPID_HERE"></script>
    ```

4. **Retrieve User's Information**

   >Customize the otpless function to handle the user data after successful login. The provided example logs the data to the console, stores it in localStorage, and redirects to another page.
   ```html
   function otpless(otplessUser) {
        // Customize handling of user data after successful login
        console.log(JSON.stringify(otplessUser));
        localStorage.setItem('otplessUserData', JSON.stringify(otplessUser));
        window.location.href = 'otherpage.html'; // Replace with your desired redirection
    }
   ```

### Customization

>You can further customize the behavior and appearance of the OTPless onclick button loginPage by modifying the provided HTML and JavaScript code.
>Adjust the styles of the modal and button to match your application's design.
>Customize the otpless function to meet your specific requirements for handling user data after login.****

### Codes of Interest

- [Button](onclickbutton.html#L11) - to open OTPless floater
- [OTPless-script](onclickbutton.html#L14) - script to integrate OTPless SDK
- [Callback function](onclickbutton.html#L17) - callback function to retrieve user data

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
