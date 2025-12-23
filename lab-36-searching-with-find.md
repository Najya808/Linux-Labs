Lab 36: Searching with find

What I Learned
In this lab, I learned how to use the find command in Linux to search for files based on specific criteria such as file name and file size. I also practiced using the -exec option to run commands on the files found. These skills are important for efficient file management and automation in Linux systems.

Tasks I Performed

Found All .txt Files in the Home Directory
I used the find command to search for all .txt files in my home directory:

find ~ -name "*.txt"


I learned that:

~ represents the home directory

-name filters files based on their names

This command listed all text files within the home directory and its subdirectories.

Found Files Larger Than 1MB
I searched for files larger than 1MB using:

find ~ -size +1M


I learned that the -size option allows filtering files based on their size, which is useful for identifying large files that may need cleanup.

Executed a Command on Found Files Using -exec
I used the -exec option to count the number of lines in each .txt file:

find ~ -name "*.txt" -exec wc -l {} \;


This helped me understand how to run additional commands on each file found using find.

Summary
This lab improved my ability to:

Search for files using name and size filters

Navigate directory structures efficiently

Execute commands on multiple files using the -exec option

These skills are essential for managing files and automating tasks across Linux systems.
