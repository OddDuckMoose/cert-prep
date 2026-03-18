# Domain 5 — Security Program Management and Oversight (20%)

### Q1. Risk Assessment — Qualitative

A risk committee categorizes risks as High, Medium, or Low based on expert judgment and likelihood/impact matrices rather than precise dollar values. Which type of risk assessment is this?

- A) Quantitative
- B) Qualitative
- C) Hybrid
- D) Residual

<details>
<summary>Answer</summary>

**B) Qualitative**

Qualitative risk assessment uses subjective categories (High/Medium/Low) and expert judgment to evaluate risk. Quantitative uses numerical values (ALE, SLE, ARO). Qualitative is faster but less precise; quantitative requires more data but produces dollar-value estimates.
</details>

---

### Q2. Business Impact Analysis (BIA)

An organization determines that their e-commerce platform generates $50,000/hour in revenue and that the maximum acceptable downtime is 4 hours. Which BIA metric defines the maximum acceptable downtime?

- A) Recovery Time Objective (RTO)
- B) Recovery Point Objective (RPO)
- C) Mean Time to Repair (MTTR)
- D) Maximum Tolerable Downtime (MTD)

<details>
<summary>Answer</summary>

**A) Recovery Time Objective (RTO)**

RTO defines the maximum acceptable time to restore a system after a disruption. RPO defines the maximum acceptable data loss measured in time. MTTR is the average time to repair a failed component. MTD is the total outage time an organization can survive.
</details>

---

### Q3. Risk Response — Transfer

A company purchases a cybersecurity insurance policy to cover potential losses from a data breach. Which risk response strategy does this represent?

- A) Risk avoidance
- B) Risk mitigation
- C) Risk transfer
- D) Risk acceptance

<details>
<summary>Answer</summary>

**C) Risk transfer**

Risk transfer shifts the financial impact of a risk to a third party — typically through insurance or contractual arrangements. The risk itself doesn't disappear, but the financial burden is shared or transferred.
</details>

---

### Q4. Security Policy

A document states: "All employees must use company-approved encrypted communication tools for transmitting sensitive data. Violations may result in disciplinary action up to and including termination." What type of document is this?

- A) Standard
- B) Guideline
- C) Policy
- D) Procedure

<details>
<summary>Answer</summary>

**C) Policy**

A policy is a high-level mandatory statement of management intent. It defines what must be done and consequences for non-compliance. Standards define specific requirements. Procedures define step-by-step how-to. Guidelines are recommendations (not mandatory).
</details>

---

### Q5. Third-Party Risk — Vendor Assessment

Before selecting a cloud provider to store sensitive customer data, an organization evaluates the vendor's SOC 2 Type II report, reviews their security controls, and assesses their incident response capabilities. Which risk management activity is this?

- A) Penetration testing
- B) Vendor assessment
- C) Internal audit
- D) Gap analysis

<details>
<summary>Answer</summary>

**B) Vendor assessment**

Vendor assessment evaluates a third party's security posture before engaging them. SOC 2 Type II reports provide independent verification of a vendor's security controls over time. This is a critical third-party risk management activity.
</details>

---

### Q6. Data Classification

An organization labels its data as Public, Internal, Confidential, and Restricted, with each classification level requiring progressively stronger security controls. What is this process called?

- A) Data masking
- B) Data classification
- C) Data retention
- D) Data sovereignty

<details>
<summary>Answer</summary>

**B) Data classification**

Data classification categorizes data based on sensitivity and value, determining the appropriate level of security controls. Common schemes: Public → Internal → Confidential → Restricted (or Top Secret in government).
</details>

---

### Q7. Quantitative Risk — ALE

An organization estimates that a server failure occurs once every 5 years (ARO = 0.2) and each occurrence costs $100,000 (SLE). What is the Annual Loss Expectancy (ALE)?

- A) $500,000
- B) $100,000
- C) $20,000
- D) $50,000

<details>
<summary>Answer</summary>

**C) $20,000**

ALE = SLE × ARO = $100,000 × 0.2 = $20,000 per year. ALE helps organizations make cost-effective decisions about security controls — a control costing more than $20,000/year to prevent this risk may not be justified.
</details>

---

### Q8. Compliance — PCI DSS

A retail company that processes credit card transactions must comply with a standard that requires encryption of cardholder data, regular vulnerability scans, and access controls. Which compliance framework is this?

- A) HIPAA
- B) SOX
- C) PCI DSS
- D) GDPR

<details>
<summary>Answer</summary>

**C) PCI DSS (Payment Card Industry Data Security Standard)**

PCI DSS applies to any organization that stores, processes, or transmits credit card data. It mandates specific security controls including encryption, vulnerability management, access controls, and regular testing.
</details>

---

### Q9. Acceptable Use Policy (AUP)

An employee is disciplined for using their company laptop to mine cryptocurrency. The organization references a signed document that explicitly prohibits using company resources for personal commercial activities. What is this document?

- A) NDA
- B) Acceptable Use Policy (AUP)
- C) Service Level Agreement (SLA)
- D) Memorandum of Understanding (MOU)

<details>
<summary>Answer</summary>

**B) Acceptable Use Policy (AUP)**

An AUP defines acceptable and prohibited uses of company IT resources. Employees typically sign the AUP acknowledging they understand the rules. It provides the organizational basis for disciplinary action when policies are violated.
</details>

---

### Q10. Penetration Testing Phases

A security firm is engaged to test an organization's defenses. The firm begins by gathering publicly available information about the target — employee names, email formats, IP ranges, and technology stack — from LinkedIn, DNS records, and WHOIS. Which penetration testing phase is this?

- A) Exploitation
- B) Scanning and enumeration
- C) Reconnaissance (information gathering)
- D) Reporting

<details>
<summary>Answer</summary>

**C) Reconnaissance (information gathering)**

Reconnaissance is the first phase of penetration testing, involving passive and active information gathering about the target. Passive recon uses public sources (OSINT). Active recon directly interacts with target systems (scanning).
</details>

---

### Q11. Data Retention Policy

A company's legal department requires that all financial records be retained for 7 years to comply with regulatory requirements, after which they must be securely destroyed. Which policy governs this?

- A) Data classification policy
- B) Data retention policy
- C) Backup policy
- D) Incident response policy

<details>
<summary>Answer</summary>

**B) Data retention policy**

A data retention policy defines how long data must be kept and when it must be destroyed. Retention periods are often driven by regulatory requirements (SOX, HIPAA, GDPR) and legal obligations.
</details>

---

### Q12. Separation of Duties

An organization requires that the person who approves a purchase order cannot be the same person who issues the payment. Which security principle does this implement?

- A) Least privilege
- B) Separation of duties
- C) Job rotation
- D) Mandatory vacation

<details>
<summary>Answer</summary>

**B) Separation of duties**

Separation of duties divides critical tasks among multiple people so no single person can complete a high-risk action alone. This prevents fraud and errors by requiring collusion between multiple individuals.
</details>

---

### Q13. Risk Register

A security team maintains a document listing all identified risks, their likelihood, impact, current status, assigned owners, and planned mitigation actions. What is this document called?

- A) Risk assessment report
- B) Risk register
- C) Business impact analysis
- D) Security audit report

<details>
<summary>Answer</summary>

**B) Risk register**

A risk register is a living document that tracks all identified risks along with their assessment, ownership, and treatment status. It's a central artifact for ongoing risk management.
</details>

---

### Q14. NDA — Non-Disclosure Agreement

Before a third-party auditor reviews an organization's security controls, both parties sign a document preventing the auditor from sharing confidential information discovered during the audit. Which agreement is this?

- A) SLA
- B) NDA (Non-Disclosure Agreement)
- C) MOU
- D) BPA

<details>
<summary>Answer</summary>

**B) NDA (Non-Disclosure Agreement)**

An NDA legally binds parties to protect confidential information shared between them. NDAs are critical when third parties will have access to sensitive systems, data, or processes.
</details>

---

### Q15. Security Awareness Training

After a phishing simulation reveals that 30% of employees clicked a malicious link, the security team mandates additional training focused on identifying phishing emails. Which security program component is this?

- A) Penetration testing
- B) Security awareness training
- C) Tabletop exercise
- D) Vulnerability management

<details>
<summary>Answer</summary>

**B) Security awareness training**

Security awareness training educates employees about threats and security best practices. Phishing simulations are a common tool for testing awareness and identifying who needs additional training.
</details>

---

### Q16. SLA — Service Level Agreement

A cloud provider guarantees 99.99% uptime and commits to a response time of under 15 minutes for critical issues. These commitments are documented in which agreement?

- A) NDA
- B) SLA (Service Level Agreement)
- C) MOU
- D) AUP

<details>
<summary>Answer</summary>

**B) SLA (Service Level Agreement)**

An SLA defines measurable performance metrics and service guarantees between a service provider and customer — including uptime percentages, response times, and remediation timelines.
</details>

---

### Q17. GDPR — Data Subject Rights

Under GDPR, a customer requests that a company delete all of their personal data from their systems. Which GDPR right is the customer exercising?

- A) Right to access
- B) Right to be forgotten (right to erasure)
- C) Right to data portability
- D) Right to rectification

<details>
<summary>Answer</summary>

**B) Right to be forgotten (right to erasure)**

GDPR Article 17 grants individuals the right to request deletion of their personal data when it's no longer necessary, consent is withdrawn, or data was unlawfully processed. Organizations must comply unless legal retention requirements override the request.
</details>

---

### Q18. Residual Risk

After implementing a firewall, IDS, and MFA, an organization determines that some risk still remains because no security control is 100% effective. What is this remaining risk called?

- A) Inherent risk
- B) Residual risk
- C) Risk appetite
- D) Risk tolerance

<details>
<summary>Answer</summary>

**B) Residual risk**

Residual risk is the risk that remains after controls are applied. Inherent risk is the risk before any controls. Organizations must ensure residual risk falls within their risk appetite (the amount of risk they're willing to accept).
</details>

---

### Q19. External Audit

A regulatory body sends an independent assessor to verify that a financial institution's security controls meet industry requirements. The institution has no control over the scope or timing of this assessment. Which type of audit is this?

- A) Internal audit
- B) External audit
- C) Self-assessment
- D) Penetration test

<details>
<summary>Answer</summary>

**B) External audit**

An external audit is conducted by an independent third party, often required by regulations. The organization being audited has limited control over the scope. Internal audits are conducted by the organization itself.
</details>

---

### Q20. Risk Avoidance

A company decides not to collect or store customer credit card information at all, instead using a third-party payment processor for all transactions. Which risk response strategy does this represent?

- A) Risk transfer
- B) Risk avoidance
- C) Risk mitigation
- D) Risk acceptance

<details>
<summary>Answer</summary>

**B) Risk avoidance**

Risk avoidance eliminates the risk entirely by not engaging in the risky activity. By not storing credit card data, the company avoids PCI DSS compliance requirements and the risk of cardholder data breach entirely.
</details>

---

### Q21. Job Rotation

An organization periodically moves employees between different roles and responsibilities. This practice helps detect fraud and reduces the risk of a single person having unchecked control over a process. Which security practice is this?

- A) Least privilege
- B) Mandatory vacation
- C) Job rotation
- D) Separation of duties

<details>
<summary>Answer</summary>

**C) Job rotation**

Job rotation moves employees between roles periodically. This cross-trains staff (improving business continuity) and helps detect fraud — irregularities may surface when a new person takes over responsibilities.
</details>

---

### Q22. Data Privacy Officer (DPO)

GDPR requires certain organizations to appoint an individual responsible for overseeing data protection strategy and compliance. What is this role called?

- A) CISO
- B) Data Privacy Officer (DPO)
- C) Security Analyst
- D) Compliance Manager

<details>
<summary>Answer</summary>

**B) Data Privacy Officer (DPO)**

GDPR requires organizations processing personal data at scale to appoint a DPO. The DPO oversees data protection compliance, advises on data privacy obligations, and serves as a point of contact for supervisory authorities.
</details>

---

### Q23. Threat Intelligence

An organization subscribes to feeds that provide indicators of compromise (IoCs) — malicious IP addresses, domains, file hashes, and TTPs — used by current threat actors. What is this information called?

- A) Vulnerability intelligence
- B) Threat intelligence
- C) Security baselines
- D) Compliance data

<details>
<summary>Answer</summary>

**B) Threat intelligence**

Threat intelligence provides information about current and emerging threats — including IoCs, threat actor profiles, attack patterns, and TTPs. It enables proactive defense by informing detection rules, hunting activities, and strategic planning.
</details>

---

### Q24. Regulatory Compliance — HIPAA

A healthcare organization is fined for failing to encrypt patient health information stored on employee laptops, one of which was stolen from a car. Which regulation was violated?

- A) PCI DSS
- B) GDPR
- C) HIPAA
- D) SOX

<details>
<summary>Answer</summary>

**C) HIPAA (Health Insurance Portability and Accountability Act)**

HIPAA requires healthcare organizations to protect the confidentiality, integrity, and availability of Protected Health Information (PHI). Failing to encrypt PHI on portable devices is a common HIPAA violation leading to significant fines.
</details>

