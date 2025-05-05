 CTF Writeup: Cookie Cracking
This was my second CTF, and here's how I managed to capture the flag.

When I first landed on the login page, I tried entering a random username and password just to see what would happen:
![Screenshot 2025-05-05 134149](https://github.com/user-attachments/assets/efe41af5-effc-4cff-8a60-60e2bc3f350a) 
As expected, it returned an “Access Denied” message. But what caught my attention was the text on the page:
![Screenshot 2025-05-05 134201](https://github.com/user-attachments/assets/df9e8dac-2314-4bce-89ed-c284a0e4cde9)
So I opened up my browser’s developer tools and checked the cookies. One of the cookie values stood out—it looked encoded:
![Screenshot 2025-05-05 134254](https://github.com/user-attachments/assets/14a2b2b8-7942-4d8a-8afc-d61b88c317aa)
I copied it and decoded it using base64decode.org. That’s when the real content revealed itself—and with it, the flag.

That’s it for this challenge. See you in the next CTF!

