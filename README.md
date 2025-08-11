# Task 4: Setup and Use a Firewall on Linux (UFW)

## Objective
Configure and test basic firewall rules to allow or block traffic on **port 22 (SSH)** using **UFW** on Linux.

---

## Tools
- **Linux Terminal**
- **UFW (Uncomplicated Firewall)**

---

## Steps to Perform

### 1️⃣ Check if UFW is installed
```bash
sudo ufw status
```
If UFW is not installed:
```bash
sudo apt install ufw
```

---

### 2️⃣ Enable the Firewall
```bash
sudo ufw enable
```
📸 **Screenshot :** Output of `sudo ufw status` showing `Status: active`.

---

### 3️⃣ View Current Firewall Rules
```bash
sudo ufw status numbered
```
📸 **Screenshot :** Initial list of rules before making changes.

---

### 4️⃣ Block Port 22 (SSH)
```bash
sudo ufw deny 22
```
📸 **Screenshot :** Output of `sudo ufw status numbered` showing `DENY 22`.

---

### 5️⃣ Test the Block
```bash
ssh localhost
```
Expected: **"Connection refused"** message.  
📸 **Screenshot :** Failed SSH connection attempt.

---

### 6️⃣ Allow Port 22 (SSH)
```bash
sudo ufw allow 22
```
📸 **Screenshot :** Output of `sudo ufw status numbered` showing `ALLOW 22`.

---

### 7️⃣ Remove Port 22 Rule
```bash
sudo ufw status numbered
sudo ufw delete <rule_number>
```
📸 **Screenshot :** Final `sudo ufw status numbered` with original state restored.

---

## Summary: How Firewall Filters Traffic
UFW is a frontend for **iptables**, simplifying firewall management.  
It filters network packets based on:
- **Port** (e.g., 22 for SSH)
- **Protocol** (TCP/UDP)
- **IP Address** (source/destination)

When a port is blocked, incoming packets to that port are dropped before reaching the application. When allowed, packets are passed to the application layer.

---

## Deliverables
1. Screenshot : UFW enabled
2. Screenshot : Initial rules list
3. Screenshot : Rule list showing `DENY 22`
4. Screenshot : Failed SSH connection attempt
5. Screenshot : Rule list showing `ALLOW 22`
6. Screenshot : Final rules after deletion

---

## Author
**Rishabh** – Cybersecurity Lab Exercise
