## 🔧 Open Port Details

### ➤ **Port 53/tcp — Domain (DNS)**

- **Service:** DNS (Domain Name System)
- **Protocol:** TCP
- **Common Software:** BIND, Windows DNS, dnsmasq
- **Primary Use:**  
  - Resolving domain names to IPs  
  - Zone transfers between DNS servers  
  - DNS tunneling and fallback for large DNS responses

##  Potential Security Risks

**1. DNS Zone Transfer Exposure**
  - Zone transfers (AXFR) are used to replicate DNS databases across servers.
  - If misconfigured, an attacker can extract the full DNS zone file.
**2. DNS Tunneling**
  - Malicious actors can exfiltrate data or create C2 (command & control) channels via DNS over TCP.

**3. DNS Amplification Attacks**
  - If misconfigured and allows recursive queries, the server could be abused in DDoS reflection attacks.


Test for **zone transfer**:
  ```bash
  dig axfr @192.168.229.143 ragav.local
  ```
