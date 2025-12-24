Lab 54: Using df and du
What I Learned

In this lab, I learned how to monitor disk usage and manage storage effectively using the df and du commands. I practiced checking overall disk space, analyzing directory usage, and identifying large files or folders to optimize storage.

 Lab Objectives

Understand and use the df command to check disk space usage

Utilize the du command to assess directory usage

Analyze disk and directory usage to manage system storage efficiently

 Lab Tasks Performed

Task 1: Checking Disk Space with df

Step 1.1: Open Terminal

Launch the terminal on your Linux system.

Step 1.2: Use df to Check Disk Space

df -h


Explanation:

df displays available disk space on mounted filesystems.

-h flag shows output in human-readable format (GB, MB, etc.).

Step 1.3: Analyze Output

Review columns: Filesystem, Size, Used, Avail, Use%, Mounted on.

Example: If /dev/sda1 shows high usage, it may require cleanup or expansion.

Key Concept:
The df command provides a high-level overview of disk usage across all mounted filesystems.

🔹 Task 2: Checking Directory Usage with du

Step 2.1: Identify a Directory to Analyze

Example: /home/user/Documents

Step 2.2: Measure Directory Usage

du -sh /home/user/Documents


Explanation:

du estimates file space usage.

-s provides a summary of total size.

-h formats the output in human-readable form.

Step 2.3: Interpret the Results

Analyze how much space the directory is consuming.

Step 2.4: Identify Large Files or Folders

du -ah /home/user/Documents | sort -rh | head -n 10


Explanation:

Lists the top 10 largest files or directories.

-a shows all files, not just directories.

sort -rh sorts in reverse order, human-readable.

head -n 10 displays only the top 10 results.

Key Concept:
Finding large files or directories helps in targeting unnecessary files for deletion or archiving to free up disk space.

Summary

In this lab, I learned how to:

Use df to check overall disk space and filesystem usage

Use du to analyze specific directory space consumption

Identify the largest files or directories for storage management

Apply disk management practices to maintain optimal system performance
