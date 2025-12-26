Lab 57: Simple Log Rotation
What I Learned

In this lab, I learned the fundamentals of log rotation in Linux using logrotate. I explored default log rotation configurations, inspected service-specific rotation rules, and manually forced log rotation to understand how logs are managed, compressed, and retained to prevent disk space issues.

🎯 Lab Objectives

Understand the basics of log rotation in Linux

Learn how to inspect and interpret logrotate configuration files

Manually trigger log rotation and verify results

🧪 Lab Tasks Performed

🔹 Task 1: Check Default Configuration in /etc/logrotate.conf

Step 1.1: Access the Configuration File

cat /etc/logrotate.conf


Observation:
The default configuration defines how logs are rotated system-wide.

Common Settings Found:

weekly
rotate 4
create
compress


Key Concepts:

weekly → Logs are rotated once per week

rotate 4 → Keeps 4 old log files

compress → Old logs are compressed (usually .gz)

create → New log files are created after rotation

Default Behavior:

Logs rotate weekly

Old logs are compressed

Four previous log files are retained

New logs maintain original permissions

🔹 Task 2: Inspect a File in /etc/logrotate.d/

Step 2.1: Navigate to Configuration Directory

cd /etc/logrotate.d


Step 2.2: List Available Configurations

ls


Step 2.3: Open a Specific Configuration File

cat apache2


Example Configuration Observed:

/var/log/apache2/*.log {
    weekly
    missingok
    rotate 14
    compress
    delaycompress
    notifempty
    create 640 root adm
    sharedscripts
    postrotate
        if [ -f /var/run/apache2.pid ]; then
            /etc/init.d/apache2 reload > /dev/null
        fi
    endscript
}


Key Settings Explained:

missingok → No error if log file is missing

notifempty → Skip rotation if log is empty

delaycompress → Compress logs one rotation later

postrotate / endscript → Commands executed after rotation

Key Concept:
Service-specific rules override global defaults and allow fine-grained log management.

🔹 Task 3: Manually Force Log Rotation

Step 3.1: Force Log Rotation

sudo logrotate --force /etc/logrotate.conf


Explanation:
The --force option rotates logs regardless of the rotation schedule.

Step 3.2: Verify Log Rotation

ls -ltr /var/log


Observations:

New rotated log files appear

Older logs may be compressed as .gz

File timestamps confirm recent rotation

Key Concept:
Manual log rotation is useful for testing configurations and immediate cleanup.

Summary

In this lab, I learned how to:

Inspect default logrotate configurations

Understand key log rotation parameters

Analyze service-specific rotation rules

Manually force and verify log rotation
