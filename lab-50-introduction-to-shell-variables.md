Lab 50: Introduction to Shell Variables
What I Learned

In this lab, I learned the difference between local and global shell variables, how to create and access them, and how special variables like $?, $$, and $# work. I also practiced using variables in the shell and understood their scope and behavior in scripts and subprocesses.

🎯 Lab Objectives

Understand the concept of shell variables

Learn how to set and use local and global variables

Learn how to utilize special shell variables such as $?, $$, and $#

🧪 Lab Tasks Performed

🔹 Task 1: Working with Local Variables
Step 1: Create a Local Variable

MYVAR="HelloWorld"


Step 2: Access the Local Variable

echo $MYVAR


Observation: The value HelloWorld is displayed.
Key Concept: Local variables exist only in the current shell session.

🔹 Task 2: Working with Global Variables
Step 1: Create a Global Variable

export MYVAR2="GlobalHello"


Step 2: Access the Global Variable in a Subshell

bash -c 'echo $MYVAR2'


Observation: The value GlobalHello is printed in the new shell session.
Key Concept: Exported variables are available to all child processes.

🔹 Task 3: Understanding Special Variables

$? → Exit status of the last command

echo $?


$$ → Process ID (PID) of the current shell

echo $$


$# → Number of arguments passed to a script or function

bash -c 'echo $#'


Observation: Each variable provides useful information for scripting and shell management.

Summary

In this lab, I learned how to:

Create and use local and global variables in the shell

Use special variables to check command status, process IDs, and argument counts

Understand variable scope and behavior in scripts and subshells

This lab helped me build a foundation for scripting and automating tasks in Linux.
