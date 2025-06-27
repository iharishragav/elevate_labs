
---

```markdown
# Task 4 – Linux Firewall Setup Report
```

This document summarizes the configuration of UFW on Arch Linux.

## Commands Used

```bash
# Enable UFW
sudo ufw enable

# List rules
sudo ufw status numbered

# Block Telnet
sudo ufw deny 23

# Test Telnet
telnet localhost 23

# Allow SSH
sudo ufw allow 22

# Deny SSH (demonstration)
sudo ufw deny 22

# Check UFW status
sudo systemctl status ufw

# Disable/Enable UFW service
sudo systemctl disable ufw
sudo systemctl enable ufw
```
## How Firewall Filters Traffic
- Deny rules block unsolicited connections to specified ports.
- 
- Allow rules permit trusted services.
- 
- Limit rules restrict connection attempts to mitigate brute force.

- ### Default policy:

    - Deny incoming.

    - Allow outgoing.


## Deliverables
- analysis.md	: Detailed analysis of open ports and firewall configurations

- readme.md (this document)

- Screenshot(s) of sudo ufw status numbered showing the active rules

## 👨‍💻 Author

**Name:** kamalesh  
**Internship Role:** Cybersecurity Intern  
**Date:** June 27, 2025

