Hello, this is the Logon CTF challenge, and here's how I solved it:

First, I'm greeted with a login page:
![Screenshot 2025-05-07 140528](https://github.com/user-attachments/assets/867d2b45-037a-4cb6-8da0-71e601208def)
I entered some test credentials, and upon logging in, I was shown this message:
![Screenshot 2025-05-07 140552](https://github.com/user-attachments/assets/0611f0cb-b5db-4479-8cbe-9fd50076a37e)
Next, I opened the browser's developer tools and navigated to Inspect → Application → Cookies. There, I noticed a cookie with a key named admin, and its value was set to false.
![Screenshot 2025-05-07 140610](https://github.com/user-attachments/assets/93d3b085-37e8-404a-a0cc-852a4de3faeb)
I changed the value of admin to true, refreshed the page, and the flag was revealed:
![Screenshot 2025-05-07 140620](https://github.com/user-attachments/assets/48fbbc7d-92ef-45b3-9798-25e4e922155b)
