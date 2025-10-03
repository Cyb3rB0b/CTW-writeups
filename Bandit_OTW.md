# BANDIT 00

### TASK:
The task of the game is to establish a connection to an host (*bandit.labs.overthewire.org*) using the SSH protocol, specifying the number of the port (*2220*) and the username (*bandit0*).

You also need to log in to the server by entering the password that corresponds to the username (*bandit0*).

You have to exclusively use the CLI.

### SOLUTION
- `ssh bandit.labs.overthewire.org -p 2220 -l bandit0`
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



# BANDIT 00 to 01

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





#BANDIT 2 TO 3

###TASK: 
How to read the contents of a file whose name contains spaces.

###SOLUTION
1. Type: `cat '--spaces in the filename--'`

###EXPLANATION
If you try to read a file in the terminal whose name is `--spaces in the file name--` without using quotation marks, the terminal will interpret the dashes (-) and spaces as argument or option separators, not as part of the file name.
This would lead to an error because the terminal would not be able to find a command or file corresponding to the various pieces into which it divided your input.
To avoid these problems and tell the terminal that everything enclosed in quotation marks is a single file name, you must enclose the file name in single quotation marks (') (but you can also use the double quotation marks ").



#BANDIT 3 TO 4

###TASK: How to find a hidden file stored in a directory

###SOLUTION
1. Type: `cd inhere`
2. Type: `ls -a`
3. Type: `cat ...Hiding-From-You`

###EXPLANATION
The flag `-a` in the `ls`command let you to see the hidden file in a directory.
You use the cat command to read the content of the file.


#BANDIT 4 TO 5
###TASK
How to find a readable file that is located in a specific directory (`inhere`). Specification: The first letter of all the files stored in the inhere directory is `-`.

###SOLUTION 
1. Type: `file -- -*`
2. Type: `cat ./"-file07"`

###EXPLANATION
`file -- -*` 
`file` : This is the main command. It's a utility that examines a file's contents and metadata to determine its type. 
`--` :This is the end-of-options marker. This is the most crucial part of the command for this specific use case. It signals to **`file`** that all subsequent arguments are to be treated as filenames, not command-line options.
`-*`: This is a wildcard pattern that matches all filenames that start with a hyphen. The asterisk (`*`) acts as a wildcard, matching any sequence of characters.

Once you type this command it returns a list of files which shows the files' type. You can see that only the `-file07` is a plain text file.
The command's output, ASCII text, means the file contains standard characters that are human-readable and can be opened with any basic text editor. It indicates the file is not a binary file, an image, or an executable program.

'cat ./"-file07"`
The command `cat ./"-file07"`  is used to read the contents of a file named -file07 located in the current directory.

Here's a breakdown of each part of the command:
` cat` : This is the primary command. `cat` (short for "concatenate") is a standard Linux utility that reads files and prints their content to the screen.

` ./` : This is a relative path. The period (`.`) represents the "current directory." Adding the forward slash (/) tells the shell to look for a file inside the folder you're currently in.

` "-file07"` : This is the filename. The quotation marks are crucial here. The initial hyphen (` -`) is a special character that most commands interpret as the start of an option. By enclosing the filename in quotation marks, you force the shell to treat it as a literal filename, including any spaces or special characters it may contain.



#BANDIT 5 TO 6

###TASK: Find a file that is stored somewhere under the inhere directory and that must have three main, identified characteristics.

###SOLUTION: 
1. Type: `cd inhere`
2. Type: `find . -type f - size 1033c`
3. Type: `file ./maybehere07/.file2`
4. Type: `cat ./inhere/maybehere07/.file2`

***`cd inhere`***
The `cd` command used in a Linux or Unix-like environment to change your current directory. It stands for "change directory."
You must specify the name of the directory you want to move into. 
When you run this command, your current working location in the terminal changes from your starting directory to the inhere directory

***`find . -type f - size 1033c`***
This command find is used to search for files that meet specific criteria within a given directory (In this case, we're specifying two out of the three criteria provided).

Breaking down each part of the command:

- `find`: This is the primary command. Its purpose is to search for files and directories within a specified location.
`.`: This is the path where the search begins. The period (.) is a shorthand for the current directory, meaning the command will search the directory you're currently in and all of its subdirectories.
- `-type f`: This is a search criterion. It filters the results to only include files. The `f` stands for "file." If you were to use `d` instead (`-type d`), the command would only look for directories.
- `-size 1033c`: This is another criterion that specifies the exact size of the files to be found. The number `1033` represents the size, and the `c` is a suffix that specifies the unit of measurement, which in this case is bytes.

After typing this code, the following string is returned to us: `./inhere/maybehere07/.file`

***`file ./maybehere07/.file2`***
- `file` This command examines a file's content and metadata to determine its type. 
In this case we want to check the file that was returned to us in the output from the previous command. The file is stored in the directory `./inhere/maybehere07/`.

After running the command, the system will tell us that the file is an ASCII text file, which means it's human-readable.


***`cat ./inhere/maybehere07/.file2`***
With this command, we can read the content of the file that meets all three of the requirements we were given.



#BANDIT 6 TO 7

###TASK: Find a file that is stored somewhere under the inhere directory and that must have three main, identified characteristics. In this case the characteristics are: 
1. owned by user bandit7
2. owned by group bandit6
3. 33 bytes in size

###SOLUTION: 
1. Type: `find / -user tizio7 -group tizio6 -size 33c 2>/dev/null`
2. Type: `cat /var/lib/dpkg/info/bandit7.password`

###EXPLANATION:
***`find / -user tizio7 -group tizio6 -size 33c 2>/dev/null`***
`find /`: The find command starts its search from the root directory (/). This ensures that every single folder and subfolder on the server is scanned.

`-user bandit7`: This filters files to be owned by the user bandit7.

`-group bandit6`: This further filters the results for files owned by the group bandit6.

`-size 33c`: This finds only the files that have an exact size of 33 bytes.

`2>/dev/null`: This part doesn't help find the file, but it manages errors. When you search the entire server, you will likely get many "Permission denied" messages for folders you can't access. This redirects the error output (identified by the number 2) to the system's "black hole" (/dev/null), making the output clean and easy to read.

After running the command, the system will tell us the name of the file which meets all of the giver requirements.

***`cat /var/lib/dpkg/info/bandit7.password`***
With this command, we can read the content of the file that meets all three of the requirements we were given.


#BANDIT 7 TO 8

###TASK: How to search for and view a line that contain a specified pattern within specific text files

###SOLUTION
1. Type: `ls`
2. Type: `grep "millionth" data.txt`


###EXPLANATION
1. Type: `ls`
This command is not necessary to find the solution of this game but it helps to be sure that the file named data.txt is actually in our working directory.

2. Type: `grep "millionth" data.txt`
`grep`  is the main command. It stands for "globally search for a regular expression and print". Its purpose is to search for text patterns.

`"millionth"`: This is the text string (or pattern) you are looking for. Double quotation marks 'are important because they ensure that the terminal interprets `"millionth"` as a single string, even if it contained spaces or special characters. In this case, look for the word "millionth" exactly.

`data.txt`: This is the filename where grep will search for the string. The command will examine each line of the data.txt file to see if it contains “millionth”.