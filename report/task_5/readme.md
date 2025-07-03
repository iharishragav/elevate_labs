# Network Packet Capture and Analysis

## 📋 Overview
This project demonstrates live network packet capturing and basic protocol identification using **Wireshark**. It was performed as part of a practical exercise to develop packet analysis skills.

---

## 🧰 Tools Used
- **Wireshark** – Network protocol analyzer
- Terminal / Command Prompt
- Ping utility

---

## 🎯 Objective
Capture live network packets, identify at least 3 protocols, and export the data for analysis.

---

## 🚀 How to Reproduce

1. **Install Wireshark**
   - Download: pacman -S wireshark
2. **Start Wireshark**
   - Select your active network interface.
   - Click **Start Capture**.
3. **Generate Traffic**
   - Open a web browser and visit:
     - `google.com`
     - `search.brave.com`
   - Run in terminal:
     ```
     ping google.com
     ```
4. **Stop Capture**
   - Click **Stop** after ~30 seconds.
5. **Filter and Inspect**
   - Use filters such as:
     - `dns`
     - `icmpv6`
     - `tcp`
     - `tls`
6. **Export**
   - Save the capture file as `network-capture.pcap`.

---

## 📝 Files Included

- `network-capture.pcap` – Raw packet capture file
- `analysis.md` – Detailed report of findings
- `README.md` – This project overview
- `screenshots\` - contains screenshots of reports
---

## 🕵️‍♂️ Protocols Identified

- **DNS** – Domain Name queries and responses
- **ICMPv6** – Echo request/reply (ping)
- **ARP** – Address Resolution Protocol
- **TLS over TCP** – Encrypted HTTPS traffic

---

## 📌 Author Notes

**Name:** kamalesh  
**Internship Role:** Cybersecurity Intern  
**Date:** June 30, 2025

This project was created to practice real-world packet capture and protocol analysis skills for educational and research purposes only.
