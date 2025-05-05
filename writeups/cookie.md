CTF Writeup: Cookie Search
This was my third CTF challenge, and it started off with a simple interface—a search bar that seemed to revolve around cookies:
![Screenshot 2025-05-05 162308](https://github.com/user-attachments/assets/fbc29424-0500-42de-bf55-c0fac8267b27)
After submitting a few inputs, I got a message saying:
![Screenshot 2025-05-05 162322](https://github.com/user-attachments/assets/ffe208af-6b52-4aa9-a92d-732380bdbb06)
So I opened DevTools → Application → Cookies and started experimenting with the cookie values. At first, I was too tired to test all of them and ended up wasting about 30 minutes just aimlessly trying random values (lesson learned).

Later, I came back with a fresh mindset and tried going through the values one by one. Eventually, when I hit 18, I was rewarded with the flag.
![Screenshot 2025-05-05 162358](https://github.com/user-attachments/assets/f5df512e-b16e-40d6-b647-c7b39c30746c)

Persistence paid off on this one. On to the next CTF!
