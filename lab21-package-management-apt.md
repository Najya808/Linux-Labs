# Lab 21: Package Management with APT

## 🎯 Objectives

In this lab, I learned to:

- Use APT to manage software packages on Debian-based systems
- Update the package list from repositories
- Search for available packages
- Install and remove software using the command line

---

## What I Learned

### 🔹 Task 1: Update Package Lists

Keeping the package list updated ensures that the system knows about the latest versions of software.

#### 📌 Command used:
```bash
sudo apt-get update

🔹 Task 2: Search for a Package
This helps identify whether a package is available and what it's called in the repository.

📌 Command used:

apt-cache search editor
This command displayed a list of packages related to "editor". It's useful when you're not sure of the exact package name.

🔹 Task 3: Install and Remove a Package
Installing and removing packages lets me manage which software is available on my system.

📦 To install Vim:

sudo apt-get install vim
The system downloaded and installed Vim, a popular terminal-based text editor.

🗑️ To remove Vim:

sudo apt-get remove vim
This removed the Vim editor from my system but kept the configuration files.

🧩 Conclusion

Using APT, I now understand how to update package lists, search for software, and install or remove packages efficiently. These are essential skills for system administration.

I also learned:

Use sudo apt-get upgrade to upgrade installed software.
Use sudo apt-get autoremove to clean up unneeded packages.
Always update the package list (apt-get update) before installing new software.
This lab strengthened my confidence in using the APT package manager to maintain a clean, secure, and up-to-date Linux system.
