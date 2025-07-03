#  Full Vulnerability Scan Report – Localhost

**Scanner**: OpenVAS (Greenbone GVM via Docker)  
**Scan Type**: Full and Fast  
**Target**: 127.0.0.1  
**Scan Date**: 26 June 2025  
**Analyst**: Kamalesh

---

##  Summary

| Item                 | Result               |
|----------------------|----------------------|
| Total Vulnerabilities | 24                  |
| Critical              | 3                   |
| High                  | 6                   |
| Medium                | 8                   |
| Low                   | 7                   |
| Open Ports            | 22, 80, 631, 5353   |
| Services Detected     | SSH, HTTPD, CUPS    |

---

##  Top Vulnerabilities

### 1. CVE-2023-38408 – OpenSSH RCE

- **Severity:** Critical  
- **Description:** Vulnerability allows unauthenticated code execution.  
- **Fix:** Upgrade OpenSSH to version >= 9.3

---

### 2. CVE-2022-0185 – Linux Kernel Heap Exploit

- **Severity:** Critical  
- **Description:** Heap buffer overflow in kernel namespace handling  
- **Fix:** Update Linux kernel using `sudo pacman -Syu`

---

### 3. CVE-2021-44228 – Apache Log4j Log4Shell

- **Severity:** Critical  
- **Fix:** Remove vulnerable JARs, upgrade Log4j to >= 2.17

---

##  Fixes (Applied Simulated)

- Updated system packages  
- Disabled remote CUPS and Avahi  
- Applied UFW firewall: blocked 5353/UDP, 631/TCP  
- Scheduled monthly scans

---

##  Screenshots 

- `scan_overview.png`  
- `cve_openssh_detail.png`  
- `after_patch_summary.png`

---

##  Final Notes

- Results show typical weaknesses on an unpatched Linux system.  
- Routine scans + minimal services + patching = secure baseline.

