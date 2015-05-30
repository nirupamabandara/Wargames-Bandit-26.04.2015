# Wargames-Bandit-26.04.2015
Bandit exercice
Nirupama Bandara- MS13961718

Exercise : Learning Security Concepts through Games offered by the OvertheWire Community

URL: http://overthewire.org/wargames/

Wargames

Wargame in hacking is a security challenge in which one must exploit a vulnerability in a system or application or gain access to a computer system.

Bandit Level 0: Log into game using SSH

Open a SSH connection with bandit.labs.overthewire.org using putty

Host : bandit.labs.overthewire.org

level 0 :
username: bandit0

password: bandit0

logged to level0

![1 banditlevel0](https://cloud.githubusercontent.com/assets/12378369/7897338/f16ee248-06f5-11e5-8edd-60a4896206ba.PNG)


Level 1 Hint: password for the level1 is stored in a file called readme.


![2 loggedtolevel1](https://cloud.githubusercontent.com/assets/12378369/7897382/eb5bb3d4-06f7-11e5-812c-9720df818e34.PNG)

list the files : ls

Open the readme file: cat readme

![3 findpwforlevel1](https://cloud.githubusercontent.com/assets/12378369/7897386/0f221d12-06f8-11e5-9c41-68c6bf2700dd.PNG)

password : boJ9jbbUNNfktd78OOpsqOltutMc3MY1

copy text from putty shell= ctrl + insert

paste text from putty shell= shif +insert

Level 2 Hint: password for level2 is stored in a file called - located in the home directory

![4 findpwforlevel2](https://cloud.githubusercontent.com/assets/12378369/7897393/2c8ecf62-06f8-11e5-88ba-0c6dc9fa911c.PNG)

list the files: ls

output: -
command to open a file named -: cat ./-

password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Accessed level2

![5 loggedlevel2](https://cloud.githubusercontent.com/assets/12378369/7897395/56b32446-06f8-11e5-8bf0-5158a624ac57.PNG)

Level 3 Hint: Password for the level3 is stored in a file called "spaces in this filename"

challenge: Reading a file with spaces in its name

![6 findpwlevel3](https://cloud.githubusercontent.com/assets/12378369/7897396/6df3fc84-06f8-11e5-9a02-3885373ec192.PNG)

commands: ls

output: spaces in this filename

command: cat "spaces in this filename"

![7 loggedlevel3](https://cloud.githubusercontent.com/assets/12378369/7897397/85334b2a-06f8-11e5-8971-96a9f0a7ebd1.PNG)

password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Level 4 Hint: password for the level4 is stored in hidden file in the inhere directory

![8 findpwlevel4](https://cloud.githubusercontent.com/assets/12378369/7897399/a19f8986-06f8-11e5-8352-7e5075f63604.PNG)

list the files: ls

output: inhere

go to inhere directory: cd inhere

view hidden files: ls -la

open a hidden file : cat .hidden

bandit3@melinda:~$ ls

inhere

bandit3@melinda:~$ cd inhere

bandit3@melinda:~/inhere$ ls

bandit3@melinda:~/inhere$ ls -la

total 12

drwxr-xr-x 2 root root 4096 Nov 14 2014 .

drwxr-xr-x 3 root root 4096 Nov 14 2014 ..

-rw-r----- 1 bandit4 bandit3 33 Nov 14 2014 .hidden

bandit3@melinda:~/inhere$ cat .hidden

pIwrPrtPN36QITSp3EQaw936yaFoFgAB


password level4:
pIwrPrtPN36QITSp3EQaw936yaFoFgAB

![9 loggedlevel4](https://cloud.githubusercontent.com/assets/12378369/7897400/b12baa38-06f8-11e5-9998-46b1d5533ee6.PNG)

Accessed level 4

Level 5 Hint: password is stored in the only human readable file stored in the inhere directory.

![10 findpwlevel5](https://cloud.githubusercontent.com/assets/12378369/7897402/cd31f82c-06f8-11e5-8494-c4179440c24b.PNG)

koReBOKuIDDepwhWk7jZC0RTdopnAYKh

bandit4@melinda:~/inhere$ ^C

![11 loggedlevel5](https://cloud.githubusercontent.com/assets/12378369/7897407/e0449e9c-06f8-11e5-98c8-2b323b716101.PNG)

password level5: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

Host : bandit5.labs.overthewire.org

Level6 Hint: password is included in a file stored in the inhere directory, it is in human readable format, size of 1033 bytes and non executable

![12 findpwlevel6](https://cloud.githubusercontent.com/assets/12378369/7897409/f9f9bc64-06f8-11e5-9f8b-b3d687630782.PNG)

password level6 : DXjZPULLxYr17uwoI01bNLQbtFemEgo7

![13 loggedbandit6](https://cloud.githubusercontent.com/assets/12378369/7897412/0ab4b734-06f9-11e5-896d-25c8e7ae18bb.PNG)

Level 6 Hint: stored somewhere in the server and has following properties owned by user bandit7, owned by group bandit6 and 33bytes in size

Host : bandit6.labs.overthewire.org

commands: find / -user bandit7 -group bandit6 -size 33

command : cat /var/lib/dpkg/info/bandit7.password

![14 findpwlevel7_1](https://cloud.githubusercontent.com/assets/12378369/7897417/23f927fc-06f9-11e5-95be-7b247e12a0d1.PNG)
![15 findpwlevel7_2](https://cloud.githubusercontent.com/assets/12378369/7897418/36d58ab4-06f9-11e5-9061-63f8f63e277a.PNG)

Password level7: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

![16 loggedlevel7](https://cloud.githubusercontent.com/assets/12378369/7897422/496e4fd0-06f9-11e5-9c60-0aa9c3a20207.PNG)

Level 7 Hint : password for level 8 is stored in the file called data.txt next to the word millionth

command : cat data.txt | grep millionth

Host : bandit7.labs.overthewire.org

![17 findpwlevel8](https://cloud.githubusercontent.com/assets/12378369/7897424/5fc0cf1a-06f9-11e5-9591-e5059ac9e503.PNG)

password level8: cvX2JJa4CFALtqS87jk27qwqGhBM9plV

![18 loggedlevel8](https://cloud.githubusercontent.com/assets/12378369/7897427/7605aa0c-06f9-11e5-85cb-a1a6b2975e0a.PNG)

Level 8 Hint: The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Host : bandit8.labs.overthewire.org

command: cat data.txt | sort | uniq -u

password level 9: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

![20 loggedlevel9](https://cloud.githubusercontent.com/assets/12378369/7897432/8d738682-06f9-11e5-9062-750f707dc884.PNG)

Level 9 Hint : The password for the next level is stored in the file data.txt in one of the few human-readable strings, beginning with several ‘=’ characters.

![21 findpwlevel10](https://cloud.githubusercontent.com/assets/12378369/7897434/9dd75ac6-06f9-11e5-8777-42f5f953756d.PNG)

Host : bandit9.labs.overthewire.org

command: bandit9@melissa:~$ ls
data.txt
bandit9@melissa:~$ strings data.txt | grep '='

password level 10: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

![22 loggedlevel10](https://cloud.githubusercontent.com/assets/12378369/7897435/b28c25c8-06f9-11e5-880f-b22700f301fd.PNG)

Level 10 Hint :The password for the next level is stored in the file data.txt, which contains base64 encoded data. We need to decode the file.

Host : bandit10.labs.overthewire.org

commands: bandit10@melissa:~$ ls

data.txt

bandit10@melissa:~$ base64 -d data.txt

![23 pwlevel11](https://cloud.githubusercontent.com/assets/12378369/7897436/c4f36500-06f9-11e5-83c2-adb877e99eee.PNG)


password level 11: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

![24 loggedlevel11](https://cloud.githubusercontent.com/assets/12378369/7897438/d754c0a4-06f9-11e5-86cc-1d6c846af2a2.PNG)

Level 11 Hint : The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
Host : bandit11.labs.overthewire.org

bandit12@melissa:/tmp/stw$ cat lost

![25 pwlevel12](https://cloud.githubusercontent.com/assets/12378369/7897440/e8894304-06f9-11e5-9d98-fb0e7d90fb7b.PNG)

The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL</str

![26 loggedlevel12](https://cloud.githubusercontent.com/assets/12378369/7897449/ff6fd358-06f9-11e5-82eb-835e9310e80f.PNG)

![27 findpwlevel13_p1](https://cloud.githubusercontent.com/assets/12378369/7897454/153dbe2a-06fa-11e5-9c0c-a9b9405ad677.PNG)
![28 pwlevel13](https://cloud.githubusercontent.com/assets/12378369/7897457/26763cbc-06fa-11e5-9aa7-2cc5d2a98df9.PNG)

Password level 13: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

![29 loggedlevel13](https://cloud.githubusercontent.com/assets/12378369/7897459/36479154-06fa-11e5-9a4f-50f6361467ba.PNG)

level 13 Hint: This one switches things up a little. The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. We need to borrow an SSH key to move on.

Host : bandit14.labs.overthewire.org

commands:

bandit13@melissa:~$ ssh -i sshkey.private bandit14@localhost

Are you sure you want to continue connecting (yes/no)? yes

andit14@melissa:~$ cat /etc/bandit_pass/bandit14

![30 findpwlevel14](https://cloud.githubusercontent.com/assets/12378369/7897462/4cea3600-06fa-11e5-8c5d-3c61b0e3b1b5.PNG)


password level 14: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

![31 findpwlevel15](https://cloud.githubusercontent.com/assets/12378369/7897467/605b1f10-06fa-11e5-821c-f1cb9f253302.PNG)

Level 15 Hint: The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost. Here we have a lesson in telnet. Basically, we will use telnet to connect to localhost on port 30000 and enter the password while we are still in bandit14’s shell.

Host : bandit15.labs.overthewire.org

commands:bandit14@melissa:~$ telnet localhost 30000 then give the password found in level 14. then we can obtain the password for level 15.

Password level 15: BfMYroe26WYalil77FoDi9qh59eK5xNr

![32 passwordlevel16](https://cloud.githubusercontent.com/assets/12378369/7897473/7ca99bb0-06fa-11e5-9787-f16222d9740c.PNG)

Level 16 Hint:The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption. Now we are using SSL commands. Nothing to it but to do it.

Host : bandit15.labs.overthewire.org

cat /etc/banditpass/bandit15 | openssl sclient -connect localhost:30001 -quiet

Password level 16:cluFn7wTiGryunymYOu4RcffSxQluehd

cluFn7wTiGryunymYOu4RcffSxQluehd

![33 bandit17shell](https://cloud.githubusercontent.com/assets/12378369/7897474/909fd8dc-06fa-11e5-9e30-20210e71cd07.PNG)

![34 bandit17pw](https://cloud.githubusercontent.com/assets/12378369/7897476/a653d3ae-06fa-11e5-8644-46cf2f617a2e.PNG)

Level 17 Hint: The password for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next password, the others will simply send back to you whatever you send to it.

Moving up with our network skills we are introduced to nmap. Let’s run some scans to find the listening server. Note netcat can also do basic port scans. Good to know because many systems have that by default and you may be in a situation where you cannot use nmap.


password bandit 17: kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

Level 18 Hint:
 ![35 bandit19shell](https://cloud.githubusercontent.com/assets/12378369/7897479/c3fdadb2-06fa-11e5-9d83-c27a64930e64.PNG)
 
Host :

Level 19 Hint:

Host :

![36 bandit20pw](https://cloud.githubusercontent.com/assets/12378369/7897485/d5b2562a-06fa-11e5-901b-7b7455b29bdd.PNG)

password level 20: GbKksEFF4yrVs6il55v6gwY5aVje5f0j

![37 bandit2ologgedin](https://cloud.githubusercontent.com/assets/12378369/7897486/e563e6f6-06fa-11e5-9651-ef51d60aa091.PNG)

Level 20 Hint:There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: To beat this level, you need to login twice: once to run the setuid command, and once to start a network daemon to which the setuid will connect.

NOTE 2: Try connecting to your own network daemon to see if it works as you think

Host: bandit20.labs.overthewire.org

![38 findpw21](https://cloud.githubusercontent.com/assets/12378369/7897488/f47a0bd4-06fa-11e5-9cc8-0e83b840d6d9.PNG)

password level 21: gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

![39 loggedasbandit21](https://cloud.githubusercontent.com/assets/12378369/7897492/0b0b185c-06fb-11e5-9b6c-6cb5895dfda7.PNG)

Level 21 Hint:A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Host: bandit21.labs.overthewire.org

![40 pwlevel22](https://cloud.githubusercontent.com/assets/12378369/7897493/1b099706-06fb-11e5-916e-e3d80ea9dc70.PNG)

password level 22: Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI

![41 loggedlevel22](https://cloud.githubusercontent.com/assets/12378369/7897494/2b0d77b2-06fb-11e5-8d15-0067e1d5e412.PNG)

Level 22 Hint:A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Host: bandit22.labs.overthewire.org

![42 pwlevel23](https://cloud.githubusercontent.com/assets/12378369/7897495/370a91d0-06fb-11e5-9792-ff0889fb2860.PNG)

password level 23: jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n

![43 loggedaslevel23](https://cloud.githubusercontent.com/assets/12378369/7897497/48032312-06fb-11e5-86bd-7fd867a7733e.PNG)

Level 23 Hint:

Host: bandit23.labs.overthewire.org





