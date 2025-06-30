# 📄 Network Packet Capture Report

**Date of Capture:** *June 30, 2025*  
**Tool Used:** Wireshark  
**Capture Duration:** ~30 seconds  
**Interface:** Active network interface on 192.168.115.x subnet

## 🎯 Objective

Capture live network packets and identify basic protocols and traffic types to develop packet analysis skills and protocol awareness.

## 📝 Summary of Activity

* Wireshark was started on the active network interface.
* Commands executed:
   * `ping google.com` (to generate ICMPv6 echo traffic)
   * Browsed `glean.com` and `search.brave.com` (generating DNS and HTTPS/TLS)
* Capture was stopped after sufficient packets were observed.
* Filters applied to inspect specific protocols.

## 🌐 Protocols Observed

At least **4** distinct protocols were identified:

### 1. DNS (Domain Name System)
* Queries and responses for:
   * `glean.com`
   * `search.brave.com`
   * `star-randsrv.bsg.brave.com`
* Example:
  ```
  Frame 1 Standard query A google.com Src: 192.168.115.36 Dst: 192.168.115.116
  ```
* IPv4 and IPv6 (AAAA) lookups.
* Reverse PTR lookup observed:
  ```
  Query PTR e.0.0.2...ip6.arpa Response: pnmaaa-as-in-x0e.1e100.net
  ```

### 2. ICMPv6 (Internet Control Message Protocol for IPv6)
* Echo Request and Reply packets confirming IPv6 connectivity.
* Example:
  ```
  Echo request seq=1 Echo reply seq=1
  ```

### 3. TLS over TCP
* Encrypted HTTPS communication:
   * TLSv1.2 Application Data exchanges with google and other servers.
* Example:
  ```
  Frame 6 TLSv1.2 Application Data Src: IPv6 client Dst: 2a03:2880:f284:1cd:face:b00c:0:167
  ```

### 4. ARP (Address Resolution Protocol)
* Address resolution within the local network:
   * Who has 192.168.115.116?
   * 192.168.115.116 is at MAC address.
* Example:
  ```
  Frame 19 ARP Request
  ```

## 🔍 Sample Packet Details

| Frame No. | Protocol | Source | Destination | Details |
|-----------|----------|--------|-------------|---------|
| 1 | DNS | 192.168.115.36 | 192.168.115.116 | Query A google.com |
| 5 | ICMPv6 | 2401:4900:...:d051 | 2404:6800:4007:835::200e | Echo request seq=1 |
| 6 | TLSv1.2 | 2401:4900:...:d051 | 2a03:2880:f284:... | Application Data |
| 19 | ARP | AzureWaveTec_8f:a2:b1 (local MAC) | Broadcast | Who has 192.168.115.116? |
| 29 | DNS | 192.168.115.116 | 192.168.115.36 | Response A search.brave.com |

## 📂 Captured File

**Filename:** `network-capture.pcap`

## 🖥️ Screenshots

* Wireshark running in terminal.(wireshark.png)
* Ping command output.(ping.png)
* Wireshark GUI with packet listings.(capture1,2,3.png)


## ✅ Outcome

The objective was achieved successfully. I demonstrated:
* Capturing live network traffic.
* Identifying key protocols (DNS, ICMPv6, ARP, TLS over TCP).
* Filtering and interpreting packets.
* Exporting the `.pcap` file.