#  Internship Task – Nmap Network Scan & Analysis

##  Task Overview

This task was assigned as part of my cybersecurity internship. The objective was to scan the local network, identify live hosts and open ports, analyze running services, and assess potential security risks.

---

##  Steps Followed

1. **Installed Nmap** from pacman
2. **Identified local IP address**:
   - `192.168.229.36/24`
3. **Ran TCP SYN scan** across the subnet:
   ```bash
   nmap -sS 192.168.229.0/24 -oN nmap_result.txt
   ```
4. Extracted scan results for active hosts

5. Performed in-depth analysis of open ports and services

6. Identified security risks

7. Saved and documented findings in this repository

## Repository Contents

**File	Description**
- nmap_result.txt : Raw Nmap output from the SYN scan
- analysis.md	: Detailed analysis of open ports and services
- README.md	:Summary of task steps and findings (this file)