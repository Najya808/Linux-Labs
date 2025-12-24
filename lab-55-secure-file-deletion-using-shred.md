Lab 55: Secure File Deletion Using shred
What I Learned

In this lab, I learned how to securely delete files using the shred command in Linux. I practiced creating a test file, using shred to overwrite and remove it, and verifying that the file cannot be recovered. This reinforced the importance of secure file deletion, especially when handling sensitive information.

Lab Objectives

Understand the necessity of secure file deletion

Learn how to use the shred command to delete files securely

Verify that shredded files are unrecoverable

 Lab Tasks Performed

 Task 1: Creating a Test File

Step 1.1: Create a Sample File

echo "This is a sensitive file that needs secure deletion." > sample.txt


Step 1.2: Verify the File's Contents

cat sample.txt


Observation:
The file displays the text correctly.

Key Concept:
Creating a test file ensures that you have a file to practice secure deletion on without risking important data.

🔹 Task 2: Using shred for Secure Deletion

Step 2.1: Shred the File

shred -u sample.txt


Explanation:

-u option overwrites the file and removes it after shredding.

By default, shred overwrites the file 3 times. Use -n to increase overwrites for more security:

shred -n 5 -u sample.txt


Step 2.2: Considerations

shred is most effective on HDDs.

On SSDs or journaled filesystems, complete file removal is not guaranteed due to data storage mechanics.

Key Concept:
shred overwrites file contents to prevent recovery, making it more secure than normal deletion.

🔹 Task 3: Verification of Unrecoverability

Step 3.1: Check if File Exists

ls -l sample.txt


Observation:
Error indicates the file does not exist.

Step 3.2: Attempt Recovery

grep "sensitive" sample.txt


Observation:
Nothing is found, confirming the file has been effectively shredded.

Key Concept:
Verifying deletion ensures the file cannot be recovered, which is critical for data confidentiality.

Summary

In this lab, I learned how to:

Create and verify a test file for practice

Use shred to securely delete a file by overwriting it multiple times

Confirm that shredded files are unrecoverable

Understand limitations on SSDs and journaled filesystems
