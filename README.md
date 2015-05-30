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

Level 1 Hint: password for the level1 is stored in a file called readme.

list the files : ls

Open the readme file: cat readme

password : boJ9jbbUNNfktd78OOpsqOltutMc3MY1

copy text from putty shell= ctrl + insert

paste text from putty shell= shif +insert

Level 2 Hint: password for level2 is stored in a file called - located in the home directory

list the files: ls

output: -
command to open a file named -: cat ./-

password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Accessed level2

Level 3 Hint: Password for the level3 is stored in a file called "spaces in this filename"

challenge: Reading a file with spaces in its name

commands: ls

output: spaces in this filename

command: cat "spaces in this filename"

password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Level 4 Hint: password for the level4 is stored in hidden file in the inhere directory

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

Accessed level 4

Level 5 Hint: password is stored in the only human readable file stored in the inhere directory.


koReBOKuIDDepwhWk7jZC0RTdopnAYKh

bandit4@melinda:~/inhere$ ^C

password level5: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

Host : bandit5.labs.overthewire.org

Level6 Hint: password is included in a file stored in the inhere directory, it is in human readable format, size of 1033 bytes and non executable

password level6 : DXjZPULLxYr17uwoI01bNLQbtFemEgo7

Level 6 Hint: stored somewhere in the server and has following properties owned by user bandit7, owned by group bandit6 and 33bytes in size

Host : bandit6.labs.overthewire.org

commands: find / -user bandit7 -group bandit6 -size 33

command : cat /var/lib/dpkg/info/bandit7.password

Password level7: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

Level 7 Hint : password for level 8 is stored in the file called data.txt next to the word millionth

command : cat data.txt | grep millionth

Host : bandit7.labs.overthewire.org

password level8: cvX2JJa4CFALtqS87jk27qwqGhBM9plV

Level 8 Hint: The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Host : bandit8.labs.overthewire.org

command: cat data.txt | sort | uniq -u

password level 9: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
Level 9 Hint : The password for the next level is stored in the file data.txt in one of the few human-readable strings, beginning with several ‘=’ characters.

Host : bandit9.labs.overthewire.org

command: bandit9@melissa:~$ ls
data.txt
bandit9@melissa:~$ strings data.txt | grep '='

password level 10: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

Level 10 Hint :The password for the next level is stored in the file data.txt, which contains base64 encoded data. We need to decode the file.

Host : bandit10.labs.overthewire.org

commands: bandit10@melissa:~$ ls

data.txt

bandit10@melissa:~$ base64 -d data.txt

password level 11: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

Level 11 Hint : The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
Host : bandit11.labs.overthewire.org

bandit12@melissa:/tmp/stw$ cat lost
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL</str

Password level 13: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

level 13 Hint: This one switches things up a little. The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. We need to borrow an SSH key to move on.

Host : bandit14.labs.overthewire.org

commands:

bandit13@melissa:~$ ssh -i sshkey.private bandit14@localhost

Are you sure you want to continue connecting (yes/no)? yes

andit14@melissa:~$ cat /etc/bandit_pass/bandit14

password level 14: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

Level 15 Hint: The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost. Here we have a lesson in telnet. Basically, we will use telnet to connect to localhost on port 30000 and enter the password while we are still in bandit14’s shell.

Host : bandit15.labs.overthewire.org

commands:bandit14@melissa:~$ telnet localhost 30000 then give the password found in level 14. then we can obtain the password for level 15.

Password level 15: BfMYroe26WYalil77FoDi9qh59eK5xNr

Level 16 Hint:The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption. Now we are using SSL commands. Nothing to it but to do it.

Host : bandit15.labs.overthewire.org

cat /etc/banditpass/bandit15 | openssl sclient -connect localhost:30001 -quiet

Password level 16:cluFn7wTiGryunymYOu4RcffSxQluehd

cluFn7wTiGryunymYOu4RcffSxQluehd

Level 17 Hint: The password for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next password, the others will simply send back to you whatever you send to it.

Moving up with our network skills we are introduced to nmap. Let’s run some scans to find the listening server. Note netcat can also do basic port scans. Good to know because many systems have that by default and you may be in a situation where you cannot use nmap.

password bandit 17: kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

Level 18 Hint:

Host :

Level 19 Hint:

Host :

password level 20: GbKksEFF4yrVs6il55v6gwY5aVje5f0j

Level 20 Hint:There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: To beat this level, you need to login twice: once to run the setuid command, and once to start a network daemon to which the setuid will connect.

NOTE 2: Try connecting to your own network daemon to see if it works as you think

Host: bandit20.labs.overthewire.org

password level 21: gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

Level 21 Hint:A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Host: bandit21.labs.overthewire.org

password level 22: Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI

Level 22 Hint:A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Host: bandit22.labs.overthewire.org

password level 23: jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n

Level 23 Hint:

Host: bandit23.labs.overthewire.org





