Lab 38: Systemd Services Overview

What I Learned
In this lab, I learned about systemd, the init system used by modern Linux distributions to manage services and system startup. I practiced listing active services and managing them using the systemctl command. This included starting, stopping, enabling, and disabling services, which are essential skills for Linux system administration.

Tasks I Performed
1. Understanding systemd Services

Systemd is responsible for initializing the system, managing background services, and controlling system states during boot and runtime. Services managed by systemd are called units, and service units end with .service.

2. Listing Running Services

I listed all active systemd services using:

systemctl list-units --type=service


This command displayed running services along with their status information such as:

LOAD – whether the service configuration is loaded

ACTIVE – whether the service is running

SUB – the detailed runtime state of the service

3. Starting a Service

To start a service, I used:

sudo systemctl start <service-name>


Example:

sudo systemctl start apache2


To confirm the service status, I ran:

systemctl status <service-name>

4. Stopping a Service

To stop a running service, I used:

sudo systemctl stop <service-name>


I verified the service state again using:

systemctl status <service-name>

5. Enabling a Service at Boot

To ensure a service starts automatically when the system boots, I enabled it using:

sudo systemctl enable <service-name>


This command creates a symbolic link so the service starts during system initialization.

6. Disabling a Service at Boot

To prevent a service from starting automatically at boot time, I disabled it using:

sudo systemctl disable <service-name>


This removes the boot-time startup configuration for the service.

Summary

In this lab, I learned how to:

Understand the role of systemd in Linux

List active systemd services

Start and stop services using systemctl

Enable and disable services to control boot-time behavior

These skills are critical for managing Linux servers, ensuring required services run reliably, and optimizing system performance and stability.
