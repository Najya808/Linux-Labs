# Lab 26: Group Management Basics

## What I Learned

In this lab, I learned how to manage user groups in a Linux environment. I practiced creating new groups, adding users to them, and removing users from groups. I also understood how these actions help in organizing user permissions and access controls in a system. These skills are essential for system administration and secure user management.

## Tasks I Performed

### ✅ Task 1: Create a New Group

- Used `sudo groupadd developers` to create a new group.
- Verified its creation by checking `/etc/group` using:
  ```bash
  grep developers /etc/group

I also tried creating another group named designers with:

sudo groupadd designers

✅ Task 2: Add a User to the Group

Added an existing user (alice) to the developers group with:
sudo usermod -aG developers alice
Verified group membership using:
groups alice

✅ Task 3: Remove a User from the Group

Removed user alice from the developers group using:
sudo gpasswd -d alice developers
Confirmed removal by running:

groups alice

Key Commands Used

Command	Description

groupadd groupname	Creates a new group
usermod -aG group user	Adds a user to a group
gpasswd -d user group	Removes a user from a group
groups username	Displays groups that a user belongs to
grep groupname /etc/group	Checks if the group exists and lists members

Summary

I can now create and manage Linux groups.
I learned how to add and remove users from groups securely.
These steps help organize access controls in multi-user systems.
