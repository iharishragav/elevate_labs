# VPN Connection Analysis Report

## 📌 Overview
This report documents the process of connecting to a VPN server using OpenVPN on Arch Linux, including encountered errors, troubleshooting steps, and their solutions.

---

## 🖥️ System Details
- **OS:** Arch Linux
- **OpenVPN Version:** 2.6.14
- **VPN Service:** VPNGate (public server in Japan)
- **Config File:** `vpngate_public-vpn-113.opengw.net_tcp_443(japan).ovpn`

---

## ✅ Steps Performed
1. Installed OpenVPN
2. Obtained `.ovpn` configuration files
3. Attempted connection to the VPN server
4. Verified IP address changes and encryption
5. Compared browsing speed and DNS leaks
6. Disconnected the VPN and re-tested connectivity

---

## ❌ Initial Errors Encountered

### 1️⃣ Cipher Negotiation Failure
```
OPTIONS ERROR: failed to negotiate cipher with server. Add the server's cipher ('AES-128-CBC') to --data-ciphers (currently 'AES-256-GCM:AES-128-GCM:CHACHA20-POLY1305') if you want to connect to this server.
```

**Reason:** The server was using an older cipher (`AES-128-CBC`) not included in OpenVPN's default `--data-ciphers` list.

---

### 2️⃣ No Server Certificate Verification
```
WARNING: No server certificate verification method has been enabled. See http://openvpn.net/howto.html#mitm for more info.
```

**Reason:** VPNGate servers are community-run and do not have certificates trusted by OpenVPN by default.

---

## 🛠️ Solutions Applied

### 🔹 Fix for Cipher Negotiation
Added AES-128-CBC to allowed ciphers.

**Option 1:** Command line flag:
```bash
sudo openvpn --config ./config.ovpn --data-ciphers AES-128-CBC
```

**Option 2:** Added line to `.ovpn` file:
```
data-ciphers AES-128-CBC
```

✅ This allowed negotiation to proceed successfully.

### 🔹 Note on Certificate Verification
Since this was a learning exercise on a test server, I ignored the warning. **(Not recommended in production environments.)**

---

## 🟢 Successful Connection
After applying the fixes, OpenVPN output:
```
Initialization Sequence Completed
Data Channel: cipher 'AES-128-CBC', auth 'SHA1'
```

I confirmed the new IP address using:
```bash
curl ifconfig.me
```

✅ The traffic was routed through the VPN server in Japan.

---

## 📸 Screenshots
Screenshots were taken for each of these steps:
- Initial connection attempts
- Cipher error
- Edited configuration file
- Successful connection
- IP verification
- DNS leak test
- Disconnection

---

## 🧭 Learnings
- Cipher negotiation must match exactly between client and server
- Public VPN servers often lack proper TLS verification
- DNS leak testing is essential to confirm anonymity
- Older ciphers like AES-128-CBC are functional but not recommended for sensitive data

---

## 🔒 Security Recommendations
- Prefer servers that support modern ciphers (`AES-256-GCM`)
- Always verify server certificates
- Avoid public VPN servers for production workloads or private browsing
- Use reputable VPN providers with proper security implementations
- Regularly test for DNS leaks and IP address verification

---

## 📝 Conclusion
The VPN connection was successfully established after resolving cipher compatibility issues. While public VPN servers like VPNGate are useful for learning and testing, they should not be relied upon for security-critical applications due to potential certificate verification issues and the use of older encryption standards.
