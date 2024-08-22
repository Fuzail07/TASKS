NOTE : Copy the content of the file and make them executable




Here's a `README.md` file that explains the two scripts provided:

---

# Linux System Monitoring and Security Audit Scripts

## Overview

This repository contains two Bash scripts designed for real-time system monitoring and comprehensive security auditing on Linux servers. The first script provides continuous system resource monitoring, while the second script performs detailed security audits and applies hardening measures.

## Script 1: Real-Time System Monitoring

### Description

This script provides real-time monitoring of essential system metrics such as CPU and memory usage, network statistics, disk usage, system load, memory statistics, and the status of critical services. It refreshes the information every few seconds, making it ideal for live system monitoring.

### Features

- **Top CPU and Memory Processes**: Displays the top 10 processes consuming the most CPU and memory.
- **Network Statistics**: Shows active connections, packet drops, and bandwidth usage.
- **Disk Usage**: Displays usage statistics for all mounted file systems.
- **System Load**: Reports the system load average over the last 1, 5, and 15 minutes.
- **Memory Usage**: Displays current memory usage, including free and used memory.
- **Service Monitoring**: Monitors the status of critical services like SSH and Nginx.

### Usage

 **Adjust the Update Frequency**:
   - The script is set to refresh every 5 seconds by default. You can change this by modifying the `UPDATE_FREQUENCY` variable at the beginning of the script.

### Requirements

- Requires root or sudo privileges to execute.
- Tools like `ps`, `netstat`, `tcpdump`, and `ifconfig` should be installed on the system.

---

## Script 2: Security Audit and Hardening

### Description

This script automates the process of auditing a Linux server's security configuration and applies basic hardening measures. It checks for weak passwords, improper file permissions, firewall status, security updates, and more.

### Features

- **User and Group Audits**: Lists all users and groups, identifies users with root privileges, and checks for weak or missing passwords.
- **File and Directory Permissions**: Scans for world-writable files and directories and checks SSH directory permissions.
- **Service Audits**: Lists all running services, checks the status of critical services, and identifies services listening on non-standard ports.
- **Firewall and Network Security**: Verifies firewall status, lists open ports, and checks for insecure network configurations like IP forwarding.
- **IP and Network Configuration**: Differentiates between public and private IP addresses and checks sensitive service exposure.
- **Security Updates and Patching**: Checks for available security updates and ensures the server is configured for automatic updates.
- **Log Monitoring**: Searches for suspicious log entries, especially failed SSH login attempts.
- **SSH Hardening**: Disables password-based login for root and ensures secure storage of SSH keys.
- **IPv6 Disabling**: Disables IPv6 if not required and adjusts service configurations accordingly.

### Usage

**Custom Security Checks**:
   - The script allows for custom security checks defined in the `custom_security_checks.conf` file. You can edit this file to add additional checks specific to your environment.

### Requirements

- Requires root or sudo privileges to execute.
- Tools like `getent`, `netstat`, `ufw`, `apt`, and `systemctl` should be installed on the system.

## Contribution

Feel free to fork the repository and submit pull requests for any improvements or additional features.


Replace the placeholder GitHub URLs with your actual repository URLs. This `README.md` provides clear instructions and descriptions for both scripts, making it easy for users to understand and use them effectively.
