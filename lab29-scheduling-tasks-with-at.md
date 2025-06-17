# Lab 29: Scheduling Tasks with `at`

## Introduction

The `at` command is a powerful tool in Linux that allows users to schedule tasks to run **once** at a specified future time. Unlike cron, which is for recurring jobs, `at` is ideal for one-time automation. This lab will walk you through the installation, usage, and management of tasks with `at`.

---

## Lab Tasks

### Task 1: Install `at` (if necessary)

#### Check Installation

To verify if `at` is installed:
```bash
at -V

Task 2: Schedule a One-Time Task with at

Schedule a job to write “Hello World” into a file one minute from now:

echo "echo 'Hello World' >> ~/hello.txt" | at now + 1 minute
This queues the command for execution one minute from now.
The at job will append the message to hello.txt in the user's home directory.

Task 3: Check Pending at Jobs

List all scheduled at tasks:

atq
Displays job ID and scheduled execution time.

Task 4: Remove a Scheduled Task with atrm

Remove a job using its job ID:

atrm <job_id>
Example:

atrm 1
This cancels the job with ID 1.
Conclusion

By completing this lab, I learned how to:

Install and activate the at command.
Schedule a one-time task.
List and remove scheduled tasks.
