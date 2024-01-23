[![OTPless](https://d1j61bbz9a40n6.cloudfront.net/website/home/v4/logo/white_logo.svg)](https://otpless.com/platforms/javascript)

# Javascript Demo

## Steps to add OTPless SDK to your Website

1. **Copy the HTML code provided below into your project's HTML file.**

    > A modal where otpless login page will load as a modal.

    ```html
    <!DOCTYPE html>
        <html lang="en">
        <head>
            <!-- Include meta tags and title -->
        </head>
        <body>
            <!-- A modal where otpless login page will load as a modal -->
            <div id="otpless-login-modal">
        
              <!-- Add div to load otpless login page with id as given below  -->
              <div id="otpless-login-page"></div>
        
            </div>

            <!-- button to load otpless login page -->
            <button type="button" id="login-button">Login</button>
        
            <script>
              // JavaScript code provided in further steps
            </script> 

        </body>
    </html>

    ```

2. **Add this javascript code to open OTPless sign in page as a modal**

   > function to open otpless loginPage as a moidal
    ```html
        function openOtplessLoginPage() {
            loginModal.style.display = "flex";
            const scriptElement = document.createElement("script");
            scriptElement.type = "text/javascript";
            scriptElement.setAttribute("cid", "YOUR_CID_HERE") //Replace with your cid
            scriptElement.src = "https://otpless.com/auth.js";
          
            document.getElementById("otpless-login-page").appendChild(scriptElement);
            loginButton.style.display = 'none';
          }
    ```

3. **Add this javascript code to Close OTPless sign in page modal**

   > function to close OTPless sign in page modal
    ```html
    function closeOtplessLoginPage() {
        loginModal.style.display = "none";
        // document.getElementById("otpless-login-page").innerHTML = "";
        loginButton.style.display="block";
      }
    ```
4. **Customize the otpless function to handle the user data after successful login. The provided example logs the data to the console, stores it in localStorage, and redirects to another page.**

    > Implement the following javascript code to retrive the **user data** upon successful authentication of the user.

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
>Customize the otpless function to meet your specific requirements for handling user data after login.
    
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
