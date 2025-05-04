Step-by-Step
Here’s how I solved my first CTF:

Step 1: Open the PCAP file
When I first opened the PCAP file in Wireshark, I was scrolling through a lot of packets and didn’t notice packet number 4 at all. After about 5 minutes, I finally took a closer look at it — and it caught my attention.

It showed something interesting: a username root and password toor. That definitely stood out, so I decided to follow the TCP stream.
![ctf1](https://github.com/user-attachments/assets/68682eac-9f48-4075-b8ee-69199322bec2)


Step 2: Follow the TCP Stream
When I followed the TCP stream, it revealed another packet — and this time the answer was literally in front of me. On the right side, it showed the flag in plain text: picoCTF...

This was my first time using Wireshark, so I wasn't sure what to do. I copied the encoded-looking text and pasted it into CyberChef to try decoding it. Turns out, I didn’t need to — the flag was already visible in Wireshark the whole time 😅.

Lesson learned: always read carefully before overthinking it.
![ctf sc 2](https://github.com/user-attachments/assets/8d2c3617-ba94-4f5f-8996-f692f21bed29)

  Summary
Opened PCAP file

Found credentials in packet 4

Followed the TCP stream

Found the flag in clear text

Overcomplicated it with CyberChef 😅

This was my first CTF, and it was a great learning experience! On to the next one 🔥

