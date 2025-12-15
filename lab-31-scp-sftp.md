Lab 31: Using SCP and SFTP

What I Learned
In this lab, I learned how to securely transfer files between local and remote systems using SCP and SFTP. I practiced copying files in both directions, uploading and downloading using SFTP, and verifying file integrity using SHA-256 hashes. These tasks are important for maintaining security and data consistency in networked environments.

Tasks I Performed

Securely Copy a File with SCP (Local to Remote)
I created a sample file named example.txt on my local system. I used the following command to copy it to the remote system:

scp example.txt <remote_username>@<remote_ip>:~/


I learned that the colon : separates the remote host information from the destination path. This allowed me to securely transfer a file to the remote system.

Securely Copy a File with SCP (Remote to Local)
I retrieved the file from the remote system using:

scp <remote_username>@<remote_ip>:~/example.txt ~/Downloads/


This demonstrated transferring files back from the remote system to my local environment.

Upload a File Using SFTP
I started an SFTP session with:

sftp <remote_username>@<remote_ip>


Inside the session, I uploaded the file using:

put example.txt ~/


This helped me understand how to securely send files using SFTP.

Download a File Using SFTP
In the same SFTP session, I downloaded the file from the remote system using:

get ~/example.txt downloaded_example.txt


This ensured I could transfer files both ways securely.

Verify File Integrity
I generated SHA-256 hashes of the original file on my local system:

sha256sum example.txt


And of the transferred file on the remote system:

sha256sum ~/example.txt


Comparing the hash values confirmed that the files were identical and transferred securely.

Summary
This lab improved my ability to:

Use SCP to securely copy files between local and remote systems.

Use SFTP to upload and download files safely.

Verify data integrity using SHA-256 hashes.

These are essential skills for secure file management and maintaining reliable systems in both personal and professional environments.
