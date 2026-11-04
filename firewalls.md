# Firewalls in Cybersecurity

---

## 1. What is a Firewall?
* A **firewall** is a network security system that acts as a barrier between a trusted internal network and untrusted external networks (such as the Internet).
* **Core Function:** Monitors, filters, and controls incoming and outgoing network traffic based on predetermined security rules.

---

## 2. How Firewalls Work
Firewalls operate at the boundaries of networks or hosts to inspect data packets.

* **Packet Inspection:** When data travels across a network, it is broken down into small units called **packets**. Each packet contains a header (source/destination IP address, port numbers, protocol) and a payload (actual data).
* **Rule Sets (Access Control Lists - ACLs):** Firewalls evaluate packet headers against defined rules (e.g., *Allow traffic from IP X on Port 80*, *Block incoming traffic on Port 22*).
* **Actions:**
  1. **Allow / Accept:** Permits the packet to pass through.
  2. **Deny / Block:** Drops the packet and sends a response to the sender (or drops it silently via "Drop").
  3. **Log:** Records details about the traffic for auditing.

---

## 3. Key Types of Firewalls

### A. Deployment Methods
* **Hardware Firewalls:** Physical appliances placed between the internal network and the router/gateway. Best for protecting entire networks.
* **Software Firewalls:** Programs installed directly on individual endpoints (hosts) to control traffic entering/leaving that specific device (e.g., Windows Defender Firewall).
* **Cloud-Based / Managed Firewalls (FWaaS):** Delivered as a cloud service to protect cloud infrastructures, remote workforces, and distributed applications.

### B. Inspection Technologies
1. **Packet-Filtering Firewall (Layer 3/4):**
   * Inspects basic packet information (IP addresses, ports, protocols).
   * Fast and low-overhead, but lacks context—cannot inspect packet contents.
2. **Stateful Inspection Firewall (Layer 3/4):**
   * Tracks active connections and the state of network sessions (TCP handshake, active streams).
   * Blocks traffic that does not match an established, legitimate connection.
3. **Application-Level Gateway / Proxy Firewall (Layer 7):**
   * Acts as an intermediary between client and server.
   * Inspects traffic at the application layer (e.g., HTTP, FTP, DNS) and deep-analyzes actual payload data.
4. **Next-Generation Firewall (NGFW):**
   * Combines traditional stateful inspection with advanced features:
     * **Deep Packet Inspection (DPI)**
     * **Intrusion Prevention Systems (IPS)**
     * **TLS/SSL Encrypted Traffic Inspection**
     * **Application & User Identification**
     * **Threat Intelligence Integration**

---

## 4. Why Firewalls are Essential Today

1. **Defense Against Unauthorized Access:** Prevents unauthorized external users or automated bots from gaining remote entry to private systems.
2. **Mitigation of Malware & Ransomware:** Blocks communication with known malicious command-and-control (C2) servers, preventing malware from executing exfiltration or payload downloads.
3. **Protection for Hybrid & Remote Workplaces:** Cloud firewalls and NGFWs secure remote users connecting to enterprise cloud assets outside traditional perimeter boundaries.
4. **Data Loss Prevention (DLP):** Monitors outgoing traffic to prevent sensitive data, credentials, or proprietary information from leaving the network without authorization.
5. **DDoS Defense:** Helps absorb and filter out malicious traffic spikes during Distributed Denial of Service attacks.
6. **Compliance Requirements:** Mandatory for regulatory frameworks (e.g., PCI-DSS, HIPAA, GDPR, ISO 27001) to protect sensitive client and financial data.

---

## 5. Summary Cheat Sheet

| Feature / Type | Primary Focus | Best Used For |
| :--- | :--- | :--- |
| **Packet-Filtering** | Source/Dest IP & Ports | Basic perimeter control |
| **Stateful Inspection** | Connection tracking & state | Standard network filtering |
| **Proxy Firewall** | Application payload inspection | High-security web environments |
| **NGFW** | DPI, IPS, Threat Intelligence | Enterprise modern defense |