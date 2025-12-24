Lab 46: Bash Profile vs. Bashrc
What I Learned

In this lab, I learned the difference between .bash_profile and .bashrc files and how they affect the shell environment in Linux. I explored when each file is executed and practiced customizing the shell by adding aliases and environment variables. This lab helped me understand how to personalize and optimize the command-line experience for daily use.

🔹 Introduction

Bash uses different configuration files depending on how the shell is started. The .bash_profile file is executed for login shells, while .bashrc is executed for interactive non-login shells. Understanding the distinction is important for applying configurations correctly and avoiding unexpected behavior.

🧪 Lab Tasks Performed
🔹 Task 1: Examine .bash_profile and .bashrc
✅ Locate the Files

I navigated to my home directory and listed all files, including hidden ones:

cd ~
ls -a


This allowed me to confirm the presence of .bash_profile and .bashrc.

✅ Review .bash_profile

I opened the file using nano:

nano ~/.bash_profile


Explanation:

.bash_profile is executed when a user logs in.

It often contains environment variables and startup configurations.

✅ Review .bashrc

I opened the .bashrc file:

nano ~/.bashrc


Explanation:

.bashrc runs every time a new terminal session is opened.

It is commonly used for aliases, functions, and shell behavior settings.

🔹 Task 2: Customize .bashrc
✅ Backup Configuration Files

Before making changes, I created backups:

cp ~/.bashrc ~/.bashrc.backup
cp ~/.bash_profile ~/.bash_profile.backup


This ensures the original files can be restored if needed.

✅ Add Custom Aliases

I added the following alias at the end of .bashrc:

alias ll='ls -la'


I also explored additional aliases such as:

alias gs='git status'
alias lt='ls --tree'


Aliases help shorten frequently used commands and improve efficiency.

✅ Add an Environment Variable

Below the aliases, I added:

export MY_VAR="Hello World!"


Explanation:

Environment variables store values that can be used by programs and scripts.

Exporting the variable makes it available to child processes.

✅ Reload .bashrc

To apply the changes immediately, I reloaded the file:

source ~/.bashrc

✅ Verify the Changes

I verified the alias:

ll


And checked the environment variable:

echo $MY_VAR


Both worked as expected.

Summary

In this lab, I learned how to:

Identify and understand .bash_profile and .bashrc

Differentiate between login and non-login shells

Customize the shell using aliases and environment variables

Apply changes without restarting the terminal

This knowledge is essential for improving productivity and maintaining consistent shell behavior across Linux environments.
