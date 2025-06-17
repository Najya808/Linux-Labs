# Lab 30: SSH Basics

## Lab Tasks

### Task 1: Generate SSH Keys with ssh-keygen

#### Step 1: Open Terminal on Your Local Machine
- Use the terminal (Linux/macOS) or PowerShell/Windows Terminal on Windows.

#### Step 2: Generate SSH Key Pair
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

Step 3: Save the Key Pair

Press Enter to save to the default location: ~/.ssh/id_rsa.
Step 4: Set a Passphrase (Optional)

Press Enter if you don’t want to set a passphrase.

Task 2: Copy Public Key to Remote Host

Option 1: Using ssh-copy-id

ssh-copy-id username@remote_host
Option 2: Manual Method

Display the public key:
cat ~/.ssh/id_rsa.pub
SSH into the remote host:
ssh username@remote_host
Create the .ssh directory if it doesn’t exist:
mkdir -p ~/.ssh
Paste the copied public key:
echo "your_copied_public_key" >> ~/.ssh/authorized_keys

Task 3: SSH into the Remote Server Without a Password

Step 1: Connect to the Remote Host

ssh username@remote_host
Step 2: Verify Connection

ls -la
This confirms that SSH access works without password authentication.
