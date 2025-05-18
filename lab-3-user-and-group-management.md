# Lab 3: User and Group Management

## 🎯 Objectives

- Understand how to create and manage users and groups in Linux.
- Learn how to assign users to groups and view current group memberships.

## 📚 What I Learned

In this lab, I explored how to manage users and groups using the command line:

- `useradd` creates a new user.
- `passwd` sets or changes a user’s password.
- `groupadd` creates a new group.
- `usermod -aG` adds a user to a specific group.
- `id` or `groups` shows which groups a user belongs to.

These commands are essential for system administration, especially when handling multi-user systems.

## 🔧 Commands Used

```bash
sudo useradd newuser                # Create a user
sudo passwd newuser                # Set password for the user
sudo groupadd newgroup             # Create a group
sudo usermod -aG newgroup newuser  # Add user to a group
id newuser                         # View user ID and group memberships
groups newuser                     # View groups for a user
