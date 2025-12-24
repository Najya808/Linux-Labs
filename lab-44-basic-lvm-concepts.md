Lab 44: Basic LVM Concepts
What I Learned

In this lab, I learned the basic concepts of Logical Volume Manager (LVM) and how it provides flexible disk management compared to traditional partitioning. I practiced creating physical volumes, volume groups, and logical volumes, formatting and mounting them, and finally removing them safely. This lab helped me understand how LVM is used in real-world Linux systems to manage storage efficiently.

🔹 Introduction

Logical Volume Manager (LVM) is a disk management system in Linux that allows dynamic allocation and resizing of disk space. Unlike fixed disk partitions, LVM provides flexibility by abstracting physical storage into logical components that can be easily managed.

🧪 Lab Tasks Performed
🔹 Task 1: Check Existing Logical Volumes

To verify if any logical volumes already existed on the system, I ran:

sudo lvdisplay


Explanation:

lvdisplay shows detailed information about existing logical volumes.

This helps confirm the current LVM setup before making changes.

🔹 Task 2: Create a Volume Group and Logical Volume
✅ Create a Physical Volume

First, I checked available disks using:

sudo fdisk -l


I assumed /dev/sdb was an unused disk and initialized it as a physical volume:

sudo pvcreate /dev/sdb


Explanation:

pvcreate prepares a disk for LVM usage by labeling it as a physical volume.

✅ Create a Volume Group

Next, I created a volume group named myvg:

sudo vgcreate myvg /dev/sdb


Explanation:

A volume group combines one or more physical volumes into a storage pool.

✅ Create a Logical Volume

I created a logical volume named mylv with a size of 1GB:

sudo lvcreate -L 1G -n mylv myvg


Explanation:

Logical volumes are virtual partitions created from volume groups.

They can be resized or removed easily compared to traditional partitions.

✅ Format and Mount the Logical Volume

I formatted the logical volume with the ext4 filesystem:

sudo mkfs.ext4 /dev/myvg/mylv


Then I created a mount directory and mounted the volume:

sudo mkdir /mnt/mylv
sudo mount /dev/myvg/mylv /mnt/mylv


Explanation:

Formatting prepares the logical volume for data storage.

Mounting makes the volume accessible through the filesystem.

🔹 Task 3: Remove the LVM Setup After Testing

After testing, I safely removed the logical volume and related LVM components.

Unmount the logical volume:

sudo umount /mnt/mylv


Remove the logical volume:

sudo lvremove /dev/myvg/mylv


Remove the volume group:

sudo vgremove myvg


Revert the physical volume:

sudo pvremove /dev/sdb


Explanation:

Each step ensures that storage resources are released safely.

Proper removal prevents data corruption and frees disk space.

Summary

In this lab, I learned how to:

Inspect existing logical volumes

Create physical volumes, volume groups, and logical volumes

Format and mount logical volumes

Safely remove LVM configurations

These skills are essential for managing storage in enterprise Linux environments where flexibility, scalability, and efficient disk utilization are required.
