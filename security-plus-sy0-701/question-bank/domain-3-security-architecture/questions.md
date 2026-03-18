# Domain 3 — Security Architecture (18%)

### Q1. Network Segmentation — DMZ

A company needs to host a public-facing web server while protecting internal resources. Which network architecture places the web server in a zone accessible from the internet but isolated from the internal network?

- A) VLAN
- B) DMZ (demilitarized zone)
- C) VPN
- D) Air gap

<details>
<summary>Answer</summary>

**B) DMZ (demilitarized zone)**

A DMZ is a network segment between the external (internet) and internal networks. Public-facing servers are placed here so external users can access them without direct access to internal resources. Typically implemented with dual firewalls or a multi-homed firewall.
</details>

---

### Q2. Cloud Service Models

An organization moves its email to a provider where the vendor manages everything — servers, storage, networking, application, and updates. The organization only manages user accounts and data. Which cloud service model is this?

- A) Infrastructure as a Service (IaaS)
- B) Platform as a Service (PaaS)
- C) Software as a Service (SaaS)
- D) Function as a Service (FaaS)

<details>
<summary>Answer</summary>

**C) Software as a Service (SaaS)**

SaaS delivers fully managed applications over the internet. The customer manages only user access and data. Examples: Microsoft 365, Salesforce, Gmail. IaaS provides infrastructure (VMs, storage). PaaS provides a platform for developing applications.
</details>

---

### Q3. Load Balancer

A web application experiences high traffic. To distribute incoming requests across multiple web servers and ensure no single server is overwhelmed, which device should be deployed?

- A) Reverse proxy
- B) Load balancer
- C) Web application firewall (WAF)
- D) Content delivery network (CDN)

<details>
<summary>Answer</summary>

**B) Load balancer**

A load balancer distributes incoming traffic across multiple servers to ensure availability, reliability, and performance. It can also provide health checking to route traffic away from failed servers.
</details>

---

### Q4. VPN — Site-to-Site

Two branch offices need to securely communicate over the public internet as if they were on the same local network. Which solution BEST addresses this requirement?

- A) Remote access VPN
- B) Site-to-site VPN
- C) Split tunnel VPN
- D) SSL/TLS proxy

<details>
<summary>Answer</summary>

**B) Site-to-site VPN**

A site-to-site VPN creates an encrypted tunnel between two networks (typically using IPSec), allowing all devices on both networks to communicate securely. Remote access VPN connects individual users to a network.
</details>

---

### Q5. RAID — Availability

A database administrator needs to ensure that a disk failure does not cause data loss or downtime. Which RAID level provides both disk mirroring and performance through striping?

- A) RAID 0
- B) RAID 1
- C) RAID 5
- D) RAID 10

<details>
<summary>Answer</summary>

**D) RAID 10**

RAID 10 (1+0) combines mirroring (RAID 1) and striping (RAID 0), providing both redundancy and performance. RAID 0 provides striping only (no redundancy). RAID 1 provides mirroring only. RAID 5 uses striping with parity.
</details>

---

### Q6. Infrastructure as Code (IaC)

A DevOps team defines their entire server infrastructure in configuration files stored in a Git repository. Changes to infrastructure are made by modifying these files and running automated deployment tools. Which concept does this represent?

- A) Configuration management
- B) Infrastructure as Code (IaC)
- C) Continuous integration
- D) Containerization

<details>
<summary>Answer</summary>

**B) Infrastructure as Code (IaC)**

IaC manages infrastructure through machine-readable configuration files rather than manual processes. Tools like Terraform and Ansible enable version-controlled, repeatable, and auditable infrastructure deployments.
</details>

---

### Q7. Microservices Architecture

Instead of deploying a monolithic application, a development team breaks the application into small, independently deployable services that communicate via APIs. Which architectural approach is this?

- A) Serverless
- B) Microservices
- C) Containerization
- D) Service-oriented architecture (SOA)

<details>
<summary>Answer</summary>

**B) Microservices**

Microservices architecture decomposes an application into small, independent services. Each service handles a specific function and communicates via APIs. This improves scalability, fault isolation, and deployment flexibility.
</details>

---

### Q8. Firewall — Stateful vs. Stateless

Which type of firewall tracks the state of active network connections and makes filtering decisions based on the context of the traffic flow, not just individual packets?

- A) Stateless packet filter
- B) Stateful inspection firewall
- C) Web application firewall (WAF)
- D) Proxy firewall

<details>
<summary>Answer</summary>

**B) Stateful inspection firewall**

A stateful inspection firewall maintains a state table tracking active connections. It can make decisions based on the connection state (new, established, related), providing more intelligent filtering than stateless packet filters which examine each packet independently.
</details>

---

### Q9. Containerization — Security Benefit

A security architect recommends deploying applications in containers rather than directly on host operating systems. Which security benefit does containerization provide?

- A) Containers are immune to all malware
- B) Containers provide application isolation and reduce the attack surface by packaging only necessary dependencies
- C) Containers eliminate the need for patching
- D) Containers encrypt all data at rest by default

<details>
<summary>Answer</summary>

**B) Containers provide application isolation and reduce the attack surface by packaging only necessary dependencies**

Containers isolate applications and their dependencies, reducing the attack surface compared to full OS installations. They don't eliminate malware risk or patching needs, but they limit blast radius and enforce consistency.
</details>

---

### Q10. High Availability

An organization requires that their critical application remain operational even if an entire data center goes offline. Which approach BEST ensures this level of availability?

- A) RAID 5 across all servers
- B) Active-active cluster across geographically separated data centers
- C) Daily full backups stored offsite
- D) UPS with generator backup at the primary site

<details>
<summary>Answer</summary>

**B) Active-active cluster across geographically separated data centers**

An active-active cluster across geographically separated sites ensures that if one entire data center fails, the other continues serving traffic. RAID and UPS address component failures at a single site. Backups enable recovery but don't maintain uptime.
</details>

---

### Q11. Proxy Server

A company routes all employee web traffic through a device that inspects HTTP/HTTPS requests, enforces URL filtering policies, caches content, and logs all web activity. Which device is this?

- A) IDS
- B) Forward proxy
- C) Reverse proxy
- D) Load balancer

<details>
<summary>Answer</summary>

**B) Forward proxy**

A forward proxy sits between internal clients and the internet, inspecting outbound web requests. It can enforce URL filtering, cache content, and log activity. A reverse proxy sits in front of servers to protect them from external clients.
</details>

---

### Q12. Embedded Systems Security

A manufacturing plant uses programmable logic controllers (PLCs) that run outdated firmware and cannot be easily patched. Which mitigation strategy is MOST appropriate for securing these embedded systems?

- A) Install endpoint protection software on each PLC
- B) Isolate the OT network from the IT network using network segmentation
- C) Replace all PLCs with modern cloud-based controllers
- D) Apply automatic Windows updates to the PLCs

<details>
<summary>Answer</summary>

**B) Isolate the OT network from the IT network using network segmentation**

Embedded systems and OT/ICS devices often cannot be patched or run security software. The primary mitigation is network segmentation — isolating them from IT networks and the internet to limit attack exposure.
</details>

---

### Q13. Serverless Computing

A developer deploys application code that executes only when triggered by an event (like an API call) and automatically scales. The developer does not manage any servers or infrastructure. Which cloud computing model is this?

- A) IaaS
- B) PaaS
- C) SaaS
- D) Serverless / Function as a Service (FaaS)

<details>
<summary>Answer</summary>

**D) Serverless / Function as a Service (FaaS)**

Serverless computing (FaaS) executes code in response to events without the developer managing any infrastructure. The cloud provider handles all server management, scaling, and availability. Examples: AWS Lambda, Azure Functions.
</details>

---

### Q14. SD-WAN

A company with 50 branch offices wants to securely connect all locations using commodity internet connections rather than expensive MPLS circuits, with centralized policy management and encrypted tunnels. Which technology BEST fits this requirement?

- A) MPLS
- B) SD-WAN
- C) Site-to-site VPN
- D) VXLAN

<details>
<summary>Answer</summary>

**B) SD-WAN**

SD-WAN (Software-Defined Wide Area Network) uses software to manage WAN connections, enabling secure connectivity over commodity internet links with centralized policy management, traffic optimization, and encrypted tunnels between sites.
</details>

---

### Q15. Data Sovereignty

A European company must ensure that all customer data is stored and processed within the EU to comply with GDPR. Which cloud architecture consideration does this represent?

- A) Data classification
- B) Data sovereignty
- C) Data masking
- D) Data retention

<details>
<summary>Answer</summary>

**B) Data sovereignty**

Data sovereignty requires that data is subject to the laws of the country where it is stored or processed. GDPR imposes restrictions on transferring personal data outside the EU, making data sovereignty a critical cloud architecture consideration.
</details>

---

### Q16. Honeypot

A security team deploys a server that mimics a vulnerable web application with fake data. The server has no legitimate business purpose but is monitored to detect and study attacker behavior. What is this?

- A) Bastion host
- B) Jump server
- C) Honeypot
- D) Proxy server

<details>
<summary>Answer</summary>

**C) Honeypot**

A honeypot is a decoy system designed to attract attackers. It has no legitimate production purpose but is monitored to detect intrusions, study attack techniques, and divert attackers from real systems. A honeynet is a network of honeypots.
</details>

---

### Q17. Encryption at Rest

A company stores sensitive customer data in a cloud database. To protect the data if the storage media is physically stolen or improperly decommissioned, which control should be implemented?

- A) TLS encryption
- B) Encryption at rest (AES-256)
- C) IPSec VPN
- D) Data masking

<details>
<summary>Answer</summary>

**B) Encryption at rest (AES-256)**

Encryption at rest protects stored data by encrypting it on disk. If physical media is stolen, the data is unreadable without the encryption key. TLS and IPSec protect data in transit. Data masking obscures data for non-production use.
</details>

---

### Q18. Physical Security — Bollards

A government building installs reinforced concrete posts around its perimeter to prevent vehicles from driving into the building. What are these called?

- A) Mantrap
- B) Bollards
- C) Turnstile
- D) Fencing

<details>
<summary>Answer</summary>

**B) Bollards**

Bollards are short, sturdy posts installed to prevent vehicle-borne attacks. They protect building perimeters and pedestrian areas from unauthorized vehicle access — a physical security control against ramming attacks.
</details>

---

### Q19. Backup Types

An organization performs a full backup every Sunday. On weekdays, they back up only the data that has changed since the last full backup. Which backup type describes the weekday backups?

- A) Incremental
- B) Differential
- C) Snapshot
- D) Full

<details>
<summary>Answer</summary>

**B) Differential**

A differential backup copies all data that has changed since the last full backup. It grows larger each day but requires only the full + latest differential to restore. An incremental backup copies only changes since the last backup of any type — smaller but requires the full + all incrementals to restore.
</details>

---

### Q20. Jump Server / Bastion Host

Administrators must access servers in a secured network segment, but direct connections from the corporate network are prohibited. They are required to first connect to an intermediary hardened server, then access the target systems from there. What is this intermediary server called?

- A) Proxy server
- B) Jump server (bastion host)
- C) Honeypot
- D) SIEM

<details>
<summary>Answer</summary>

**B) Jump server (bastion host)**

A jump server (bastion host) is a hardened intermediary system used to access systems in a different security zone. All administrative access passes through the jump server, providing a single auditable access point.
</details>

---

### Q21. Secure Protocol — HTTPS

A web developer is configuring a public-facing website. To encrypt all traffic between the browser and the web server, which protocol should be implemented?

- A) HTTP
- B) HTTPS (HTTP over TLS)
- C) FTP
- D) Telnet

<details>
<summary>Answer</summary>

**B) HTTPS (HTTP over TLS)**

HTTPS encrypts HTTP traffic using TLS, protecting data in transit between the browser and server. HTTP transmits data in plaintext. FTP and Telnet are also insecure plaintext protocols.
</details>

---

### Q22. Deception Technology — Honeytoken

A database administrator places fake records (e.g., a fictitious high-value customer account) in a production database. An alert fires if anyone accesses or queries this specific record. What is this technique called?

- A) Honeynet
- B) Honeypot
- C) Honeytoken
- D) Canary deployment

<details>
<summary>Answer</summary>

**C) Honeytoken**

A honeytoken is a fake piece of data (fake account, file, credential, or record) planted in a system to detect unauthorized access. Any access to the honeytoken triggers an alert, indicating potential compromise or insider threat.
</details>

