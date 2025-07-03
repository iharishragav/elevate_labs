# Task 4 Analysis – Setup and Use a Firewall on Linux

## Objective
Configure and test firewall rules to secure the system and validate rule enforcement.

## Tools Used
- UFW (Uncomplicated Firewall) on Arch Linux

## Steps Performed
1. **Enabled UFW:**
 ```bash
 sudo ufw enable
 ```
2. **Listed current firewall rules:**

```bash
sudo ufw status numbered
```
- Confirmed initial status was active.

3. **Added rules to block inbound Telnet (port 23):**

```bash
sudo ufw deny 23
```
4. **Tested the Telnet block:**

```bash
telnet localhost 23
```
- Connection refused as expected.

5. **Added rules to allow SSH on port 22:**


```bash
sudo ufw allow 22
```
6. **Confirmed updated rules:**

```bash
sudo ufw status numbered
```
7. **Removed and re-added the SSH rule to test rule updates:**

```bash
sudo ufw deny 22
sudo ufw allow 22
```
8. **Checked service status:**

```bash
sudo systemctl status ufw
sudo systemctl disable ufw
sudo systemctl enable ufw
```
- Verified UFW remains active after re-enabling.

## Final Rules Applied

- Deny Telnet inbound.
- 
- Allow SSH inbound (with LIMIT).
- 
- Allow HTTP and HTTPS inbound.
- 
- Allow DNS inbound.
- 
- Allow outbound DNS, HTTP, HTTPS, and NTP.
- 
- Allow TCP 8080 inbound.
- 
- Deny SSH explicitly (demonstration).

## Observations
- The firewall successfully blocked Telnet connections.
- 
- Rules applied in the correct order.
- 
- The system remained accessible over allowed services.
- 
- Duplicate rules (e.g., 22/tcp LIMIT and 22 DENY) can conflict—needs cleanup.
- 
- UFW service was correctly enabled and verified.
- 
## Security Considerations
- Denying Telnet effectively blocks insecure protocols.
- 
- Allowing SSH should use LIMIT to mitigate brute force.
- 
- System should avoid conflicting allow/deny rules on the same port.
