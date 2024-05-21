The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220

ssh banditX@bandit.labs.overthewire.org -p 2220 states to connect Secure Shell of User:Bandit Host:"bandit.labs.overthewire.org" -p stands for port X stands for the level
## Level-0
The Task is to log into the SSH of the given details with Username:bandit0 password:bandit0
## Level-1
The Password is Hidden in the directory to find content of present working directory we can use "ls" command set for listings

To Read the content from a text file or metadata of the exicutable file The "cat <filename>" command is used

To move from One Directory to Other we use "cd <filename>" stands for Change Directory

Password: "NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL"
## Level-2
The present Working Directory Contains the file "-" Since special character cant be accessed as filename

prefix "./" is used which stands for excute file it defines the special character of file as datatype file

password:"rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi"

## Level-3
Spaces in the file name seems to be work as different Directories to make it as Single Directory we use "Filename" i.e "spaces in this file" and find the content in th file to find flag

password:"aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG"

## Level-4
The Content in the Present Working Directory is know by listings Command but few file are hidden as per there properties 

To find all files in an Directory is to Move to the Directory and add  to the Main command listings

To Find Special properties of the main Command we find them Using man <Command> which stands for manual

to Find hidden File in present Working Directory 


