# Born2beRoot - Virtual Machine Setup Project

Welcome to my Born2beRoot project, a virtualization and system administration project I completed as part of the 42 school curriculum. This project involved setting up a secure and functional server environment using VirtualBox (or UTM) and Debian.

## Features

### Operating System and Partition Setup
For this project, we had the choice beetween Debian and Rocky. I chose to use **Debian** due to its simplicity and robustness, making it ideal for me as a newbee to system administration.
- **Operating System:** Latest stable version of Debian.
- **Encrypted Partitions:** Created at least 2 encrypted partitions using LVM.
- **Minimal Services:** No graphical interface installed to ensure a lightweight server setup.
- **Security Modules:** Configured and activated AppArmor at startup.

### Server Configuration
I configured the server with the following specifications to meet the project requirements:
- **SSH Service:** Configured to run on port 4242, with root login disabled for security.
- **Firewall:** UFW configured to allow only port 4242.
- **Hostname:** Set to my 42 login ending with 42 (e.g., user42).
- **User Management:** Created a user with my login, belonging to user42 and sudo groups.
- **Strong Password Policy:**
  - Password expiry every 30 days.
  - Minimum 2 days between password changes.
  - 7-day warning before password expiry.
  - Password complexity requirements (length, character types, no user name, no repeated sequences).
- **Sudo Configuration:**
  - Limited to 3 authentication attempts.
  - Custom error message: (who doesn't like insults of the Holy Grail ?)
  - Logging of all sudo commands to `/var/log/sudo/`.
  - Enabled TTY mode and restricted PATH.

### Monitoring Script
I developed a script named `monitoring.sh` to provide real-time system information:
- **Script Name:** `monitoring.sh`
- **Functionality:** Displays system information every 10 minutes on all terminals.
- **Information Displayed:**
  - OS architecture and kernel version
  - Number of physical and virtual processors
  - RAM and memory usage
  - CPU utilization
  - Last reboot date and time
  - LVM status
  - Active connections
  - Number of users
  - IPv4 and MAC addresses
  - Number of sudo commands executed

### Bonuses Implemented
In addition to the mandatory requirements, I implemented several bonus features:
- **Advanced Partitioning:** I implemented a complex partition structure.
- **WordPress Setup:** I configured a functional WordPress website with lighttpd, MariaDB, and PHP.
- **Additional Service:** I installed and configured Docker to enhance server capabilities (I simulated a smart home as an exemple).

## Educational Value

Completing the Born2beRoot project provided substantial educational value by helping me to:

- **Understand Virtualization:** Gain hands-on experience with VirtualBox, learning how to create and manage virtual machines.
- **Strengthen Security Practices:** Implement strict security policies and configurations, including SSH hardening, firewall management, and strong password policies.
- **Learn System Administration:** Manage services, users, and partitions in a Linux environment, gaining practical experience with essential system administration tasks.
- **Automate Monitoring:** Develop and deploy scripts for real-time system monitoring, understanding how to gather and display critical system metrics.
- **Enhance Troubleshooting Skills:** Configure and troubleshoot complex setups involving encryption, LVM, AppArmor, and various services.

## Project Reflection

While at first, the Born2beRoot project may seem like following a mindless set of instructions, deep diving into it actually opens up the doors to the possibilities of system administration and server capacities. It offers a hands-on approach to understanding the intricacies and importance of server configurations and security measures.

Thank you for taking the time to check out my Born2beRoot project! This comprehensive setup serves as a solid foundation for any server-related tasks and further learning in system administration.
