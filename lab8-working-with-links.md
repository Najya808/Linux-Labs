# Lab 8: Working with Links

## Objectives
- Understand the difference between hard links and symbolic links.
- Learn how to create hard and symbolic links using command-line tools.
- Explore and compare the file sizes and inodes of hard and symbolic links.

## What I Learned
- Hard links directly reference the inode of the original file.
- Symbolic (soft) links reference the file name/path, not the inode.
- Hard links can’t span across different file systems, but symbolic links can.
- Used `ln` for hard links and `ln -s` for symbolic links.
- Used `ls -l` and `ls -i` to compare file details and inodes.
