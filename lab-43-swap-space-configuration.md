Lab 43: Swap Space Configuration
What I Learned

In this lab, I learned what swap space is and why it is important in Linux systems. I practiced checking existing swap usage, creating a swap file, enabling it, and making the configuration persistent across reboots. This lab helped me understand how swap acts as virtual memory and improves system stability when RAM is limited.

Introduction

Swap space is disk space used by Linux as an extension of physical memory (RAM). When RAM is fully utilized, inactive memory pages are moved to swap, preventing system crashes and improving reliability.

🧪 Lab Tasks Performed
🔹 Task 1: Check Current Swap Usage

To check if any swap space was already active, I ran:

swapon --show


Explanation:

This command lists all active swap areas.

If no output is shown, it means swap is not currently enabled.

To verify memory and swap usage, I used:

free -h


Explanation:

Displays memory and swap usage.

-h shows values in a human-readable format (MB/GB).

Key Concept:

Monitoring swap helps understand system memory behavior.

🔹 Task 2: Create a Swap File

I decided to create a 1GB swap file at /swapfile.

To create the swap file, I ran:

sudo fallocate -l 1G /swapfile


Explanation:

fallocate allocates disk space quickly.

-l 1G specifies the size of the swap file.

To secure the swap file, I changed its permissions:

sudo chmod 600 /swapfile


Explanation:

Ensures only the root user can access the swap file.

This is required for security reasons.

To convert the file into swap space, I executed:

sudo mkswap /swapfile


Explanation:

Initializes the file so the system recognizes it as swap space.

🔹 Task 3: Enable and Persist the Swap File

To activate the swap file, I ran:

sudo swapon /swapfile


To confirm that the swap file was enabled:

swapon --show


To make the swap configuration permanent across reboots, I edited the /etc/fstab file:

sudo nano /etc/fstab


I added the following line at the end of the file:

/swapfile none swap sw 0 0


Explanation:

This ensures the swap file is automatically enabled at system startup.

Key Concepts:

Swap persistence prevents the need to manually enable swap after reboot.

Proper swap management improves system reliability.

Summary

In this lab, I learned how to:

Check existing swap usage

Create a swap file using fallocate

Secure swap files with proper permissions

Enable swap using swapon

Make swap configuration persistent using /etc/fstab

Swap space plays a crucial role in maintaining system stability, especially on systems with limited RAM. Proper configuration helps prevent crashes and improves overall performance.
