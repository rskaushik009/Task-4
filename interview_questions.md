

---

**1. What is a firewall?**
A firewall is a network security system that monitors and controls incoming and outgoing network traffic based on predetermined rules. It acts as a barrier between trusted and untrusted networks, filtering packets to allow safe traffic and block potentially harmful traffic.

---

**2. Difference between stateful and stateless firewall?**

* **Stateful firewall**: Tracks the state of active connections and makes filtering decisions based on the context of the traffic (e.g., related packets are allowed automatically).
* **Stateless firewall**: Filters packets solely based on predefined rules for each packet without tracking connection states.

---

**3. What are inbound and outbound rules?**

* **Inbound rules**: Control traffic coming **into** a system or network from external sources.
* **Outbound rules**: Control traffic going **out** from a system to external networks.

---

**4. How does UFW simplify firewall management?**
UFW (Uncomplicated Firewall) provides a simple command-line interface to manage firewall rules without directly configuring complex `iptables` syntax, making it easier for beginners and faster for experienced users.

---

**5. Why block port 23 (Telnet)?**
Telnet transmits data, including passwords, in plain text without encryption, making it vulnerable to interception and man-in-the-middle attacks. Blocking it prevents unauthorized remote access through this insecure protocol.

---

**6. What are common firewall mistakes?**

* Forgetting to allow SSH/remote access before enabling the firewall.
* Allowing too many open ports.
* Not updating firewall rules as services change.
* Misconfiguring rules so legitimate traffic is blocked.
* Not enabling logging to monitor activity.

---

**7. How does a firewall improve network security?**
A firewall reduces the attack surface by filtering unwanted or malicious traffic, preventing unauthorized access, mitigating malware spread, and enforcing security policies across networks.

---

**8. What is NAT in firewalls?**
NAT (Network Address Translation) is a method where the firewall modifies IP addresses in packet headers to map private internal addresses to public ones (and vice versa). It hides internal network structure and helps conserve public IP addresses.

---

