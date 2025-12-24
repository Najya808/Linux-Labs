Lab 47: Using the history Command
What I Learned

In this lab, I learned how to use the history command to view previously executed commands in the shell. I practiced re-running commands using their history numbers and learned how to clear the command history when needed. This lab showed how command history can improve efficiency and save time when working in a Linux terminal.

🔹 Introduction

The history command in Linux stores a list of commands that have been executed in the shell. This feature is useful for reviewing past commands, repeating tasks quickly, and troubleshooting previous actions without retyping long commands.

🧪 Lab Tasks Performed
🔹 Task 1: View Command History

To display previously executed commands, I ran:

history


Explanation:

This command shows a numbered list of commands executed in the shell.

The numbers assigned to each command can be used to re-run them easily.

🔹 Task 2: Re-run a Command Using History Number

After viewing the history, I identified a command I wanted to execute again.

For example, if command number 25 was:

ls -la


I re-ran it using:

!25


Explanation:

The ! symbol followed by a number executes the command stored at that history position.

This is useful for quickly repeating commands without retyping them.

🔹 Task 3: Clear the Command History

To clear the command history of the current shell session, I ran:

history -c


To verify that the history was cleared:

history


Explanation:

Clearing history can be useful for privacy or resetting the command log.

This removes stored commands from the current session’s history.

Summary

In this lab, I learned how to:

View previously executed commands using history

Re-run commands using history numbers

Clear the command history when required

These skills improve efficiency when working in the terminal and help streamline daily Linux administration tasks.
