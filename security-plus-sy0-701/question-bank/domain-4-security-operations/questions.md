# Domain 4 — Security Operations (28%)

### Q1. Vulnerability Scanning

A security team runs a weekly automated tool that identifies missing patches, open ports, default credentials, and known CVEs on all networked devices. Which security activity does this describe?

- A) Penetration testing
- B) Vulnerability scanning
- C) Threat hunting
- D) Log analysis

<details>
<summary>Answer</summary>

**B) Vulnerability scanning**

Vulnerability scanning uses automated tools (Nessus, Qualys, OpenVAS) to identify known vulnerabilities, misconfigurations, and missing patches. Unlike penetration testing, vulnerability scanning identifies weaknesses without actively exploiting them.
</details>

---

### Q2. SIEM

A SOC analyst reviews a platform that collects logs from firewalls, servers, and endpoints, correlates events in real time, and generates alerts when suspicious patterns are detected. Which technology is this?

- A) SOAR
- B) SIEM
- C) DLP
- D) EDR

<details>
<summary>Answer</summary>

**B) SIEM (Security Information and Event Management)**

A SIEM aggregates logs from multiple sources, correlates events, provides real-time alerting, and enables investigation through dashboards and search. Examples: Splunk, Microsoft Sentinel, Wazuh.
</details>

---

### Q3. Incident Response — Containment

During an active ransomware incident, a security analyst immediately disconnects the infected workstation from the network. Which incident response phase does this action represent?

- A) Preparation
- B) Detection and Analysis
- C) Containment
- D) Eradication

<details>
<summary>Answer</summary>

**C) Containment**

Containment limits the scope and impact of an incident. Disconnecting an infected system prevents the malware from spreading to other systems. This is a short-term containment action taken during an active incident.
</details>

---

### Q4. Chain of Custody

During a forensic investigation, an analyst documents every person who handled a seized hard drive, including dates, times, and purposes. Which forensic concept does this maintain?

- A) Order of volatility
- B) Chain of custody
- C) Legal hold
- D) Data preservation

<details>
<summary>Answer</summary>

**B) Chain of custody**

Chain of custody documents the chronological handling of evidence — who collected it, who stored it, who accessed it, and when. This ensures evidence integrity and admissibility in legal proceedings.
</details>

---

### Q5. EDR

An endpoint security tool continuously monitors process execution, file changes, network connections, and registry modifications on workstations, providing automated threat detection and response capabilities. Which technology is this?

- A) Antivirus
- B) Host-based IDS (HIDS)
- C) Endpoint Detection and Response (EDR)
- D) Data Loss Prevention (DLP)

<details>
<summary>Answer</summary>

**C) Endpoint Detection and Response (EDR)**

EDR goes beyond traditional antivirus by continuously monitoring endpoint activity, detecting suspicious behavior, providing investigation capabilities, and enabling automated response actions like isolating endpoints.
</details>

---

### Q6. MFA — Something You Know, Have, Are

An organization implements a login system requiring a password (something you know) and a push notification to a mobile app (something you have). Which authentication concept does this implement?

- A) Single sign-on (SSO)
- B) Multi-factor authentication (MFA)
- C) Federation
- D) RBAC

<details>
<summary>Answer</summary>

**B) Multi-factor authentication (MFA)**

MFA requires two or more different authentication factors: something you know (password), something you have (phone/token), or something you are (biometric). Using two factors from the same category (two passwords) is NOT MFA.
</details>

---

### Q7. Log Analysis — Failed Login Attempts

A security analyst reviewing authentication logs notices 500 failed login attempts against a single account from various IP addresses over 30 minutes. Which attack does this indicate?

- A) Credential stuffing
- B) Brute-force attack
- C) Password spraying
- D) Phishing

<details>
<summary>Answer</summary>

**B) Brute-force attack**

500 failed attempts against a single account indicates a brute-force attack — systematically trying passwords against one target. Credential stuffing uses known credentials from breaches. Password spraying tries a few passwords against many accounts.
</details>

---

### Q8. Data Loss Prevention (DLP)

An organization needs to prevent employees from emailing files containing credit card numbers or Social Security numbers to external recipients. Which technology should be implemented?

- A) IDS/IPS
- B) Firewall
- C) Data Loss Prevention (DLP)
- D) SIEM

<details>
<summary>Answer</summary>

**C) Data Loss Prevention (DLP)**

DLP systems detect and prevent unauthorized transmission of sensitive data based on content inspection. They can identify patterns like credit card numbers, SSNs, and other PII in emails, file transfers, and web uploads.
</details>

---

### Q9. Incident Response — Eradication

After containing a malware incident, the security team removes the malware, patches the exploited vulnerability, and resets compromised credentials. Which incident response phase is this?

- A) Containment
- B) Eradication
- C) Recovery
- D) Lessons learned

<details>
<summary>Answer</summary>

**B) Eradication**

Eradication removes the threat from the environment — deleting malware, patching vulnerabilities, and eliminating the attacker's access. This follows containment and precedes recovery (restoring systems to normal operations).
</details>

---

### Q10. File Integrity Monitoring

A security tool alerts when critical system files (like /etc/passwd or Windows registry keys) are modified unexpectedly. Which security control does this describe?

- A) Antivirus
- B) File integrity monitoring (FIM)
- C) DLP
- D) Vulnerability scanner

<details>
<summary>Answer</summary>

**B) File integrity monitoring (FIM)**

FIM monitors critical files and directories for unauthorized changes by comparing current file hashes against known-good baselines. Changes trigger alerts for investigation. Examples: OSSEC, Tripwire, Wazuh FIM.
</details>

---

### Q11. Disk Imaging — Forensics

Before analyzing a seized computer, a forensic examiner creates a bit-for-bit copy of the hard drive and then works exclusively from the copy. Why is this procedure critical?

- A) To speed up the analysis process
- B) To preserve the original evidence in its unaltered state
- C) To encrypt the evidence for secure storage
- D) To convert the data into a searchable format

<details>
<summary>Answer</summary>

**B) To preserve the original evidence in its unaltered state**

Forensic imaging creates an exact bit-for-bit copy (including deleted data and slack space). Working from the copy preserves the original evidence, maintaining its integrity for potential legal proceedings. The original is stored securely.
</details>

---

### Q12. IDS vs. IPS

A network security device monitors traffic and generates alerts when it detects suspicious activity but does NOT block the traffic. Which device type is this?

- A) IPS (Intrusion Prevention System)
- B) IDS (Intrusion Detection System)
- C) Firewall
- D) WAF

<details>
<summary>Answer</summary>

**B) IDS (Intrusion Detection System)**

An IDS monitors and alerts on suspicious activity but does not take action to block it (passive). An IPS can detect AND block malicious traffic (active/inline). The key difference is whether the device takes automated blocking action.
</details>

---

### Q13. Access Control — RBAC

A company assigns permissions based on job functions: all members of the "Finance" group can access financial systems, and all members of the "HR" group can access HR systems. Which access control model is this?

- A) Discretionary Access Control (DAC)
- B) Mandatory Access Control (MAC)
- C) Role-Based Access Control (RBAC)
- D) Attribute-Based Access Control (ABAC)

<details>
<summary>Answer</summary>

**C) Role-Based Access Control (RBAC)**

RBAC assigns permissions to roles (groups/job functions) rather than individual users. Users inherit permissions by being assigned to roles. This simplifies access management in organizations.
</details>

---

### Q14. Playbook / Runbook

A SOC has documented step-by-step procedures for responding to specific incident types: phishing, ransomware, DDoS, and insider threat. What are these documented procedures called?

- A) Policies
- B) Playbooks/Runbooks
- C) Baselines
- D) Service level agreements

<details>
<summary>Answer</summary>

**B) Playbooks/Runbooks**

Playbooks (runbooks) are documented, step-by-step procedures for handling specific security incidents. They ensure consistent, repeatable response actions and reduce decision-making time during high-pressure incidents.
</details>

---

### Q15. Order of Volatility

During a forensic investigation of a running system, which data should be collected FIRST?

- A) Hard drive contents
- B) CPU registers and cache
- C) Network connection logs from SIEM
- D) Backup tapes

<details>
<summary>Answer</summary>

**B) CPU registers and cache**

The order of volatility dictates collecting the most volatile (shortest-lived) data first: CPU registers/cache → RAM → swap/temp files → hard drive → remote logs → backups. CPU registers are lost the moment the system state changes.
</details>

---

### Q16. Group Policy

A Windows administrator needs to enforce a minimum password length of 12 characters and require screen lock after 5 minutes of inactivity across all domain-joined workstations. Which tool should they use?

- A) Local security policy on each machine
- B) Group Policy Objects (GPOs)
- C) Registry editor on each machine
- D) PowerShell scripts scheduled via Task Scheduler

<details>
<summary>Answer</summary>

**B) Group Policy Objects (GPOs)**

GPOs in Active Directory enable centralized configuration management across all domain-joined machines. Password policies, lockout policies, and other security settings can be deployed once and enforced across the entire domain.
</details>

---

### Q17. SOAR

A security tool automatically enriches alerts with threat intelligence, triggers predefined response actions (like blocking an IP), and orchestrates workflows across multiple security tools without human intervention. Which technology is this?

- A) SIEM
- B) SOAR
- C) EDR
- D) XDR

<details>
<summary>Answer</summary>

**B) SOAR (Security Orchestration, Automation, and Response)**

SOAR platforms automate and orchestrate security workflows across multiple tools. They execute playbooks automatically — enriching alerts, taking response actions, and coordinating between SIEM, firewalls, EDR, and other security tools.
</details>

---

### Q18. Mobile Device Management (MDM)

A company issues smartphones to employees and needs the ability to enforce encryption, remotely wipe devices if lost, and restrict which applications can be installed. Which solution provides these capabilities?

- A) DLP
- B) Mobile Device Management (MDM)
- C) NAC
- D) VPN

<details>
<summary>Answer</summary>

**B) Mobile Device Management (MDM)**

MDM solutions manage and secure mobile devices: enforcing encryption, enabling remote wipe, restricting app installation, configuring VPN, and enforcing security policies on corporate and BYOD devices.
</details>

---

### Q19. Network Access Control (NAC)

A hospital's network requires that all devices must have updated antivirus and current OS patches before being allowed to connect to the network. Devices that don't meet these requirements are placed in a remediation VLAN. Which technology enforces this?

- A) Firewall
- B) Network Access Control (NAC)
- C) IDS/IPS
- D) Proxy server

<details>
<summary>Answer</summary>

**B) Network Access Control (NAC)**

NAC checks endpoint health (AV status, patch level, configuration) before granting network access. Non-compliant devices are quarantined in a remediation VLAN until they meet the security baseline.
</details>

---

### Q20. Privilege Access Management (PAM)

An organization requires that all administrator accounts check out credentials from a vault, with sessions recorded and passwords automatically rotated after each use. Which solution provides this?

- A) SSO
- B) Privileged Access Management (PAM)
- C) RBAC
- D) Directory services

<details>
<summary>Answer</summary>

**B) Privileged Access Management (PAM)**

PAM solutions manage privileged credentials through vaulting (secure storage), session recording (audit trail), just-in-time access (temporary elevation), and automatic password rotation. Examples: CyberArk, BeyondTrust.
</details>

---

### Q21. Wireless Security — WPA3

Which wireless security protocol provides the STRONGEST encryption and is recommended for enterprise wireless networks deployed today?

- A) WEP
- B) WPA
- C) WPA2
- D) WPA3

<details>
<summary>Answer</summary>

**D) WPA3**

WPA3 is the latest wireless security standard, providing stronger encryption (SAE handshake replacing PSK), protection against offline dictionary attacks, and forward secrecy. WEP and WPA are deprecated. WPA2 is still acceptable but WPA3 is preferred.
</details>

---

### Q22. Certificate-Based Authentication

An organization requires that only devices with a specific digital certificate installed can connect to the corporate Wi-Fi network. Which authentication method is this?

- A) PSK (Pre-Shared Key)
- B) Certificate-based authentication (EAP-TLS)
- C) RADIUS with username/password
- D) MAC address filtering

<details>
<summary>Answer</summary>

**B) Certificate-based authentication (EAP-TLS)**

EAP-TLS uses digital certificates on both the client and server for mutual authentication. It's the most secure wireless authentication method, as certificates are much harder to steal or share than passwords.
</details>

---

### Q23. Tabletop Exercise

A company brings together key stakeholders to walk through a simulated cybersecurity incident scenario in a conference room, discussing roles, decisions, and communication procedures without touching any real systems. What type of exercise is this?

- A) Penetration test
- B) Red team exercise
- C) Tabletop exercise
- D) Vulnerability assessment

<details>
<summary>Answer</summary>

**C) Tabletop exercise**

A tabletop exercise is a discussion-based drill where participants walk through an incident scenario, discussing their roles and decisions. No real systems are affected. It tests the incident response plan's completeness and team coordination.
</details>

---

### Q24. Secure Email — S/MIME

An organization needs to encrypt email messages end-to-end and digitally sign them to verify the sender's identity. Which email security standard should they implement?

- A) SPF
- B) DKIM
- C) DMARC
- D) S/MIME

<details>
<summary>Answer</summary>

**D) S/MIME**

S/MIME (Secure/Multipurpose Internet Mail Extensions) provides end-to-end email encryption and digital signatures using PKI certificates. SPF, DKIM, and DMARC are email authentication protocols that verify sender domains but don't encrypt message content.
</details>

---

### Q25. Hardening — Disable Unnecessary Services

During a security audit, an administrator discovers that an FTP server, Telnet, and SNMP v1 are running on a production web server that only needs to serve HTTPS traffic. What is the MOST appropriate action?

- A) Monitor the services for suspicious activity
- B) Disable the unnecessary services and close their ports
- C) Install antivirus on the server
- D) Place the server behind a WAF

<details>
<summary>Answer</summary>

**B) Disable the unnecessary services and close their ports**

Disabling unnecessary services reduces the attack surface. FTP, Telnet, and SNMPv1 are insecure protocols that should not run on a production web server. Only HTTPS (port 443) should be enabled for its intended function.
</details>

---

### Q26. Account Lockout Policy

An organization configures its domain to lock user accounts for 30 minutes after 5 consecutive failed login attempts. Which security control does this implement?

- A) Rate limiting
- B) Account lockout policy
- C) Password complexity
- D) Session timeout

<details>
<summary>Answer</summary>

**B) Account lockout policy**

Account lockout policies lock accounts after a defined number of failed attempts, defending against brute-force attacks. The lockout duration and threshold should balance security against the risk of denial-of-service (locking out legitimate users).
</details>

---

### Q27. Firewall Rule — Implicit Deny

A firewall has three explicit rules allowing specific traffic. A packet arrives that doesn't match any of the three rules. If the firewall follows best practices, what happens to the packet?

- A) The packet is allowed through
- B) The packet is logged but allowed
- C) The packet is dropped (implicit deny)
- D) The packet is forwarded to the IDS for analysis

<details>
<summary>Answer</summary>

**C) The packet is dropped (implicit deny)**

Implicit deny (deny all) is a firewall best practice where any traffic not explicitly permitted by a rule is automatically denied. This follows the principle of least privilege — only specifically authorized traffic is allowed.
</details>

---

### Q28. Data Sanitization

Before donating old hard drives, an organization needs to ensure no data can be recovered — even with advanced forensic tools. Which sanitization method provides the STRONGEST assurance?

- A) Quick format
- B) Degaussing
- C) Physical destruction (shredding)
- D) Deleting all files and emptying the recycle bin

<details>
<summary>Answer</summary>

**C) Physical destruction (shredding)**

Physical destruction (shredding, incineration, pulverizing) is the most secure sanitization method — it eliminates any possibility of data recovery. Degaussing works for magnetic media but not SSDs. Quick format and file deletion leave data recoverable.
</details>

---

### Q29. SCAP

An organization needs to automate vulnerability assessment and compliance checking against CIS benchmarks across thousands of endpoints. Which framework standardizes this process?

- A) NIST CSF
- B) SCAP (Security Content Automation Protocol)
- C) OWASP
- D) ISO 27001

<details>
<summary>Answer</summary>

**B) SCAP (Security Content Automation Protocol)**

SCAP is a suite of specifications for automating vulnerability management, security measurement, and compliance checking. It uses standardized formats (CVE, CVSS, CPE, CCE) to enable automated security assessment at scale.
</details>

---

### Q30. Port Security

A network administrator configures a switch to allow only one MAC address per port and shut down the port if a different MAC address is detected. Which feature is being used?

- A) VLAN tagging
- B) Port security
- C) 802.1X
- D) NAC

<details>
<summary>Answer</summary>

**B) Port security**

Port security limits the number of MAC addresses allowed on a switch port and defines actions (shutdown, restrict, protect) when violations occur. This prevents unauthorized devices from connecting and mitigates MAC flooding attacks.
</details>

---

### Q31. Geofencing

A company configures its MDM solution to disable the camera application on employee phones when they are within the building's GPS boundaries. Which technology enables this location-based restriction?

- A) Remote wipe
- B) Geofencing
- C) Containerization
- D) Application whitelisting

<details>
<summary>Answer</summary>

**B) Geofencing**

Geofencing creates a virtual geographic boundary that triggers actions when a device enters or exits the defined area. Combined with MDM, it can enforce location-specific policies like disabling cameras in sensitive areas.
</details>

---

### Q32. Secure DNS — DNSSEC

An organization wants to ensure that DNS responses received by their clients have not been tampered with in transit. Which DNS security extension should they implement?

- A) DNS over HTTPS (DoH)
- B) DNSSEC
- C) DNS sinkhole
- D) DNS filtering

<details>
<summary>Answer</summary>

**B) DNSSEC**

DNSSEC adds digital signatures to DNS records, allowing clients to verify that responses are authentic and have not been modified (integrity). DNS over HTTPS (DoH) encrypts DNS queries for privacy but doesn't verify response integrity the same way.
</details>

---

### Q33. Incident Response — Lessons Learned

After resolving a security incident, the team holds a meeting to discuss what happened, what went well, what could be improved, and documents recommendations for preventing similar incidents. Which IR phase is this?

- A) Recovery
- B) Preparation
- C) Lessons learned (post-incident activity)
- D) Containment

<details>
<summary>Answer</summary>

**C) Lessons learned (post-incident activity)**

Lessons learned (post-incident review) documents findings, identifies improvements, and updates procedures and controls to prevent recurrence. This phase closes the incident response cycle and feeds back into the preparation phase.
</details>

---

### Q34. Least Privilege

A new database administrator is given only the specific permissions needed to manage databases and nothing more — no access to network devices, email servers, or other systems outside their role. Which security principle does this follow?

- A) Separation of duties
- B) Least privilege
- C) Need to know
- D) Job rotation

<details>
<summary>Answer</summary>

**B) Least privilege**

Least privilege grants users only the minimum permissions necessary to perform their job functions. This limits the blast radius if an account is compromised and reduces the risk of accidental or intentional misuse.
</details>

