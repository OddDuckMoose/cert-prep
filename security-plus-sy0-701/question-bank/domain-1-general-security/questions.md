# Domain 1 — General Security Concepts (12%)

### Q1. Security Control Categories

A company installs security cameras at all building entrances to record who enters and exits. Which type of security control does this BEST represent?

- A) Preventive
- B) Detective
- C) Corrective
- D) Deterrent

<details>
<summary>Answer</summary>

**B) Detective**

Security cameras that record activity are detective controls — they identify and document security events. If the cameras were fake/visible to discourage entry, they'd be deterrent. If they triggered automatic door locks, that would be corrective.
</details>

---

### Q2. CIA Triad — Integrity

A hospital implements digital signatures on all electronic prescriptions to ensure they haven't been altered after the prescribing physician signs them. Which element of the CIA triad does this PRIMARILY protect?

- A) Confidentiality
- B) Integrity
- C) Availability
- D) Non-repudiation

<details>
<summary>Answer</summary>

**B) Integrity**

Digital signatures verify that data has not been modified since it was signed, directly protecting integrity. While digital signatures also support non-repudiation, the primary purpose described here — ensuring prescriptions haven't been altered — is an integrity control.
</details>

---

### Q3. Zero Trust Architecture

An organization is implementing a zero trust architecture. Which principle is MOST fundamental to this approach?

- A) All internal network traffic is inherently trusted
- B) Never trust, always verify — regardless of network location
- C) Perimeter firewalls are the primary security control
- D) VPN connections from remote users are always trusted

<details>
<summary>Answer</summary>

**B) Never trust, always verify — regardless of network location**

Zero trust assumes no implicit trust based on network location. Every access request must be authenticated, authorized, and continuously validated regardless of whether the user is inside or outside the corporate network.
</details>

---

### Q4. AAA Framework

A network administrator configures a RADIUS server to handle user login requests for VPN access. After a user authenticates, the server determines what resources the user can access and logs all session activity. Which AAA components are described?

- A) Authentication, Authorization, and Accounting
- B) Authentication, Auditing, and Access Control
- C) Authorization, Accounting, and Administration
- D) Authentication, Administration, and Auditing

<details>
<summary>Answer</summary>

**A) Authentication, Authorization, and Accounting**

The three AAA components are: Authentication (verifying identity via login), Authorization (determining what resources the user can access), and Accounting (logging session activity for auditing).
</details>

---

### Q5. Gap Analysis

A security team compares their current security posture against CIS benchmarks and identifies areas where their configurations fall short. What is this process called?

- A) Vulnerability scan
- B) Penetration test
- C) Gap analysis
- D) Risk assessment

<details>
<summary>Answer</summary>

**C) Gap analysis**

A gap analysis compares the current state against a desired state (framework, benchmark, or standard) to identify deficiencies. A vulnerability scan identifies technical flaws. A penetration test actively exploits weaknesses. A risk assessment evaluates threats and their impact.
</details>

---

### Q6. Change Management

Before deploying a firewall rule change to production, a security engineer must submit a formal request documenting the change, its impact, a rollback plan, and obtain approval from the change advisory board. Which security process does this describe?

- A) Incident response
- B) Change management
- C) Configuration management
- D) Patch management

<details>
<summary>Answer</summary>

**B) Change management**

Change management is a formal process requiring documentation, impact assessment, rollback plans, and approval before implementing changes to production systems. This prevents unauthorized or poorly planned changes from introducing security risks.
</details>

---

### Q7. Cryptographic Concepts — Symmetric vs. Asymmetric

Which statement BEST describes the difference between symmetric and asymmetric encryption?

- A) Symmetric encryption uses two keys; asymmetric uses one key
- B) Symmetric encryption is slower; asymmetric encryption is faster
- C) Symmetric encryption uses a single shared key; asymmetric encryption uses a public/private key pair
- D) Symmetric encryption is only used for hashing; asymmetric is used for encryption

<details>
<summary>Answer</summary>

**C) Symmetric encryption uses a single shared key; asymmetric encryption uses a public/private key pair**

Symmetric encryption (AES, 3DES) uses one shared secret key for both encryption and decryption. Asymmetric encryption (RSA, ECC) uses a key pair — a public key for encryption and a private key for decryption. Symmetric is faster; asymmetric solves the key distribution problem.
</details>

---

### Q8. Hashing

A security analyst needs to verify that a forensic disk image has not been altered since it was created. Which cryptographic function should they use?

- A) AES-256 encryption
- B) RSA digital signature
- C) SHA-256 hash comparison
- D) Diffie-Hellman key exchange

<details>
<summary>Answer</summary>

**C) SHA-256 hash comparison**

Hashing produces a fixed-length digest of data. Comparing the hash of the original image to the hash of the current copy verifies integrity — any change produces a completely different hash. This is standard practice in digital forensics.
</details>

---

### Q9. PKI and Certificates

A user receives a browser warning that a website's certificate has been revoked. Which PKI component is responsible for publishing this revocation information?

- A) Registration Authority (RA)
- B) Certificate Authority (CA)
- C) Certificate Revocation List (CRL)
- D) Online Certificate Status Protocol (OCSP)

<details>
<summary>Answer</summary>

**C) Certificate Revocation List (CRL)**

A CRL is a list published by the CA containing serial numbers of revoked certificates. OCSP is an alternative real-time protocol for checking certificate status. The CA manages revocation, but the CRL is the component that publishes the revocation information.
</details>

---

### Q10. Security Control Types

An organization requires all employees to complete annual security awareness training. This is an example of which control type?

- A) Technical control
- B) Operational control
- C) Managerial control
- D) Physical control

<details>
<summary>Answer</summary>

**B) Operational control**

Security awareness training is an operational (administrative) control — it's a procedure or process implemented by people. Technical controls are implemented by technology (firewalls, encryption). Managerial controls include policies and risk assessments. Physical controls restrict physical access.
</details>

---

### Q11. Non-Repudiation

A contract is signed using a digital signature with the signer's private key. The signer later claims they never signed the document. Which security concept prevents the signer from denying their action?

- A) Confidentiality
- B) Integrity
- C) Authentication
- D) Non-repudiation

<details>
<summary>Answer</summary>

**D) Non-repudiation**

Non-repudiation ensures a party cannot deny having performed an action. Digital signatures provide non-repudiation because only the holder of the private key could have created the signature, providing proof of origin.
</details>

---

### Q12. Defense in Depth

An organization implements firewalls, IDS, endpoint protection, MFA, security awareness training, and physical access controls. Which security strategy does this layered approach represent?

- A) Least privilege
- B) Defense in depth
- C) Single point of failure elimination
- D) Separation of duties

<details>
<summary>Answer</summary>

**B) Defense in depth**

Defense in depth uses multiple layers of security controls so that if one layer fails, others continue to provide protection. This approach combines technical, operational, and physical controls across multiple tiers.
</details>

---

### Q13. Key Stretching

A security engineer implements bcrypt for password storage instead of plain SHA-256 hashing. What is the PRIMARY advantage of this approach?

- A) bcrypt produces shorter hashes that save storage space
- B) bcrypt adds computational cost through key stretching, making brute-force attacks significantly slower
- C) bcrypt encrypts passwords so they can be decrypted when needed
- D) bcrypt eliminates the need for salting passwords

<details>
<summary>Answer</summary>

**B) bcrypt adds computational cost through key stretching, making brute-force attacks significantly slower**

Key stretching algorithms like bcrypt, scrypt, and PBKDF2 intentionally slow down the hashing process, making brute-force and dictionary attacks computationally expensive. bcrypt also includes built-in salting.
</details>

---

### Q14. Technical vs. Managerial Controls

A CISO develops an Acceptable Use Policy (AUP) that defines how employees may use company IT resources. This policy is an example of which type of control?

- A) Technical
- B) Operational
- C) Managerial
- D) Compensating

<details>
<summary>Answer</summary>

**C) Managerial**

Policies, procedures, standards, and guidelines are managerial (administrative) controls. They establish governance and define expectations. An AUP is a policy document — a managerial control. The enforcement of the AUP (through DLP tools, for example) would be a technical control.
</details>

