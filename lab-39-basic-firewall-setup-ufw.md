Lab 39: Basic Firewall Setup (UFW)

What I Learned
In this lab, I learned how to set up and configure a basic firewall on a Linux system using UFW (Uncomplicated Firewall). I practiced enabling the firewall, allowing specific services, verifying rules, and testing the setup. These skills are essential for improving system security and controlling network traffic.

Tasks I Performed
1. Install UFW

First, I updated the package list:

sudo apt update


Then, I ensured UFW was installed:

sudo apt install ufw


I learned that UFW is often pre-installed on Ubuntu, but installing it ensures it’s available for configuration.

2. Enable UFW

I enabled the firewall with:

sudo ufw enable


Key Concept: Enabling UFW starts the firewall with default rules — incoming connections are denied, outgoing connections are allowed.

3. Configure Basic Firewall Rules

Allow SSH connections (important for remote access):

sudo ufw allow ssh


SSH (Secure Shell) allows secure remote management of Linux systems.

Allow HTTP traffic (port 80):

sudo ufw allow http


This allows web traffic to reach the server.

4. Check UFW Status and Rules

I verified active rules:

sudo ufw status


For more detailed information:

sudo ufw status verbose


This confirmed that my rules were active and correctly configured.

5. Test the Configuration

Testing SSH access from another machine ensured connectivity.

Blocking SSH temporarily to see effect:

sudo ufw deny ssh


Re-enabling SSH to restore access:

sudo ufw allow ssh

Summary

In this lab, I learned to:

Install and enable UFW on Linux

Configure basic firewall rules for services like SSH and HTTP

Verify and test firewall rules

Control incoming network traffic to improve system security

Setting up a firewall is crucial for safeguarding servers and maintaining secure network access.
