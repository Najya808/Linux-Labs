Lab 33: Basic Grep Usage

What I Learned
In this lab, I learned how to use the grep command in Linux to search for specific text patterns within files and directories. I practiced basic string searching, recursive searches across directories, and displaying context lines around matching results. These skills are important for log analysis, troubleshooting, and searching configuration files in Linux systems.

Tasks I Performed

Searched for a String in a Single File
I used the grep command to search for a specific word inside a text file:

grep "search_term" filename.txt


I also practiced with a real example by searching for the word "error" in a file:

grep "error" example.txt


This helped me understand how grep displays lines that contain the matching text.

Searched Recursively in Directories
I used the recursive option -r to search for a string across all files inside a directory and its subdirectories:

grep -r "search_term" /path/to/directory/


For example, I searched for the word "password" inside system files:

grep -r "password" /etc/


This showed me how grep can be used to scan multiple files efficiently.

Used Context Lines with -A and -B Options
I practiced displaying lines before and after a match to get better context:

grep -A 2 -B 2 "search_term" filename.txt


I also used this command to search for the word "timeout" while showing surrounding lines:

grep -A 2 -B 2 "timeout" config.txt


This helped me understand how context options make grep output more informative.

Practical grep Example
I created a sample file named sample.txt containing multiple lines, including error messages. I then ran:

grep "error" sample.txt


This highlighted all lines containing the word "error" and reinforced my understanding of basic grep usage.

Summary
This lab improved my ability to:

Use grep to search for text within files

Perform recursive searches across directories

Display contextual lines around search results

These are essential skills for analyzing logs, troubleshooting issues, and efficiently working with text files in Linux environments.
