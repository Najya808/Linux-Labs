Lab 59: Monitoring with top and htop
What I Learned

In this lab, I learned how to monitor system performance and running processes using the top and htop commands. I explored how to install htop, compared it with top, and practiced sorting processes by CPU and memory usage. This lab helped me understand real-time system monitoring, which is essential for system administration and troubleshooting.

🎯 Lab Objectives

Understand the purpose of system monitoring tools top and htop

Learn how to install and run htop

Compare the interfaces of top and htop

Sort processes by CPU and memory usage

Monitor system performance in real time

🧪 Lab Tasks Performed

🔹 Task 1: Installation of htop

Step 1.1: Update Package Manager

For Debian-based systems:

sudo apt update


For RedHat-based systems:

sudo yum check-update


Explanation:
Updating the package manager ensures access to the latest package versions.

Step 1.2: Install htop

For Debian-based systems:

sudo apt install htop


For RedHat-based systems:

sudo yum install htop


Observation:
The htop package installs successfully and becomes available as a system monitoring tool.

🔹 Task 2: Running top and htop

Step 2.1: Run top

top


Observation:
The top command displays:

System uptime

Load average

CPU and memory usage

A list of running processes

Key Concept:
top is a default Linux utility used for real-time process monitoring.

Step 2.2: Run htop

htop


Observation:

Color-coded display

Easier navigation using arrow keys

Interactive process management

Key Concept:
htop provides a more user-friendly and interactive interface than top.

🔹 Task 3: Comparing Interfaces

Differences Observed:

Interactivity:

top relies on keyboard shortcuts

htop allows arrow-key navigation

Visuals:

top has a text-based layout

htop uses colors for CPU, memory, and process states

🔹 Task 4: Sorting Processes

Step 4.1: Sort by CPU Usage

In top:

Press P


In htop:

Press F6 → Select CPU% → Enter


Observation:
Processes consuming the most CPU appear at the top of the list.

Step 4.2: Sort by Memory Usage

In top:

Press M


In htop:

Press F6 → Select MEM% → Enter


Observation:
Memory-heavy processes are easily identified.

🔹 Task 5: Exiting the Tools

Exit both top and htop:

Press q


Summary

In this lab, I learned how to:

Monitor system processes using top and htop

Install htop using a package manager

Compare basic and advanced monitoring tools

Sort processes by CPU and memory usage

Analyze system performance in real time
