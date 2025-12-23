Lab 35: awk for Data Processing

What I Learned
In this lab, I learned the basics of using the awk command for processing and analyzing structured text data in Linux. I practiced extracting specific columns from a file and filtering rows based on conditions. These skills are useful for working with logs, reports, and structured data files in Unix-like systems.

Tasks I Performed

Created a Sample Data File
I created a sample file named data.txt containing structured data:

Name Age Gender
John 28 Male
Emma 22 Female
Mike 32 Male
Lucy 29 Female


This file was used to practice column extraction and filtering using awk.

Printed Specific Columns from the File
I used awk to print the first and third columns (Name and Gender):

awk '{print $1, $3}' data.txt


I learned that:

$1 represents the first column

$3 represents the third column

awk processes each line of the file automatically

The output displayed only the selected columns.

Filtered Rows Based on a Condition
I filtered rows where the age was greater than 25 using:

awk '$2 > 25 {print $0}' data.txt


Here:

$2 refers to the Age column

$2 > 25 is the filtering condition

print $0 prints the entire matching line

This command displayed only the rows that met the condition.

Summary
This lab improved my ability to:

Use awk to extract specific columns from text files

Apply conditions to filter data

Process structured text efficiently from the command line

These skills are essential for data processing, log analysis, and automation tasks in Linux environments.
