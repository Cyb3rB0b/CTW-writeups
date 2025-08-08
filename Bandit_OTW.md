{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fnil\fcharset0 Menlo-Regular;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue255;\red255\green255\blue254;\red0\green0\blue0;
}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c100000;\cssrgb\c100000\c100000\c99608;\cssrgb\c0\c0\c0;
}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\partightenfactor0

\f0\fs28 \cf2 \cb3 \expnd0\expndtw0\kerning0
# BANDIT 00\
\
\cf4 ### TASK: \
The task of the game is to establish a connection to the host *bandit.labs.overthewire.org* using the SSH protocol on the port number 2220 and the username bandit0. \
You have to use exclusively the CLI\
\
### COMMAND USED:\
- `ssh` \
#### COMMAND\'92S OPTIONS:\
- `-p` [to specify the number of the port] \
- `-l` [to specify the username]\
\
### SOLUTION:\
- **STEP 1**: Establish a connection\
Type: *ssh bandit.labs.overthewire.org -p 2220 -l bandit0*\
- **STEP 2**: Write down the password in the text\
\
### LESSON LEARNED:\
I learn how to connect to a specific host using an ssh protocol specifying the number of the port and the username.\
\cf2 \
___\
# BANDIT 01 \
\
\cf4 ### TASK: \
The tasks of the game are the follow:\
\
1.	Enstablish a connection to the host *bandit.labs.overthewire.org using* the SSH protocol on the port number 2220 and the username *bandit1*;\
\
2.	Use the password founded in the previous level;\
\
3.	Open the file called \'93readme\'94 located in the home directory.\
\
### COMMANDS USED:\
- ` ssh ` \
- ` ls `\
- ` cat `\
\
#### COMMAND\'92S OPTIONS:\
- `-p` [to specify the number of the port] \
\
- `-l` [to specify the username]\
\
### SOLUTION:\
\
**STEP 1**: Establish a connection to the specified host\
- Type: `ssh bandit.labs.overthewire.org -p 2220 -l bandit1`\
\
**STEP 2**: Type the password founded in the previous level\
\
**STEP 3**: List all the file located in the directory\
- Type: `ls`\
\
**STEP 4**: Show the content of the file *readme*\
- Type: `cat readme`\
\
**STEP 5**: Write down the password showed on the screen\
\
### LESSON LEARNED:\
I learn how to view the content of a directory and how to read the content of a file\
\cf2 \
}