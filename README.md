# Firewall Configuration on Kali Linux (UFW)

This repository documents the configuration and testing of basic firewall rules on Kali Linux using UFW. The firewall was configured from a clean initial state, rules were applied and validated, and the system was returned to its intended configuration.

---

## UFW Setup

```bash
sudo apt update
sudo apt install ufw
sudo ufw enable
sudo ufw status verbose
```

---

## Rule Management

### Check existing rules
```bash
sudo ufw status numbered
```

### Block Telnet (port 23)
```bash
sudo ufw deny 23
sudo ufw status numbered
```

### Test Telnet block
```bash
telnet localhost 23
```

### Allow SSH (port 22)
```bash
sudo ufw allow 22
sudo ufw status numbered
```

### Allow Telnet 
```bash
sudo ufw status numbered
sudo ufw allow 23
```

---

## Final Verification

```bash
sudo ufw status verbose
```

---

## Conclusion

UFW was successfully configured to manage incoming traffic by adding, testing, and removing specific firewall rules. The process confirmed that the firewall correctly blocks and allows traffic as configured, demonstrating effective basic firewall administration on Kali Linux.