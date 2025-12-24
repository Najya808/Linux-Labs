Lab 40: Working with iptables
What I Learned

In this lab, I learned how to work with iptables, which is a powerful Linux firewall tool used to control network traffic. I practiced listing existing firewall rules, allowing or blocking specific ports, and saving firewall configurations so they persist after a reboot. This lab helped me understand low-level firewall management in Linux.

Introduction

iptables is a command-line utility used to configure the Linux kernel firewall. It allows system administrators to define rules that control incoming, outgoing, and forwarded network traffic based on IP addresses, ports, and protocols.

Tasks I Performed
🔹 Task 1: Listing Existing iptables Rules

To view the current firewall rules, I ran:

sudo iptables -L


Explanation:

-L lists all existing rules.

The output shows different chains such as INPUT, FORWARD, and OUTPUT.

Each chain has a default policy and optional rules.

Example Output:

Chain INPUT (policy ACCEPT)
target     prot opt source               destination

Chain FORWARD (policy ACCEPT)
target     prot opt source               destination

Chain OUTPUT (policy ACCEPT)
target     prot opt source               destination


This helped me understand how traffic is currently handled by the firewall.

🔹 Task 2: Allow or Block a Specific Port

To allow incoming HTTP traffic on port 80, I added this rule:

sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT


Explanation:

-A INPUT → Adds a rule to the INPUT chain

-p tcp → Uses TCP protocol

--dport 80 → Targets port 80 (HTTP)

-j ACCEPT → Allows the traffic

To block traffic instead, I learned that I can use:

sudo iptables -A INPUT -p tcp --dport 80 -j DROP


Use Case:
If a web server is running on port 80, allowing this port ensures the website is accessible.

🔹 Task 3: Saving iptables Rules

To make sure the rules persist after reboot, I saved them using:

sudo iptables-save > /etc/iptables/rules.v4


Explanation:

iptables-save exports current firewall rules.

/etc/iptables/rules.v4 stores IPv4 rules permanently.

The exact path may differ depending on the Linux distribution.

Saving rules is important because iptables rules are lost after reboot if not saved.

✅ Summary

In this lab, I learned how to:

View existing iptables firewall rules

Allow or block specific ports using iptables

Save firewall configurations for persistence

Understand how Linux handles network traffic at a low level

This lab strengthened my knowledge of Linux security and firewall management, which is essential for server administration and system hardening.

