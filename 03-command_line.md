# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > | Command              | Description                                          |
> > | -------------------- | ---------------------------------------------------- |
> > | ls folder            | Show current working directory path                  |
> > | mkdir                | Creating a directory                                 |
> > | rmdir                | Deleting a directory                                 |
> > | touch                | Creating a file using 'touch' command                |
> > | rm                   | Deleting a file                                      |
> > | mv                   | Renaming the file                                    |
> > | ls -a                | Listing hidden files                                 |
> > | mv                   | Copying a file from one directory to another         |
> > | uniq                 | Removing any exact duplicates.                       |
> > | wildcard *           | Selects all of the files in the current directory    |
> > | alias                | Allows you to create keyboard shortcuts, or aliases  |
> > | sort                 | Sort, merge, or sequence check text files            |
> > | grep                 | Search text for a pattern                            |
> > | chown                | Change the file ownership                            |
> > | awk                 | Pattern scanning and processing language              |
---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > | Command | Description                                                  |
> > | ------- | ------------------------------------------------------------ |
> > | ls      | Lists all files in the current directory.                    |
> > | ls -a   | Lists all contents in the working directory, including hidden files and directories. |
> > | ls -l   | Lists all contents of a directory in long format.            |
> > | ls -lh  | Lists all contents of a directory in long format and prints sizes in human readable format. |
> > | ls -lah | Lists all contents of a directory in long format, prints sizes in human readable format and includes hidden files and directories. |
> > | ls -t   | Orders files and directories by the time they were last modified. |
> > | ls -Glp | Lists all contents but does not print group names, long format and appends "/" indicator to directories. |

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > | Command | Description                                                  |
> > | ------- | ------------------------------------------------------------ |
> > | ls -q   | Displays non-printable characters as ?                       |
> > | ls -C   | Puts output into columns, sorted vertically; this is the default output format to the terminal. |
> > | ls -m   | Displays names in single line, with commas separating names. |
> > | ls -lS  | Displays all content in long format, sorts files and directories by size, largest to smallest.                          |
> > | ls -i   | Prints index number of each file. |

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > It is a command used to build and execute commands from standard input. It reads streams of data from standard input, then generates and executes command lines; thus it can take output of a command and pass it as argument of another command.

> > Example: **ls | xargs -n 10 echo** This command will generate a list of files names and directories but specifies how many file names or directory names are processed by echo on each iteration, in this case it would be 10.

>> This is an example for github commit through terminal
