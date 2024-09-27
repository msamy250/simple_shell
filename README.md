0x16. C - Simple Shell
By Spencer Cheng, in collaboration with Julien Barbier
This project is designed for teams of two (your team: Godswill Kalu, Vatalis Ibeh).

Learning Objectives
By the end of this project, you should be able to explain the following without needing external resources:

General Knowledge
The original designers and implementers of the Unix operating system
The creator of the first version of the UNIX shell
The inventor of the B programming language, which preceded C
Who Ken Thompson is
How a shell functions
The definitions of pid and ppid
How to manipulate the environment of the current process
The difference between functions and system calls
How to create processes
The three main function prototypes in C
How the shell uses the PATH to locate programs
How to use the execve system call to execute a program
How to pause a process until one of its child processes terminates
What EOF (End-of-File) means
Requirements
General Guidelines
Use editors like vi, vim, or emacs.
All code must compile on Ubuntu 20.04 LTS with gcc using the flags -Wall -Werror -Wextra -pedantic -std=gnu89.
Files should always end with a newline.
A README.md file is required at the root of the project directory.
Follow the Betty style guide for coding, checked with betty-style.pl and betty-doc.pl.
Ensure your shell is free from memory leaks.
Limit each file to no more than 5 functions.
Include guards must be used for all header files.
Only use system calls when necessary (why?).
GitHub Repository
There should be a single repository for the project per group. If both members have a repository with the same name on their accounts, it risks a 0% score. Be sure to add your teammate as a collaborator.

Additional Information
Output Requirements
Unless otherwise stated, your program's output must match that of the sh shell (/bin/sh), including error messages. The only exception is that your program should display the error using the name in argv[0].

Example error output in sh:

sh
Copy code
$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
Similar error in your shell (hsh):

sh
Copy code
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
Allowed Functions and System Calls
access()
chdir()
close()
closedir()
execve()
exit()
_exit()
fflush()
fork()
free()
getcwd()
getline()
getpid()
isatty()
kill()
malloc()
open()
opendir()
perror()
read()
readdir()
signal()
stat(), lstat(), fstat()
strtok()
wait(), waitpid(), wait3(), wait4()
write()
Compilation
Your shell will be compiled using the following command:

sh
Copy code
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
Project Files
README.md: Contains a description of the project.
man_1_simple_shell: The man page for the shell you're building.
AUTHORS: A file listing all contributors to the repository.
main.h: Header file that includes standard libraries and function prototypes used in the program.
main.c: Initializes the program, running an infinite loop with the prompt function.
prompt.c: Uses getline to read user input and forks a new process to keep the shell running.
special_character.c: Handles special inputs like slashes, exit, or env.
string.c: Manages string operations like length, writing, searching directories, and concatenation.
cmd.c: Finds and processes the user's command input.
execute.c: Executes the user's commands.
This version maintains the meaning and structure while using different wording and expressions.
