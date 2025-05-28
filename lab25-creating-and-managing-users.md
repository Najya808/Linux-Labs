# Lab 25: Creating and Managing Users

---

##  What I Learned

In this lab, I learned how to create, manage, and delete users in a Linux environment using key system administration commands like `useradd`, `passwd`, and `userdel`. I now understand how user accounts are stored and managed in files like `/etc/passwd`, and how to control basic user permissions.

---

## 🛠️ Tasks I Performed

### ✅ 1. Create a New User

- I opened the terminal and created a user named `newuser` using:
  ```bash
  sudo useradd newuser
  
✅ 2. Set a Password for the User
I set a password for newuser with:
sudo passwd newuser
What happened: I was prompted to type and confirm the password.
Key Concept: The passwd command updates authentication tokens for users.

✅ 3. Delete the User
I removed the user from the system with:
sudo userdel newuser
What happened: The user account was deleted, but their home directory remained.
To remove the home directory too, I used:
sudo userdel -r newuser

Key Concept: The -r flag also removes the user’s home directory and mail spool.

🏁 Summary

By completing this lab, I practiced essential Linux user management. I can now:

Add users to the system
Set secure passwords
Safely delete user accounts (with or without files)
These skills are important for system administrators to manage access and maintain a secure, multi-user environment.
