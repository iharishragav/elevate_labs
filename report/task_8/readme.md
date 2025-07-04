# OpenVPN Connection Workflow

This project documents using OpenVPN to connect to a VPN server for learning purposes.

---

## 📌 Requirements

- Arch Linux
- OpenVPN installed (`sudo pacman -S openvpn`)
- `.ovpn` configuration files from VPNGate 

---

## ✅ How to Connect

1. **Download configuration file**
   - For example: `vpngate_public-vpn-113.opengw.net_tcp_443(japan).ovpn`

2. **Inspect the file**
   ```bash
   cat ./config.ovpn
   ```

3. **Add compatible cipher if needed**
   - Edit `config.ovpn`:
   ```
   data-ciphers AES-128-CBC
   ```

4. **Connect**
   ```bash
   sudo openvpn --config ./config.ovpn
   ```
   - OR:
   ```bash
   sudo openvpn --config ./config.ovpn --data-ciphers AES-128-CBC
   ```

5. **Verify connection**
   ```bash
   curl ifconfig.me
   ```
   - IP should differ from your ISP.

6. **Test DNS leaks**
   - Go to https://dnsleaktest.com

7. **Disconnect**
   - Press `Ctrl+C` in your terminal.

---

## ⚠️ Important Notes

- VPNGate servers do **not** provide certificate verification.
- Do **not** use this setup for sensitive activities.
- Prefer modern ciphers and reputable VPN providers.

---

## 📸 Screenshots

Screenshots of all steps are available in `screenshots/` folder.

---

## 📁 Project Structure

```
openvpn-learning/
├── README.md
├── analysis.md
├── screenshots/
|   |__ installation.png
│   ├── initial-connection.png
│   ├── cipher-error.png
│   ├── successful-connection.png
│   ├── ip-verification.png
│   └── disconnection.png
└── config/
    └── vpngate_public-vpn-113.opengw.net_tcp_443(japan).ovpn
```

---

## 🚀 Quick Start

1. Clone or download this project
2. Install OpenVPN: `sudo pacman -S openvpn`
3. Download a `.ovpn` file from VPNGate
4. Follow the connection steps above
5. Document your experience!

---

## 🔗 Useful Resources

- [OpenVPN Official Documentation](https://openvpn.net/community-resources/)
- [VPNGate Public VPN Servers](https://www.vpngate.net/)
- [DNS Leak Test](https://dnsleaktest.com/)
- [What's My IP](https://ifconfig.me/)

---

## ⚖️ Legal Disclaimer

This project is for educational purposes only. Users are responsible for complying with local laws and regulations regarding VPN usage. Public VPN servers should not be used for sensitive or production activities.
