Lab 51: Basic Regex with grep
What I Learned

In this lab, I learned how to use the grep command with basic Regular Expressions (Regex) to search for patterns in text files. I practiced finding lines that start or end with certain characters and handling optional characters in patterns.

🎯 Lab Objectives

Understand the basics of Regular Expressions (Regex)

Use grep to search text files for specific patterns

Find lines starting or ending with specific characters

Utilize optional character matching with Regex

🧪 Lab Tasks Performed

🔹 Task 1: Search for Lines Starting with a Pattern

Steps:

Created a sample text file:

echo -e "apple\nbanana\ncherry\napricot\ngrapefruit" > example.txt


Used grep with Regex to find lines starting with "a":

grep '^a' example.txt


Observation:
The command output:

apple
apricot


Key Concept:
The caret ^ in Regex matches the beginning of a line.

🔹 Task 2: Search for Lines Ending with a Pattern

Steps:

Used grep with Regex to find lines ending with "y":

grep 'y$' example.txt


Observation:
The command output:

cherry


Key Concept:
The dollar sign $ in Regex matches the end of a line.

🔹 Task 3: Filter Lines with Optional Characters

Steps:

Created a file colourExample.txt with content:

color
colour
colr


Used grep to match lines with an optional "u":

grep 'colou?r' colourExample.txt


Observation:
The command output:

color
colour


Key Concept:
The question mark ? in Regex denotes that the preceding character is optional.

Summary

In this lab, I learned how to:

Use grep with Regex patterns to filter text in files

Find lines starting with specific characters using ^

Find lines ending with specific characters using $

Handle optional characters in patterns using ?

This lab strengthened my understanding of Regex and how it integrates with grep for effective text processing and search automation.
