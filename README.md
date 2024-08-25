# Safesquid-Labs-Task-2
Script Explanation
check_root: Ensures the script is run as root since many commands require root privileges.
audit_users_and_groups: Lists users and groups, checks for users with UID 0, and searches for users with empty or weak passwords.
audit_permissions: Finds world-writable files and directories and reports files with SUID/SGID bits.
audit_services: Lists all running services and checks against unauthorized services.
audit_firewall_and_network: Verifies firewall status and lists open ports.
check_ip_and_network: Displays IP configuration and checks for public/private IPs.
check_security_updates: Checks for available security updates.
monitor_logs: Monitors logs for suspicious activities, like failed SSH login attempts.
harden_server: Applies hardening measures such as securing SSH, disabling IPv6, securing GRUB, and configuring the firewall.
custom_security_checks: Placeholder for adding organization-specific checks.
generate_report: Generates a summary report of the audit and hardening process.

Configuration and Customization
Create a configuration file (config.sh) to manage custom security checks and specific settings:
# config.sh
# Custom Security Check Configuration
CUSTOM_CHECK_1="Check for unauthorized users"
CUSTOM_CHECK_2="Verify system integrity"

This Bash script automates the process of auditing security and hardening Linux servers. It performs various checks and applies hardening measures to ensure the server's security posture is robust.

## Features
- Audits users, groups, file permissions, services, and network configurations.
- Applies security hardening measures such as disabling SSH root login, securing the bootloader, and configuring the firewall.
- Customizable for organization-specific security checks.

## Installation

Clone the repository:
```bash
git clone https://github.com/Pranav1193/security-audit-script.git
cd security-audit-script

Run the script as root = sudo ./security_audit_and_hardening.sh

Customizing Security Checks
Modify the config.sh file to add custom security checks based on your organization's needs.
