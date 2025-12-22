📄 Lab 32 File Content

Create a file named:

lab-32-introduction-to-vi-vim.md


Paste this as-is:

Lab 32: Introduction to vi/vim

What I Learned
In this lab, I learned the basics of using the vi/vim text editor in a Linux environment. I understood how to open and create files, switch between different modes, navigate within a file, and perform simple editing operations like searching and replacing text. These skills are important for editing configuration files and code directly from the terminal.

Tasks I Performed

Opened and Created a File Using vi
I started by creating a new file using:

touch file.txt


I then opened the file in the vi editor using:

vi file.txt


This helped me understand how vi opens existing files and creates new ones if they do not already exist.

Entered Insert Mode and Added Text
After opening the file, I pressed:

i


to enter Insert mode and typed a few lines of text. I learned that vi has different modes and text can only be added in Insert mode.

Saved Changes and Exited the Editor
To save my changes, I exited Insert mode by pressing:

Esc


and then used:

:w


to save the file. To exit the editor, I used:

:q


This helped me understand how to safely save and quit vi.

Practiced Navigation Within the File
I practiced moving around the file using the following keys:

h to move left

j to move down

k to move up

l to move right

This improved my comfort with keyboard-based navigation inside vi.

Searched and Replaced Text
I searched for text in the file using:

/example


I also practiced replacing text using:

:%s/old/new/g


This showed me how vi can quickly modify text across an entire file.

Summary
This lab improved my ability to:

Use vi to open and edit files from the terminal

Understand and switch between Insert and Normal modes

Navigate efficiently within files

Perform search and replace operations

These are essential skills for working with Linux systems, especially when managing configuration files or editing code on servers.
