# Lab 10: Environment Variables

## Objectives
- Understand what environment variables are and how they function within an operating system.
- Learn how to view, set, and unset environment variables using command-line tools in a Linux/Unix environment.
- Demonstrate the use of environment variables in scripts and shell operations.

## What I Learned
- Used `env` to view all current environment variables like `PATH`, `HOME`, and `USER`.
- Created a variable using `export MYVAR="Hello"` and accessed it via `echo $MYVAR`.
- Learned that exported variables are available to child processes.
- Verified that variables are session-based and don’t persist across new shell sessions unless defined in `.bashrc` or `.profile`.
- Removed variables using `unset MYVAR`, and confirmed with `echo $MYVAR` that it no longer existed.
- Learned practical use of environment variables in scripting and automation tasks.
