# Lab 22: Package Management with YUM/DNF

## Objectives

In this lab, I learned to:

- Understand basic package management using YUM and DNF
- Update package metadata and install software
- Search for and remove packages using the command line
- Work confidently on RPM-based Linux distributions like CentOS, Fedora, or RHEL

---

## What I Learned

### 🔹 Task 1: Update Package Lists

Keeping the package list updated ensures access to the latest software versions and dependencies.

#### 📌 Command used:
```bash
sudo yum update
# or
sudo dnf update

These commands refreshed the system’s metadata and listed packages available for update.

To apply updates:

sudo yum upgrade
# or
sudo dnf upgrade
This upgraded all upgradable packages to the latest versions.

🔹 Task 2: Search for a Package
I learned how to search for available software in enabled repositories.

📌 Command used:

yum search vim
# or
dnf search vim
This listed all packages related to Vim, including descriptions and availability.

🔹 Task 3: Install and Remove a Package
Managing software on an RPM-based system includes installing and removing packages.

📦 To install Vim:

sudo yum install vim
# or
sudo dnf install vim
Vim was successfully installed on the system.

🧪 To verify:

vim --version
Output showed version info, confirming Vim was correctly installed.

🗑️ To remove Vim:

sudo yum remove vim
# or
sudo dnf remove vim
This cleanly uninstalled Vim from the system.

Conclusion

Using YUM and DNF, I learned how to:

Refresh package metadata (yum/dnf update)
Upgrade installed packages (yum/dnf upgrade)
Search for new software (yum/dnf search)
Install and remove packages (yum/dnf install, yum/dnf remove)
These package managers are essential for maintaining and securing RPM-based systems. I now feel more confident in managing Linux software using command-line tools.
