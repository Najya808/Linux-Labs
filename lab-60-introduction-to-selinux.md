Lab 60: Introduction to SELinux
What I Learned

In this lab, I learned the fundamentals of Security-Enhanced Linux (SELinux), including what it is, why it is used, and how it enhances system security. I practiced checking SELinux status, changing its operational modes, and verifying configuration changes after a system reboot. This lab helped me understand how SELinux enforces security policies on Linux systems.

🎯 Lab Objectives

Understand the basics of Security-Enhanced Linux (SELinux)

Learn how to check SELinux status

Change SELinux modes between Enforcing and Permissive

Verify SELinux configuration changes after reboot

Understand real-world troubleshooting scenarios involving SELinux

🧪 Lab Tasks Performed

🔹 Task 1: Check SELinux Status

Step 1: Open Terminal
Launch the terminal application on the Linux system.

Step 2: Verify SELinux Status

sestatus


Explanation:
The sestatus command displays:

SELinux status (enabled/disabled)

Current mode (Enforcing, Permissive, or Disabled)

Policy type in use

Key Concepts:

SELinux: A Linux security module that enforces mandatory access control (MAC)

Enforcing Mode: Policies are enforced and access violations are blocked

Permissive Mode: Policies are not enforced but violations are logged

🔹 Task 2: Change SELinux Mode (Permissive / Enforcing)

Step 1: Edit SELinux Configuration File

sudo vi /etc/selinux/config


Explanation:
This configuration file controls the default SELinux mode at system boot.

Step 2: Modify SELINUX Mode

Locate the line:

SELINUX=


Change it to one of the following:

For Permissive Mode:

SELINUX=permissive


For Enforcing Mode:

SELINUX=enforcing


Step 3: Save and Exit

In vi:

Press Esc → type :wq → press Enter


Key Concept:
Changes in /etc/selinux/config require a system reboot to take effect.

🔹 Task 3: Verify Changes After Reboot

Step 1: Reboot the System

sudo reboot


Step 2: Confirm SELinux Mode

sestatus


Observation:
The SELinux mode reflects the updated configuration after reboot.

🔹 Case Study: Troubleshooting with SELinux

Scenario:
A system administrator needs to troubleshoot a software installation that is failing due to SELinux restrictions.

Approach:

Temporarily switch SELinux to Permissive mode

Monitor logged policy violations

Fix the root cause before returning SELinux to Enforcing mode

Key Takeaway:
Permissive mode is useful for debugging without completely disabling SELinux.

Summary

In this lab, I learned how to:

Check the current SELinux status using sestatus

Understand SELinux modes and their impact on system security

Modify SELinux configuration safely

Verify SELinux changes after reboot

Apply SELinux knowledge to real-world troubleshooting scenarios
