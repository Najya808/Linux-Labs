# Lab 28: Scheduling Tasks with Crontab

## Lab Tasks

### Task 1: Listing User Cron Jobs

**Objective:** View existing cron jobs for the current user.

#### Steps:
1. Open your terminal.
2. List current cron jobs with:
   ```bash
   crontab -l
   
Task 2: Creating a New Cron Job

Objective: Schedule a script to run daily.

Steps:

Create a shell script:
nano ~/daily_script.sh
Add the following code:
#!/bin/bash
echo "Hello, World!" >> ~/cron_output.txt
Save and make it executable:
chmod +x ~/daily_script.sh
Open crontab editor:
crontab -e
Add this line to run the script at midnight daily:
0 0 * * * /bin/bash ~/daily_script.sh
Cron Format Explanation:

┌───────────── minute (0 - 59)
│ ┌───────────── hour (0 - 23)
│ │ ┌───────────── day of month (1 - 31)
│ │ │ ┌───────────── month (1 - 12)
│ │ │ │ ┌───────────── day of week (0 - 6) (Sunday = 0)
│ │ │ │ │
│ │ │ │ │
* * * * * command_to_execute
       
          
Task 3: Removing or Commenting Out a Cron Job

Objective: Modify or remove scheduled tasks.

Steps:

Open crontab editor:
crontab -e
To comment out a job, prefix it with #:
#0 0 * * * /bin/bash ~/daily_script.sh
To delete a job, remove the line entirely.
Confirm removal:
crontab -l
