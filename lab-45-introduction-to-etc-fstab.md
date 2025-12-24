Lab 45: Introduction to /etc/fstab
What I Learned

In this lab, I learned about the purpose and importance of the /etc/fstab file in Linux systems. I understood how Linux uses this file to automatically mount filesystems at boot time. I also practiced reading existing entries, understanding their structure, and safely adding a new mount entry for a removable partition. This lab helped me understand how persistent mounts are configured in real Linux environments.

🔹 Introduction

The /etc/fstab (File Systems Table) file is a configuration file that defines how and where storage devices and partitions are mounted. It plays a critical role during system startup by ensuring required filesystems are mounted automatically with correct options.

🧪 Lab Tasks Performed
🔹 Task 1: Review Entries in /etc/fstab
✅ Open the /etc/fstab File

I opened the file using a text editor:

sudo nano /etc/fstab


Explanation:

This file contains information about filesystems that are mounted during boot.

It usually includes entries for the root filesystem, swap, and other mounted partitions.

✅ Understand the fstab Syntax

Each entry in /etc/fstab contains six fields:

Device – The partition or UUID (e.g., /dev/sda1)

Mount Point – Directory where the filesystem is mounted

Filesystem Type – ext4, swap, ntfs, etc.

Mount Options – defaults, ro, rw, noexec

Dump – Backup option (usually 0)

Pass – Filesystem check order during boot

Understanding this structure is important to avoid misconfiguration.

✅ Identify Existing Mounts

I scrolled through the file and reviewed existing mount entries, noting:

Which partitions are mounted

Their mount points

The filesystem types and options used

This helped me understand how the system storage is currently configured.

🔹 Task 2: Add or Edit a Mount Entry
✅ Identify the Removable Partition

I listed available block devices:

lsblk


From the output, I identified a removable partition (for example /dev/sdb1).

✅ Backup the Existing fstab File

Before making any changes, I created a backup:

sudo cp /etc/fstab /etc/fstab.bak


Explanation:

This ensures the system can be restored if an incorrect entry causes boot issues.

✅ Prepare a New Mount Entry

I decided to mount /dev/sdb1 at /media/usb and prepared the following entry:

/dev/sdb1 /media/usb ext4 defaults 0 2


I also ensured the mount point directory existed:

sudo mkdir -p /media/usb

✅ Edit /etc/fstab

I opened the file again:

sudo nano /etc/fstab


I added the new entry at the bottom, then saved and exited.

✅ Test the Configuration

To test without rebooting, I ran:

sudo mount -a


Explanation:

This command mounts all filesystems listed in /etc/fstab.

If there are errors, they appear immediately.

✅ Validate the Changes

I verified the mount using:

df -h


I confirmed that /media/usb appeared with the correct size and usage.

Summary

In this lab, I learned how to:

View and interpret /etc/fstab

Understand filesystem mount syntax

Safely back up configuration files

Add persistent mount entries

Test and validate mount configurations

This knowledge is essential for managing Linux systems, especially when working with additional storage devices and ensuring reliable filesystem mounts across reboots.
