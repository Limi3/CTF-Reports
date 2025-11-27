Hello Long Time No See today we are going to do the pickle rick tryhackme ctf
So first off we run a nmap scan : sudo nmap -sS -A -T5 [ip addr] > output.txt
<img width="1900" height="409" alt="image" src="https://github.com/user-attachments/assets/7dc14e36-b770-4d9e-972d-f4fd2ff535c9" />
so it tells us that port 22 and port 80 is open so now we now if i go back to my browser and paste ip address i can confirm a web server is running
<img width="1164" height="564" alt="image" src="https://github.com/user-attachments/assets/4d6501d9-0649-42d8-aa7f-145b096792a0" />
if i view the page source i can see an internal command
<img width="1695" height="834" alt="image" src="https://github.com/user-attachments/assets/be9bc8f9-ea48-44af-b4b1-a953daac8ad3" />
this gives us a username so that means this web server has a login page too
so now i'll use gobuster to find more information about this web server
<img width="1893" height="98" alt="image" src="https://github.com/user-attachments/assets/9c61cebb-6292-43d4-933c-50707c8aed43" />
after the gobuster command has been completed we can see the hidden files in the dir's
<img width="1109" height="339" alt="image" src="https://github.com/user-attachments/assets/58d78ea7-3923-45f9-bd08-cf34ab989ef6" />
now i go to /assets but there is nothing there i dont get much information so we move to another dir
lets go to /login.php 
<img width="1111" height="462" alt="image" src="https://github.com/user-attachments/assets/5c3d1a0f-2a8d-435d-846b-89cef93f4cfa" />
this is the login.php but we dont know the password yet just the username so lets dig more
lets go to robots.txt
<img width="423" height="154" alt="image" src="https://github.com/user-attachments/assets/02692aaf-56f7-4737-8858-38e77676f1e0" />
here we can see a text 
i can check if this is the password.
and it was the password now we are in
<img width="760" height="227" alt="image" src="https://github.com/user-attachments/assets/9fcc7b28-f57a-40be-aadd-cb3bb268cdfa" />
the potions,creatures,potions,beth clone notes dont give us any information at all
so we go to the command panel and im guessing this is a linux command field so if i type pwd and click on execute i can confirm my command got executed successfully the output: /var/www/html
so lets run a quick list(ls)
<img width="1591" height="496" alt="image" src="https://github.com/user-attachments/assets/45f8f6b0-dfa1-4977-882c-b9ee96b13260" />
i get a list of all the files that are inside this dir and also the supersecret text file
so let me try to cat out the content
<img width="1169" height="768" alt="image" src="https://github.com/user-attachments/assets/383afde5-e84d-4b35-87b0-955188d9cdbb" />
it dosent let us 
let me try using the command more.
it dosent let us so let me use less
<img width="634" height="520" alt="image" src="https://github.com/user-attachments/assets/d0d9ff22-b62c-4fce-a5ae-179094d8f896" />
i can see the command less works and this is the answer to the first ingredient 
now lets try to read the content of clue.txt
<img width="833" height="464" alt="image" src="https://github.com/user-attachments/assets/1bc8821a-557e-403f-8724-f75833f5f69b" />
it tells me to look around the file system for other ingredient.
i can check what do we have under the root directory with ls /
it gives us the typical linux file system
we can check what users are in the home directory
<img width="603" height="340" alt="image" src="https://github.com/user-attachments/assets/7d27dd0d-eb6d-48b6-9d81-863bd47b0910" />
and we can see theres a user named rick 
lets check what is under the user rick's home directory
<img width="329" height="318" alt="image" src="https://github.com/user-attachments/assets/0f600111-7a4a-4bdb-9182-a25085a834fe" />
so ill copy the name of the file and read it with less
less/home/rick"second ingredients" add the name of the file in double quotation
<img width="338" height="223" alt="image" src="https://github.com/user-attachments/assets/02631767-0aca-4077-8142-b4e3edea78c7" />
and we get the answer to the second question/ingredient
now lets find the last ingredient, im guessing the last ingredient will be under the root directory
ls /root/ and obviously we need root permission for this
so lets check what permission we have with the sudo command
<img width="914" height="324" alt="image" src="https://github.com/user-attachments/assets/ea31e80e-a308-4ba7-b35d-42a0798f1d8b" />
we can basically type any command without a password with sudo
so if i type sudo ls/root/
<img width="561" height="321" alt="image" src="https://github.com/user-attachments/assets/985ca1fd-09a8-4810-818f-6d9887c5336e" />
we have the 3rd ingredient so lets read the file 3rd.txt
sudo less /root/3rd.txt
<img width="397" height="207" alt="image" src="https://github.com/user-attachments/assets/61d5d444-bb67-4180-9c3e-5ab6aa4c6239" />
and we were successfull
We have completed the challenge
however there is a better and faster way to do this challenge 
we could have had direct access to this machine with a reverse shell 
This is the end of this ctf i hope that you liked it and i'll cya on the next one Goodbye!












