Lab 41: Disk and Partition Management
What I Learned

In this lab, I learned how to view disks and partitions, create a new partition, and remove an existing partition using Linux command-line tools. I used utilities like lsblk, fdisk, and cfdisk to safely manage disk storage. This lab helped me understand how Linux organizes storage devices and how partitions are created and deleted.

Introduction

Disk and partition management is a core system administration skill. Linux provides powerful tools to inspect disks, create partitions, and modify storage layouts. Understanding these tools is essential when setting up servers, managing storage, or preparing disks for filesystems.

🧪 Lab Tasks Performed
🔹 Task 1: List Available Disks and Partitions

To view all block devices and their partitions, I ran:

lsblk


Explanation:

lsblk lists all disks and partitions in a tree-like format.

It shows disk names, sizes, mount points, and partition hierarchy.

To get detailed information about a specific disk (e.g., /dev/sda), I used:

sudo fdisk -l /dev/sda


Explanation:

fdisk -l displays the partition table.

It shows partition sizes, types, and disk layout.

sudo is required to access disk information.

🔹 Task 2: Create a Small Partition on a Test Device

To create a partition, I opened the partitioning tool:

sudo cfdisk /dev/sda


Steps Performed:

Selected Free Space using arrow keys.

Chose New to create a partition.

Entered partition size:

+500M


Selected the default Linux partition type.

Chose Write to save changes.

Typed yes to confirm.

Exited cfdisk.

Explanation:

cfdisk provides a user-friendly interface for partitioning.

Writing changes applies them to disk permanently.

Extreme caution is required to avoid data loss.

🔹 Task 3: Remove the Partition (If Not in Use)

To delete the partition, I reopened cfdisk:

sudo cfdisk /dev/sda


Steps Performed:

Selected the partition to remove.

Chose Delete.

Selected Write and typed yes to confirm.

Exited cfdisk.

Explanation:

Deleting a partition removes its entry from the partition table.

This should only be done if the partition is not mounted or in use.

 Summary

In this lab, I learned how to:

List disks and partitions using lsblk

View detailed disk information with fdisk

Create partitions using cfdisk

Delete partitions safely

Understand disk structures in Linux

This lab improved my confidence in managing Linux storage and reinforced the importance of caution when handling disk partitions to prevent data loss.
