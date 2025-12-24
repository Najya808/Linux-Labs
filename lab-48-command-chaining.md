Lab 48: Command Chaining
What I Learned

In this lab, I learned how command chaining works in Unix/Linux systems. I practiced using different chaining operators (&&, ||, and ;) to control command execution based on success or failure. This lab helped me understand how multiple commands can be executed efficiently on a single line and how command flow can be controlled.

🔹 Introduction

Command chaining allows multiple shell commands to be executed in a single line. Depending on the operator used, commands can run conditionally (based on success or failure) or sequentially regardless of outcome. This technique is commonly used in scripting and automation.

🎯 Lab Objectives

Understand the concept of command chaining

Learn to use &&, ||, and ;

Analyze how command execution changes based on success or failure

Practice real-world command chaining scenarios

🧪 Lab Tasks Performed
🔹 Task 1: Using the && Operator

The && operator executes the second command only if the first command succeeds.

Step 1: Run two successful commands
mkdir new_directory && cd new_directory


Observation:

The directory is created successfully.

Since mkdir succeeds, the cd command executes.

Step 2: Run a successful command followed by a failing command
echo "Hello, World" && cd non_existent_directory


Observation:

The echo command runs successfully.

The cd command fails because the directory does not exist.

No further commands are executed after failure.

🔹 Task 2: Using the || Operator

The || operator executes the second command only if the first command fails.

Step 1: Run a failing command followed by a fallback command
cd non_existent_directory || echo "Directory does not exist"


Observation:

The cd command fails.

The echo command executes and displays the error message.

🔹 Task 3: Using the ; Operator

The ; operator runs commands sequentially, regardless of success or failure.

Step 1: Run multiple commands using ;
echo "This will always print"; cd non_existent_directory; echo "This prints anyway"


Observation:

All commands execute one after another.

The failure of cd does not affect the execution of other commands.

📌 Case Study Example
Scenario:

Automating a simple backup process where:

A backup directory is created

If it already exists, an error message is logged

Files are copied only if directory creation succeeds

Command Chain:
mkdir backup || echo "Backup directory already exists" && cp important_file.txt backup/


Explanation:

Attempts to create the backup directory

Prints a message if directory creation fails

Copies the file only if the directory creation was successful

Summary

In this lab, I learned how to:

Use && to execute commands conditionally on success

Use || to execute commands when a failure occurs

Use ; to execute commands sequentially without conditions

Apply command chaining to real-world automation scenarios

Command chaining is an essential skill for shell scripting, automation, and efficient system administration.
