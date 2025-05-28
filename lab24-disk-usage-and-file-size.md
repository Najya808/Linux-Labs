# Lab 24: Disk Usage and File Size

## What I Learned

In this lab, I learned how to analyze disk usage and file sizes using Linux commands. I practiced identifying large files and directories to better manage system storage. These tasks are important for preventing storage issues and optimizing system performance in both personal and enterprise environments.

---

## Tasks I Performed

### 1. Checked Size of a Directory

- I used the command `du -sh /path/to/directory` to check the size of a single directory.
- I understood the use of:
  - `-s` for a summary view,
  - `-h` for human-readable output.
- This helped me get a quick overview of storage use.

### 2. Checked Sizes of Subdirectories

- I ran `du -sh /path/to/directory/*` to list sizes of all files and subdirectories.
- This command helped me pinpoint which folders were taking up the most space.

### 3. Identified the Largest Directories

- I executed `du -sh /path/to/directory/* | sort -hr` to sort directory sizes from largest to smallest.
- This allowed me to quickly detect storage-heavy directories that might need cleanup.

### 4. Performed Advanced Disk Usage Analysis

- I used `du -ah /path/to/directory | sort -hr` to see both files and directories sorted by size.
- I learned that the `-a` option includes files in the report, giving a detailed breakdown.
- This was useful for digging deeper into storage usage at the file level.

## Summary

This lab improved my ability to:
- Check overall and detailed directory sizes.
- Identify and sort large directories and files.
- Use `du` and `sort` effectively for disk management.

These are essential skills for maintaining clean, efficient Linux systems, especially in server environments where storage space can impact uptime and performance.
