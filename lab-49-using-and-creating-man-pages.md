Lab 49: Using and Creating Man Pages
What I Learned

In this lab, I learned how to use existing man pages to understand Linux commands and how to create a custom man page for a simple shell script. I also learned how man pages are structured, compressed, installed, and accessed using the man command.

🎯 Lab Objectives

Understand how to navigate and read existing man pages

Learn the structure of a man page

Create a custom man page for a shell script

Install and view a custom man page

🧪 Lab Tasks Performed
🔹 Task 1: Using Existing Man Pages
Access the Manual Page for ls
man ls


Observation:

The man page opens with several structured sections such as:

NAME

SYNOPSIS

DESCRIPTION

OPTIONS

These sections explain what the command does and how to use it.

Navigation

Arrow keys → Scroll

q → Exit the man page

Key Concept:
The man command provides built-in documentation for Linux commands and utilities, making it a critical tool for system administration and troubleshooting.

🔹 Task 2: Creating a Simple Man Page
Step 1: Create a Simple Script
nano test_script.sh


Add the following content:

#!/bin/bash
echo "This is a test script."


Save and exit.

Step 2: Create the Man Page File
nano test_script.1


Add the following content:

.TH TEST_SCRIPT 1 "October 2023" "Version 1.0" "Custom Manual"
.SH NAME
test_script \- A simple test script demonstration.
.SH SYNOPSIS
test_script
.SH DESCRIPTION
This script outputs a simple message: "This is a test script."
.SH AUTHOR
Najya Qurayshi


Save and exit.

Key Concepts:

.TH → Defines the title and header of the man page

.SH → Defines section headings

\- → Escaped hyphen so it prints correctly

🔹 Task 3: Installing and Viewing the Custom Man Page
Compress the Man Page
gzip test_script.1

Move the Man Page to the System Directory
sudo mv test_script.1.gz /usr/local/share/man/man1/

View the Custom Man Page
man test_script


Observation:

The custom man page opens successfully.

The layout follows standard man page formatting.

Key Concept:
Man pages are stored in compressed format (.gz) inside directories like man1, man5, etc., based on their section number.

Summary

In this lab, I learned how to:

Use existing man pages to understand Linux commands

Navigate and interpret man page sections

Create a custom man page using groff formatting

Compress, install, and view a custom man page

This lab strengthened my understanding of Linux documentation standards and showed how professional command-line tools are documented.
