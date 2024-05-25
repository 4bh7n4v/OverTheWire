The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220.  
ssh banditX@bandit.labs.overthewire.org -p 2220 states to connect Secure Shell of User:Bandit Host:"bandit.labs.overthewire.org" -p stands for port X stands for the level
## Level-0
The Task is to log into the SSH of the given details with Username:bandit0 password:bandit0
## Level-1
The Password is Hidden in the directory to find content of present working directory we can use "ls" command set for listings.   
To Read the content from a text file or metadata of the exicutable file The "cat <filename>" command.  
To move from One Directory to Other we use "cd <filename>" stands for Change Directory.  
Password: "NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL"
## Level-2
The present Working Directory Contains the file "-" Since special character cant be accessed as filename.  
prefix "./" is used which stands for excute file it defines the special character of file as datatype file.  
password:"rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi"  

## Level-3
Spaces in the file name seems to be work as different Directories to make it as Single Directory we use "Filename" i.e "spaces in this file" and find the content in th file to find flag.  
password:"aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG"
## Level-4
The Content in the Present Working Directory is known by listings Command but few file are hidden as per there properties.   
To find all files in an Directory is to Move to the Directory and add  to the Main command listings.  
To Find Special properties of the main Command we find them Using "man <Command>" which stands for manual.  
to Find hidden File in present Working Directory use "ls -a" find password inside the file.  
password:"2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe"  

## Level-5
As per The Question we have to find human readable file inthe following Directory .  
To Find human Readable file i.e ASCII file we have to check the file format Generally we use FILE command to get format of a file as "file <filename>".  
as there were to many file we recursively use "file /path/*" to get all file format of the file present in the directory.  
we get a file format "/home/bandit4/inhere/-file07: ASCII text" and thats the human readable file.  
password: "lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR"  

## Level-6
As per the question we have to find a human readable file with size 1033 and not excutable.  
To find a file of required Size we can use the "Find command" with feauture -size 1033c here 1033 is Size and c determine the bytes.   
the only file wuth Size 1033 bytes is "./maybehere07/.file2".  
password:"P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU"  

## Level-7
This is just the extension level of the previous one.  
Here we have to find the Defined user Defined group Defined Size.  
we can Find how to find user,group from manual that is using man command of file.  
Using Command `find -user bandit7 -group bandit6 -size 33c`.  
password:"z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S"  
## Level-8
The flag stored in the file data.txt next to the word millionth.  
we have to Find the word from the list of data Generally Find comand is use to find files based on size and it features whereas it cant file words.  
to find words we can use "grep" Command to Search word .  
Using command `cat data.txt | grep millionth`.  

password:"TESKZC0XvTetK0S9xNwm25STk5iWrBvP"
## Level-9
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.  
Tha data consist of unknown number of word which may or may not be repeated to gather up all the similar file we can use "Sort" and "Uniq -c".   
Sort will sort the words as per alphabetical order and uniq -c determinatine the count of each each word repeated.  
Using Command `cat data.txt | sort | Uniq -c`.  
the password which repated once .  
password: "EN632PlfYiZbn3PhVK3XOGSlNInNE00t".  
## Level-10
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.  
Since the file type is data it contains machine langauges to find strings in the file we can use "string command" to find strings present in the data.  
and we have to search for == near flag.  
password:"G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s"  

## Level-11
The password for the next level is stored in the file data.txt, which contains base64 encoded data.  
To decode the encrypted base64 data we need to use echo i.e printing text of echo to decrypt encrypted data we need to use base64 command.  
Using The comand `echo "encrypted.data" | base64 -d`.  
password:"6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM"  

## Level-12
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.  
Shift cipher with shift space 13 alphabet called ROT13.  
Using The Command `tr 'A-Za-z' 'N-ZA-Mn-za-m' <<< "Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi"` The cipher text is decrypted  
password : "JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv"  

## Level-13
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed.  
For this level we have to create directory in tmp directory Using command `mkdir /tmp/Security`.  
Copy the file from /home/bandit12 to the present working directory Using `cp /home/bandit12/data.txt cypher`.  
This file hexdump is repeatedly compressed to get hexdump of file Use `xxd -r cypher > Encrypted`.  
Search the file type of the Encrypted file Using `file Encrypted`.  
Change the filename using mv command for leaving extension gz .  
TO Extract the gzip file Use the Command `gzip -d Encrypted.gz`.  
Check the file type of the Extracted File and Change the file extension into bz2.  
To Extract the bzip2 file Use the Command `bzip -d Encrypted.bz2`.  
Check the FIle type and Change the filename using mv command for leaving extension gz.  
To Extract the gzip file Use the Command `gzip -d Encrypted.gz`.  
Check the FIle type and Change the filename using mv command for leaving extension tar.  
To Extract the tar file Use command `tar --extract -f Encrypted.tar`.  
Check the FIle type and Change the filename using mv command for leaving extension tar.  
To Extract the tar file Use command `tar --extract -f data5.tar`.  
Check the FIle type and Change the filename using mv command for leaving extension bz2.  
To Extract the tar file Use command `bzip2 -d data6.bz2`.  
Repeat the process until the file type `ASCII` is shown .  
password "wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw"  

## Level-14
The password of the current level is stored in the next level and they have provided and ssh private key to login through ssh with host as local host.  
Using Command `ssh bandit14@localhost -i sshkey.private -p 2220`.  
password : "fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq"  

## Level-15
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.  
To have a networt connection between clinet and the server we can use netcat.  
Using Command ` echo "fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq" | nc localhost 30000`.  
password : "jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt"  

## Level-16
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption  
To Connec to the localhost at port 30001 using SSL encryption  
Use Command `openssl s_client -connect localhost:30001`   
Enter the previous level password and get current level password  
password:"JQttfApK4SeyHwDlI9SXGR50qclOAil1"

## Level-17
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000  
To Scan the port in the range we Use Command `nmap localhost -p 31000-32000`  
The list is the following port that listing to the host   
Use the Command `openssl s_client -connect localhost:port` and trt submiting curent level passowrd when you get the correct ssl speaking port that returns
the sshkey private of level17   
We can find level18 password by following the same as Level14  

## Level-18
The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new  
To check two files Line by Line  
Use the Command `diff passwords.new passwords.old`  
if you see bye-bye while login in to next level then thats something related to next level  

## Level-19

ssh is the command for the Secure Shell protocol, which allows you to securely connect to a remote server.  
To forces a pseudo-terminal allocation you want to run an interactive command on the remote server, such as a shell.
to forcely acces apseudo-terminal Use the Command `ssh -t bandit18@bandit.labs.overthewire.org -p 2220 /bin/sh`  
'/bin/sh' This is the command to execute on the remote server once connected. /bin/sh is a standard Unix shell.  
When the shecure shell is connected we can read readme file  
password: "awhqfNnAbc1naukrpqDYcF95h7HoMTrC"

## Level-20
Here we can use ls -la to list file permisions and who can write/read/excute the file.  
We see that bandit19 can execute the bandit20-do file.  
when we Execute bandit20-do it tells us to runs another command as another user.  
Generally passwords of the level is stored at /etc/bandit_pass/bandit20 if we have a permison to read/write we can check them so i used ./bandit20-do cat /etc/bandit_pass/bandit20 to get the password.  
Password: VxCazJaVykI6W36BkBU0mJTCM8rR95XT  
## Level-21
The Currunt Directory contain Suconnect file whicah can be excuted when we try to excut the file by `./suconnect` it shows Usage: ./suconnect <portnumber>
This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.  
We have to Find the listen port working on the this user using `nmap localhost`.  
these ports are working listening port numbers which are working and not free
To connect to the tcp port and send the flag
we use `echo "VxCazJaVykI6W36BkBU0mJTCM8rR95XT" | nc -l -p 5555 & ./suconnect 5555` netcat is used to have a listing connection between a port and the device  
here we used 5555 port is not reccomeded to use 5555 we can use any tcp port other thwn which are working 
password:"NvEJF7oVjkddltPSrdKEFOllh9V1IBcq"  
## Level-22
We find that a cron job is running. if we check , we find.... `* * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null` this * represent the cron job working every min depening on the user.This states it is running cronjob_bandit.   
```
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```  
This gives us password  
This shows the following commands have been excuted and possword is been stored in the file mentioned   
`cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv`

password is `WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff`

## Level-23
Again we have to chec  the cron job of this level. Which gives us when we excut /usr/passwd/bandit22.sh
```
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
cat /etc/bandit_pass/$myname > /tmp/$mytarget
```
here the shell script shown above are the commands usedc to run and find the variables    
$(whoami) return the user but we nned the passwd of next level so we are working on next user bandit23   
Now we get the correct file by running the command `echo I am user bandit23 | md5sum | cut -d ' ' -f 1`  
This gives us `8ca319486bfbbc3663ea0fbe81326349`  
This is the location of stored flag in temp directory  
So we `cat /tmp/8ca319486bfbbc3663ea0fbe81326349  
Password is `QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G`  
## Level-24
This level is similar to previous two levels where awe have to involve in task of the cronjob and write a script.
Here we need to write a script in `/var/spool/bandit24/foo` this script gets executed as bandit 24 .This script execute once and erase it so make sure to copy the intruction  
since the cronjob is executing as bandit24 the next actuall has already stored password at /etc/bandit_pass/bandit24 so we nned to copy the passowrd and store at a place  
make sure to give permission to read write and excute to the user of the script  
The passowrds copying script is  
```
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/bandit23/password.txt
```
Once the script is excuted after a min automatically run  
`cat /tmp/bandit23/password.txt`  
Password is `VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar`
## Level-25

