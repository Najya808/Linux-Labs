# Lab 27: Password Policies

## What I Learned

In this lab, I explored the importance of password policies in securing a Linux system. I learned how to check and modify password expiry settings using the `chage` command, and I also reviewed how to enforce password complexity through system configuration files like `/etc/login.defs` and PAM. These practices help prevent weak or outdated passwords, reducing the risk of unauthorized access.

## Tasks I Performed

### ✅ Task 1: Check Current Password Policy

- Ran the command below to check password expiry details for a user:
  ```bash
  chage -l alice

  
✅ Task 2: Modify Password Expiry Options

Set the maximum password age to 60 days and the warning period to 7 days:
sudo chage -M 60 -W 7 alice
Verified the changes using:
chage -l alice
Explanation:

-M 60 sets password expiration to 60 days.
-W 7 gives a warning 7 days before the password expires.


✅ Task 3: Enforce Password Complexity (Optional)

Edited the file /etc/login.defs using:
sudo nano /etc/login.defs
Modified these lines:
PASS_MIN_LEN 8
PASS_MAX_DAYS 90
Optional PAM Rule:

To enforce complexity like requiring digits or special characters, I explored:

sudo nano /etc/pam.d/common-password
Added or ensured:

password requisite pam_pwquality.so retry=3 minlen=8
Key Commands Used

Command	Purpose
chage -l username	Displays password expiry info
chage -M days -W days username	Sets expiry and warning for passwords
nano /etc/login.defs	Adjust system-wide password policy
nano /etc/pam.d/common-password	Enforce advanced password rules using PAM
