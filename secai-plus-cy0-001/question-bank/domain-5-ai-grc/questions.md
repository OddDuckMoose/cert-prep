# Domain 5 — AI Governance, Risk & Compliance (~13%)

## Bank 1

### Q1. NIST AI RMF — MAP Function

The NIST AI Risk Management Framework (AI RMF) defines four core functions. A company conducts an assessment of its AI systems to identify potential harms, affected stakeholders, and risk context before implementing any controls. Which NIST AI RMF function does this activity PRIMARILY represent?

- A) GOVERN
- B) MAP
- C) MEASURE
- D) MANAGE

<details>
<summary>Answer</summary>

**B) MAP**

The MAP function contextualizes AI risk — identifying the AI system's intended use, affected stakeholders, potential harms, and risk context. It comes before MEASURE (which quantifies risk) and MANAGE (which treats it). GOVERN establishes the organizational policies and culture for responsible AI.
</details>

---

### Q2. EU AI Act — Unacceptable Risk (Predictive Policing)

Under the EU AI Act, an AI system used by law enforcement to predict the likelihood that an individual will commit a future crime would fall into which risk classification?

- A) Minimal risk — no regulatory requirements apply
- B) Limited risk — transparency obligations required
- C) High risk — conformity assessment and technical documentation required
- D) Unacceptable risk — prohibited in the EU

<details>
<summary>Answer</summary>

**D) Unacceptable risk — prohibited in the EU**

The EU AI Act explicitly prohibits AI systems used for predictive policing of individuals based on profiling — classifying them as 'unacceptable risk' and banning them.
</details>

---

### Q3. OWASP LLM08 — Excessive Agency (Code Review Tool)

Which OWASP Top 10 for LLM Applications vulnerability is described: An LLM-powered code review tool is given a plugin to automatically merge approved pull requests. A developer crafts a prompt that causes the LLM to approve and merge a malicious PR containing backdoor code.

- A) LLM01 – Prompt Injection
- B) LLM07 – Insecure Plugin Design
- C) LLM08 – Excessive Agency
- D) LLM02 – Insecure Output Handling

<details>
<summary>Answer</summary>

**C) LLM08 – Excessive Agency**

LLM08 describes an LLM given too much autonomy — in this case, the ability to take a consequential irreversible action (merging code) without sufficient human oversight.
</details>

---

### Q4. AI Risk Register Elements

A CISO is building an AI risk register for a new customer-facing AI chatbot. According to NIST AI RMF best practices, which elements should the risk register MINIMALLY include?

- A) Training dataset size, model accuracy metrics, and GPU specifications
- B) Risk description, likelihood, potential impact, risk owner, and mitigation measures
- C) Model vendor name, open-source license type, and deployment region
- D) Historical attack logs, CVE identifiers, and patch status

<details>
<summary>Answer</summary>

**B) Risk description, likelihood, potential impact, risk owner, and mitigation measures**

A risk register should capture: what the risk is, how likely it is to occur, what the impact would be, who owns the risk, and what mitigations are in place. This is standard risk management practice applied to AI under NIST AI RMF's MANAGE function.
</details>

---

### Q5. GDPR Article 22 — Right to Explanation

Under GDPR, an organization uses an AI model to make fully automated decisions about loan approvals that significantly affect applicants. What right does GDPR grant to individuals subjected to these decisions?

- A) The right to request deletion of the AI model that processed their data
- B) The right to an explanation of the decision and the right not to be subject to solely automated decisions with legal effects
- C) The right to access the model's source code and training data
- D) The right to opt out of any AI processing and require manual review of all future interactions

<details>
<summary>Answer</summary>

**B) The right to an explanation of the decision and the right not to be subject to solely automated decisions with legal effects**

GDPR Article 22 grants individuals the right not to be subject to solely automated decisions with legal or significant effects, and the right to obtain a meaningful explanation of the logic involved. This directly requires XAI capabilities and human review mechanisms.
</details>

---

### Q6. NIST AI RMF — GOVERN Function

Which of the following BEST describes the primary purpose of the GOVERN function in the NIST AI Risk Management Framework?

- A) To quantify and measure the risks of deployed AI systems using technical metrics
- B) To establish organizational policies, roles, culture, and accountability structures that enable responsible AI risk management
- C) To identify and prioritize AI risks before deploying controls
- D) To implement specific technical controls that mitigate identified AI risks

<details>
<summary>Answer</summary>

**B) To establish organizational policies, roles, culture, and accountability structures that enable responsible AI risk management**

GOVERN is the overarching function that establishes the organizational foundation for all other AI RMF functions — defining policies, assigning roles and responsibilities, setting risk tolerance, and cultivating a culture of responsible AI.
</details>

---

### Q7. Fairness — Biased Hiring Tool

An organization is deploying an AI hiring tool that screens resumes. The tool was trained on historical hiring data from 2010–2020. A GRC analyst flags that the model may perpetuate historical bias against certain demographic groups. Which ethical AI principle is MOST directly at risk?

- A) Transparency — the model's decisions cannot be explained
- B) Fairness — the model may produce discriminatory outputs based on biased training data
- C) Availability — biased models increase downtime risk
- D) Confidentiality — demographic data in training sets creates privacy risk

<details>
<summary>Answer</summary>

**B) Fairness — the model may produce discriminatory outputs based on biased training data**

Fairness is the ethical AI principle at risk when a model trained on historically biased data replicates or amplifies those biases in outputs. The EU AI Act classifies AI employment tools as high-risk for this reason.
</details>

---

### Q8. Third-Party AI Vendor Risk Assessment

A third-party vendor provides an AI-powered threat intelligence service under a SaaS model. The organization's GRC team must assess the risk of using this service. Which assessment activity is MOST aligned with AI supply chain risk management best practices?

- A) Reviewing the vendor's bug bounty program and CVE history
- B) Conducting a vendor AI risk assessment covering data handling practices, model governance, bias testing, and security controls for the AI system
- C) Requiring the vendor to disclose the full model weights and architecture for internal review
- D) Testing the service's API rate limits and uptime SLA

<details>
<summary>Answer</summary>

**B) Conducting a vendor AI risk assessment covering data handling practices, model governance, bias testing, and security controls for the AI system**

Third-party AI vendor risk assessment should examine how the vendor handles data, their model governance practices, bias testing results, and security controls specific to the AI system.
</details>

---

## Bank 2

### Q9. GDPR Article 22 — Automated Decision-Making Documentation

An organization's legal team asks the AI security team to explain how AI systems must be documented under GDPR for automated decision-making. Which GDPR provision is MOST directly relevant?

- A) GDPR Article 32 — Security of processing
- B) GDPR Article 22 — Right not to be subject to solely automated decision-making and right to explanation
- C) GDPR Article 17 — Right to erasure
- D) GDPR Article 5 — Principles relating to processing of personal data

<details>
<summary>Answer</summary>

**B) GDPR Article 22 — Right not to be subject to solely automated decision-making and right to explanation**

GDPR Article 22 specifically addresses automated decision-making including profiling that produces legal or significant effects. It grants individuals the right to human review and a meaningful explanation.
</details>

---

### Q10. EU AI Act — Provider Responsibilities

Under the EU AI Act, which actor in the AI value chain has PRIMARY responsibility for ensuring a high-risk AI system complies with the Act's requirements before placing it on the market?

- A) The end-user deploying the AI system in their operations
- B) The AI provider (developer/manufacturer) who develops and markets the AI system
- C) The EU member state regulator in the country of deployment
- D) The cloud provider hosting the AI system's infrastructure

<details>
<summary>Answer</summary>

**B) The AI provider (developer/manufacturer) who develops and markets the AI system**

The EU AI Act places primary compliance obligations on providers — the entities that develop and place AI systems on the market. Providers must conduct conformity assessments, maintain technical documentation, and register high-risk systems in the EU database before deployment.
</details>

---

### Q11. NIST AI RMF — MEASURE Function

A security team is implementing the NIST AI RMF MEASURE function for a deployed threat detection AI. Which activity is MOST aligned with this function?

- A) Defining the organization's AI risk tolerance and assigning model ownership
- B) Continuously monitoring model performance metrics, drift indicators, and fairness measurements against established benchmarks
- C) Identifying the stakeholders affected by the AI system's decisions
- D) Implementing technical controls to mitigate the highest-priority identified risks

<details>
<summary>Answer</summary>

**B) Continuously monitoring model performance metrics, drift indicators, and fairness measurements against established benchmarks**

The MEASURE function involves analyzing and quantifying AI risks through ongoing metrics, testing, and evaluation. GOVERN handles risk tolerance and ownership. MAP handles stakeholder identification. MANAGE implements mitigations.
</details>

---

### Q12. Fairness — Gender-Coded Language Bias

An AI ethics review board flags that an NLP model used for employee performance reviews uses 'gender-coded language' patterns from training data to score responses, systematically rating responses in stereotypically 'male' communication styles higher. Which AI ethics principle and risk does this raise?

- A) Transparency — the model's scoring rationale is not explainable
- B) Fairness — systematic bias from training data is producing discriminatory outcomes in employment decisions
- C) Availability — biased models create operational reliability risks
- D) Accountability — the model owner has not been properly assigned

<details>
<summary>Answer</summary>

**B) Fairness — systematic bias from training data is producing discriminatory outcomes in employment decisions**

This raises fairness concerns — the model has inherited and is perpetuating societal biases from training data, producing discriminatory outcomes in high-stakes employment decisions.
</details>

---

### Q13. ISO/IEC 42001:2023

ISO/IEC 42001:2023 is the international standard for AI management systems. Which of the following BEST describes its primary scope?

- A) Technical specifications for secure ML model deployment in cloud environments
- B) Requirements for establishing, implementing, maintaining, and continually improving an AI management system within organizations
- C) A certification scheme for individual AI security professionals
- D) Technical requirements for adversarial robustness testing of AI models

<details>
<summary>Answer</summary>

**B) Requirements for establishing, implementing, maintaining, and continually improving an AI management system within organizations**

ISO/IEC 42001 is the AI management system standard — analogous to ISO 27001 for information security management.
</details>

---

### Q14. AI-Specific Vendor Risk Assessment

A security team is building an AI risk assessment process for evaluating third-party AI tools before procurement. Beyond standard cybersecurity vendor assessments, which AI-specific dimension should be REQUIRED?

- A) The vendor's GitHub repository commit history and open-source contribution activity
- B) Assessment of training data sourcing practices, model bias testing results, governance processes, and incident history for AI-specific failures
- C) The vendor's hardware procurement costs for GPU infrastructure
- D) Comparison of the vendor's model accuracy metrics against public benchmarks

<details>
<summary>Answer</summary>

**B) Assessment of training data sourcing practices, model bias testing results, governance processes, and incident history for AI-specific failures**

Third-party AI vendor risk assessment must include AI-specific dimensions: how was training data sourced, what bias testing was conducted, what governance processes ensure ongoing model safety, and has the vendor had AI-specific incidents.
</details>

---

### Q15. AI-Specific Incident — Model Drift

A GRC analyst is developing an AI incident response plan. Which category of incident is UNIQUE to AI systems and would NOT be covered by a traditional cybersecurity incident response plan?

- A) Unauthorized access to the AI system's cloud infrastructure
- B) Data exfiltration from the AI system's training data storage
- C) Model drift causing silent performance degradation resulting in systematically incorrect decisions over weeks
- D) DDoS attack against the AI inference endpoint

<details>
<summary>Answer</summary>

**C) Model drift causing silent performance degradation resulting in systematically incorrect decisions over weeks**

Model drift causing silent performance degradation is unique to AI systems — there is no traditional IT equivalent where a system gradually produces increasingly wrong answers without any security event occurring. This requires AI-specific monitoring, drift detection thresholds, and response procedures.
</details>

---

### Q16. Healthcare AI Compliance Gap (Scenario)

**SCENARIO:** A healthcare organization has deployed an AI triage system that recommends patient care priority in the emergency department. The system was developed by a third-party vendor and trained on data from hospitals in three US states. A GRC audit identifies: no bias testing across demographic groups has been performed, the model has not been updated in 18 months despite significant ER patient demographic shifts, and there is no human override process documented. Under the EU AI Act and NIST AI RMF, which finding represents the MOST critical compliance gap?

- A) The model was developed by a third-party vendor rather than in-house
- B) The combination of no bias testing on a high-risk medical AI system, no drift monitoring, and no documented human oversight mechanism represents a critical multi-framework compliance failure
- C) The model was trained on US data rather than EU data, creating GDPR concerns
- D) The vendor has not provided ISO/IEC 42001 certification for the AI system

<details>
<summary>Answer</summary>

**B) The combination of no bias testing on a high-risk medical AI system, no drift monitoring, and no documented human oversight mechanism represents a critical multi-framework compliance failure**

Medical triage AI is high-risk under EU AI Act and safety-critical under NIST AI RMF. The combined failures — no demographic bias testing, no drift monitoring (18 months without update), and no human oversight documentation — represent critical failures in both frameworks.
</details>

