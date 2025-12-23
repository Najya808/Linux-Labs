Lab 34: sed for Text Manipulation

What I Learned
In this lab, I learned how to use the sed (stream editor) command to perform basic text manipulation in Linux. I practiced replacing words in a file and removing lines that match a specific pattern. These skills are useful for automating text editing tasks, especially when working with configuration files and large text data.

Tasks I Performed

Created a Sample Text File
I created a sample text file using the following command:

echo -e "Hello World\nHello Universe\nGoodbye World" > example.txt


This file was used to practice text replacement and deletion using sed.

Replaced a Word Using sed
I used sed to replace the word "World" with "Earth" in the file:

sed 's/World/Earth/g' example.txt


I learned that:

s stands for substitution

g performs a global replacement on each line

To save the changes directly to the file, I used:

sed -i 's/World/Earth/g' example.txt


Removed Lines Matching a Pattern
I used sed to delete lines containing the word "Universe":

sed '/Universe/d' example.txt


This command removed all lines that matched the specified pattern.

To apply the deletion permanently, I used:

sed -i '/Universe/d' example.txt


Summary
This lab improved my ability to:

Use sed for basic text substitution

Remove lines that match specific patterns

Edit files directly from the command line

These are essential skills for efficient text processing and automation in Linux environments, particularly when managing configuration files or scripting repetitive tasks.
