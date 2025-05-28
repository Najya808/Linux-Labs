# Lab 23: System Hardware Information

## What I Learned

In this lab, I learned how to use basic Linux commands to check and understand system hardware information. These commands help in system monitoring and troubleshooting by giving real-time information about CPU, memory, and disk usage. I practiced using open-source tools that are commonly available on all Linux distributions.

---

## Tasks I Performed

### 1. Checked CPU Information with `lscpu`

- I ran the `lscpu` command to view CPU architecture details.
- I learned how to identify the number of CPU cores, CPU vendor, and architecture type (like x86_64).
- Example output showed 4 CPU cores on a 64-bit Intel processor.

### 2. Monitored Memory Usage with `free -h`

- I used the `free -h` command to display total, used, and available RAM and swap memory.
- I understood how to read memory usage output in a human-readable format.
- For example, 2.3 GB of RAM was used out of 8 GB, and 4.2 GB was available.

### 3. Viewed Disk Space Usage with `df -h`

- I executed the `df -h` command to check disk space usage of all mounted filesystems.
- I was able to see how much space is used, available, and the mount points (like `/`).
- The output helped me see that 35 GB was used out of 100 GB on `/dev/sda1`.

## Summary

This lab helped me understand how to collect hardware information using three simple but powerful commands:
- `lscpu` for CPU
- `free -h` for RAM
- `df -h` for disk space

These tools are essential for Linux system administrators and useful in real-world troubleshooting scenarios.
