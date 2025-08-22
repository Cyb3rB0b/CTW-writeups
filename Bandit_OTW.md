# BANDIT 00

### TASK:
The task of the game is to establish a connection to an host (*bandit.labs.overthewire.org*) using the SSH protocol, specifying the number of the port (*2220*) and the username (*bandit0*).

You also need to log in to the server by entering the password that corresponds to the username (*bandit0*).

You have to exclusively use the CLI.

### SOLUTION
- ```ssh bandit.labs.overthewire.org -p 2220 -l bandit0```
- Type the given password (*bandit0*).

### EXPLANATION
- ***SSH (Secure Shell Protocol)*** is a network protocol that creates an encrypted communication channel between two hosts. 

- ***OpenSSH*** is the most widely used program that implements the SSH protocol. It's the de facto standard for secure connections in a Linux/Unix environment, where it comes pre-installed on most distributions. In the past, Windows users had to rely on third-party software, but now Windows 10 and 11 also include OpenSSH by default, making secure connections simpler from any operating system.

- The ***`ssh` command*** is part of the OpenSSH suite and its function is to start the connection process from the client side. 

The parts that follow the command are the instructions you're giving it to connect:
- `bandit.labs.overthewire.org`: This is the address of the server you want to connect to.

 - `-p 2220`: This is an **option** (or "*flag*"). 
The `-p` stands for "**port**”. The standard port for SSH is 22, but in this case, the server is using port 2220. This command tells SSH to use that specific gate.

- `-l bandit0`: This is also an **option**. The `-l` stands for "**login**".
It's used to specify the username you want to log in with, in this case, *bandit0*. Alternatively, you could write ‘*ssh 
bandit0@bandit.labs.overthewire.org -p 2220*’.



# BANDIT 01

### TASK:
The task of the game is to find the password for the next level. It is saved in a file called readme in the main directory. 

### SOLUTION:
- `cd`
- `ls`
- `cat readme`
- *write down the password shown on the screen*

### EXPLANATION:

- the **`cd` command** (short for *change directory*) is used to move from one folder to another within the file system. Its main purpose is to let you navigate the directory structure to reach the file or folder you want to work on. 
Here's how it works, with a few examples:
	- `cd folder_name`: This moves you from your current location into the folder you specified. 
	- `cd ..`: This takes you back up one level to the "parent" folder. It's useful for moving back up the directory tree.
	- `cd` (by itself) or `cd ~`: This will take you back to the home directory, no matter where you are. 

Here, we used the command `cd` (by itself) to confirm we were in the home directory

- the **`ls` command** (short for *list*) is used to list the contents of a directory.

Here, we used the `ls` command to view the content of the home directory, in order to check if the “readme” file  was inside it.

- The **`cat`** (short for concatenate) is used to display the content of one or more files directly in the terminal. Although its name refers to the action of "joining" (concatenating) files, its most common and simple use is to show what's inside a single file.

Here, we used the command `cat` to show the content of the readme file, and doing so, we found the password within it.

