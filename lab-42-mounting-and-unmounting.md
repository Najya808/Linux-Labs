Lab 42: Mounting and Unmounting
What I Learned

In this lab, I learned how mounting and unmounting works in Linux. I practiced creating a mount point, mounting a partition to a directory, and safely unmounting it. This lab helped me understand how Linux attaches storage devices to the filesystem and how data is accessed securely.

Introduction

In Linux, storage devices such as hard disks, partitions, and USB drives are accessed by mounting them to directories called mount points. Mounting makes the filesystem available, while unmounting safely detaches it to prevent data loss.

🧪 Lab Tasks Performed
🔹 Task 1: Create a Mount Point Directory

To create a directory that will act as a mount point, I ran:

sudo mkdir /mnt/my_mount


Explanation:

mkdir creates a new directory.

/mnt/my_mount is the mount point where the filesystem will be attached.

sudo is required because /mnt is a system directory.

Key Concept:

A mount point is a directory used to access a mounted filesystem.

🔹 Task 2: Mount a Partition or Image File

First, I identified available disks and partitions using:

lsblk


Explanation:

lsblk lists all block devices and partitions.

I noted the device name (e.g., /dev/sdb1).

To mount the partition, I used:

sudo mount /dev/sdb1 /mnt/my_mount


Explanation:

mount attaches the filesystem to the directory.

/dev/sdb1 is the partition being mounted.

/mnt/my_mount is the mount point.

Linux automatically detects the filesystem type, but it can also be specified using -t (e.g., ext4).

Key Concepts:

Mount command: Attaches a filesystem to the Linux directory tree.

Filesystem types: ext4, ntfs, xfs, etc.

🔹 Task 3: Unmount the Filesystem

After finishing work with the mounted filesystem, I safely unmounted it using:

sudo umount /mnt/my_mount


Explanation:

umount detaches the filesystem from the mount point.

The directory must not be in use while unmounting.

This ensures all data is written properly and prevents corruption.

Key Concept:

Unmounting safely removes a filesystem from the system.

Summary

In this lab, I learned how to:

Create mount point directories

Identify disk partitions using lsblk

Mount filesystems using the mount command

Safely unmount filesystems using umount

Understand how Linux manages storage access

These skills are essential for managing external drives, additional storage, and server disk configurations in Linux environments.
