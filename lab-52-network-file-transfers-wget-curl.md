Lab 52: Network File Transfers (wget/curl)
What I Learned

In this lab, I learned how to download files and fetch webpages using wget and curl. I practiced downloading files from URLs, saving webpage source code, and resuming interrupted downloads. I also explored practical command-line techniques for network-based file transfers.

Lab Objectives

Understand and utilize wget and curl for file transfers over the network

Download files and webpages

Explore advanced features like resuming partial downloads

Lab Tasks Performed

Task 1: Download a File Using wget

Steps:

Open the terminal.

Download a sample file using wget:

wget https://example.com/sample-file.txt


Explanation:
wget is a non-interactive utility for downloading files via HTTP, HTTPS, or FTP protocols.

Verify the download:

ls


Observation:
sample-file.txt appears in the directory.

Key Concept:
wget allows reliable downloading of files directly from the command line.

🔹 Task 2: View a Webpage's Source Using curl

Steps:

Fetch a webpage’s HTML source:

curl https://example.com


Observation:
The HTML source code of the webpage is displayed in the terminal.

Save the webpage source to a file:

curl https://example.com -o webpage.html


Open the saved file:

nano webpage.html


Key Concept:
curl fetches and outputs web resources, which can be redirected to files for offline analysis.

🔹 Task 3: Practice Partial Downloads

Steps:

Start downloading a large file and interrupt it:

wget https://example.com/large-sample-file.zip


Press Ctrl+C after a few seconds to stop the download.

Resume the interrupted download:

wget -c https://example.com/large-sample-file.zip


Observation:
The download resumes from where it was interrupted, instead of starting over.

Key Concept:
The -c flag in wget enables continuation of partially downloaded files, which is useful for large files or unstable network connections.

Summary

In this lab, I learned how to:

Use wget to download files from the internet

Use curl to fetch and save webpage source code

Resume interrupted downloads using wget -c

This lab strengthened my understanding of network file transfers via the command line and prepared me for advanced file management and automation tasks in network environments
