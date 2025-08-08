# BANDIT 00

### TASK: 
The task of the game is to establish a connection to the host *bandit.labs.overthewire.org* using the SSH protocol on the port number 2220 and the username bandit0. 
You have to use exclusively the CLI

### COMMAND USED:
- `ssh` 
#### COMMAND’S OPTIONS:
- `-p` [to specify the number of the port] 
- `-l` [to specify the username]

### SOLUTION:
- **STEP 1**: Establish a connection
Type: *ssh bandit.labs.overthewire.org -p 2220 -l bandit0*
- **STEP 2**: Write down the password in the text

### LESSON LEARNED:
I learn how to connect to a specific host using an ssh protocol specifying the number of the port and the username.

___
# BANDIT 01 

### TASK: 
The tasks of the game are the follow:

1.	Enstablish a connection to the host *bandit.labs.overthewire.org using* the SSH protocol on the port number 2220 and the username *bandit1*;

2.	Use the password founded in the previous level;

3.	Open the file called “readme” located in the home directory.

### COMMANDS USED:
- ` ssh ` 
- ` ls `
- ` cat `

#### COMMAND’S OPTIONS:
- `-p` [to specify the number of the port] 

- `-l` [to specify the username]

### SOLUTION:

**STEP 1**: Establish a connection to the specified host
- Type: `ssh bandit.labs.overthewire.org -p 2220 -l bandit1`

**STEP 2**: Type the password founded in the previous level

**STEP 3**: List all the file located in the directory
- Type: `ls`

**STEP 4**: Show the content of the file *readme*
- Type: `cat readme`

**STEP 5**: Write down the password showed on the screen

### LESSON LEARNED:
I learn how to view the content of a directory and how to read the content of a file

