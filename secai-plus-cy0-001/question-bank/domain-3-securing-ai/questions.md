# Domain 3 — Securing AI Systems (~30%)

## Bank 1

### Q1. Federated Learning for Data Residency

An ML engineer is designing a training pipeline for a credit risk model that will use data contributed by multiple financial institutions. Each institution must keep its customer data on-premises due to regulatory requirements. Which AI training technique BEST addresses both the collaborative training requirement and the data residency constraint?

- A) Transfer learning from a publicly available model
- B) Federated learning
- C) Data augmentation
- D) Centralized cloud training with VPN

<details>
<summary>Answer</summary>

**B) Federated learning**

Federated learning trains a model across decentralized devices or organizations by sharing only model gradient updates, never raw data. This satisfies data residency requirements while enabling collaborative model improvement.
</details>

---

### Q2. Supply Chain Risk from Pre-Trained Models

A security architect is reviewing an AI pipeline where a third-party pre-trained model is downloaded from a public repository and deployed to production without verification. Which risk does this practice introduce?

- A) Model hallucination due to unverified parameters
- B) Supply chain compromise through potentially backdoored or poisoned pre-trained weights
- C) Excessive agency from unverified model capabilities
- D) Differential privacy violations from open-source models

<details>
<summary>Answer</summary>

**B) Supply chain compromise through potentially backdoored or poisoned pre-trained weights**

Downloading pre-trained models from public repositories without verification introduces supply chain risk — the model weights may contain backdoors, trojans, or privacy leakage from the original training data. This maps to OWASP LLM05 (Supply Chain Vulnerabilities).
</details>

---

### Q3. Data Provenance

Which of the following BEST describes data provenance in the context of AI security?

- A) The encryption standard applied to training data at rest
- B) The ability to track the origin, transformations, and custody chain of data throughout the ML pipeline
- C) The process of anonymizing training data before use
- D) The documentation of model hyperparameters for reproducibility

<details>
<summary>Answer</summary>

**B) The ability to track the origin, transformations, and custody chain of data throughout the ML pipeline**

Data provenance refers to tracking the complete lineage of data — its origin, all transformations applied, who handled it, and when. In AI security, this is critical for detecting poisoning attacks, ensuring data integrity, and meeting compliance requirements.
</details>

---

### Q4. Model Integrity in CI/CD

An organization's MLOps team is implementing security controls for their model registry. Which combination of controls BEST protects model integrity throughout the CI/CD pipeline?

- A) Encrypting model files at rest and requiring MFA for developer access
- B) Model signing with cryptographic signatures, version control, and automated scanning of model artifacts before promotion
- C) Storing models in an air-gapped environment and requiring manual deployment approvals
- D) Using differential privacy during training and rate limiting the inference API

<details>
<summary>Answer</summary>

**B) Model signing with cryptographic signatures, version control, and automated scanning of model artifacts before promotion**

Model signing (cryptographic signing of model artifacts), version control (tracking changes and enabling rollback), and automated scanning (detecting trojans or anomalous weights) together form a defense-in-depth approach to model integrity in CI/CD.
</details>

---

### Q5. Input Validation and Output Filtering

A security team needs to protect a deployed NLP model from producing harmful outputs when processing untrusted user input. Which control should be implemented at the inference boundary?

- A) Differential privacy applied to the input tokens
- B) Input validation and output filtering at the inference layer
- C) Federated learning to distribute inference risk
- D) Adversarial training against membership inference attacks

<details>
<summary>Answer</summary>

**B) Input validation and output filtering at the inference layer**

Input validation (sanitizing, filtering, or sandboxing user inputs before passing to the model) and output filtering (scanning model responses for harmful content, PII, or policy violations) are the primary defense controls at the inference boundary for untrusted inputs.
</details>

---

### Q6. Shared Responsibility Model for Cloud AI

Under the shared responsibility model for cloud AI services such as AWS SageMaker or Azure ML, which security responsibility falls SOLELY on the customer organization?

- A) Physical security of the underlying GPU hardware
- B) Hypervisor security and VM isolation
- C) Security of training data, model access controls, and output monitoring
- D) Network infrastructure and backbone security

<details>
<summary>Answer</summary>

**C) Security of training data, model access controls, and output monitoring**

In cloud AI services, the provider is responsible for physical security, hypervisor isolation, and network infrastructure. The customer is responsible for securing their own training data, configuring access controls on their model endpoints, and monitoring model outputs.
</details>

---

### Q7. Mitigating Training Data Poisoning

An organization is implementing controls to protect against training data poisoning in their internal threat intelligence ML pipeline. Which control would MOST directly address this threat?

- A) Encrypting the model weights at rest using AES-256
- B) Implementing input anomaly detection and data validation on ingested threat feeds
- C) Rate limiting queries to the model's inference API
- D) Requiring multi-factor authentication for model deployment

<details>
<summary>Answer</summary>

**B) Implementing input anomaly detection and data validation on ingested threat feeds**

Data poisoning is mitigated at the data ingestion phase through anomaly detection (identifying statistically unusual samples), data validation (enforcing schema and value constraints), and data provenance controls.
</details>

---

### Q8. Differential Privacy Purpose

What is the primary security purpose of implementing differential privacy in a machine learning training pipeline?

- A) To prevent overfitting by adding noise during backpropagation
- B) To limit the ability of any single individual's data to influence model outputs, reducing privacy leakage risk
- C) To encrypt the gradient updates transmitted during federated learning
- D) To detect adversarial examples before they reach the model

<details>
<summary>Answer</summary>

**B) To limit the ability of any single individual's data to influence model outputs, reducing privacy leakage risk**

Differential privacy provides mathematical guarantees that the inclusion or exclusion of any single individual's data produces negligible difference in model outputs. This directly limits privacy attacks like membership inference and model inversion.
</details>

---

### Q9. Network Segmentation for GPU Clusters

A company is evaluating security controls for a GPU cluster used for training large language models. The cluster handles highly sensitive IP. Which network security control is MOST critical for this environment?

- A) Web application firewall (WAF) in front of the training cluster
- B) Network segmentation isolating the ML training environment from general corporate networks
- C) TLS encryption on the model serving endpoint
- D) Intrusion detection tuned for web application attacks

<details>
<summary>Answer</summary>

**B) Network segmentation isolating the ML training environment from general corporate networks**

Network segmentation is the most critical control — isolating the ML training environment prevents lateral movement from corporate networks, limits the blast radius of a compromise, and reduces the attack surface for data exfiltration.
</details>

---

### Q10. Detecting Backdoored Pre-Trained Models

Which technique would BEST help an organization detect that a pre-trained model downloaded from an external source has been backdoored?

- A) Reviewing the model's public documentation and change logs
- B) Applying neural cleanse or activation clustering techniques to inspect model behavior on trigger patterns
- C) Running the model through a SAST tool for code vulnerabilities
- D) Verifying the model's API rate limits match documentation

<details>
<summary>Answer</summary>

**B) Applying neural cleanse or activation clustering techniques to inspect model behavior on trigger patterns**

Neural cleanse and activation clustering are model inspection techniques that can reveal backdoor triggers by analyzing internal activation patterns. SAST tools scan source code, not model weights.
</details>

---

### Q11. Model Watermarking

An AI security architect is designing an MLOps pipeline with security controls. At which stage should model watermarking PRIMARILY be applied?

- A) During data preprocessing before training
- B) After model training before deployment to the model registry
- C) At the inference endpoint to mark each prediction
- D) During federated learning gradient aggregation

<details>
<summary>Answer</summary>

**B) After model training before deployment to the model registry**

Model watermarking embeds an imperceptible signature into model weights or behavior after training, before deployment. This allows the organization to later prove ownership if the model is stolen or if an unauthorized copy is discovered.
</details>

---

### Q12. Unrestricted Write Access to Training Data

A security review of a machine learning pipeline identifies that data scientists have direct write access to the production training dataset stored in a cloud object store. No versioning is enabled. Which risks does this create?

- A) Increased risk of model hallucination and reduced inference speed
- B) Unauthorized modification of training data (poisoning risk) and inability to detect or rollback changes
- C) Violation of the EU AI Act's minimal risk classification requirements
- D) Increased exposure to membership inference attacks through unrestricted API access

<details>
<summary>Answer</summary>

**B) Unauthorized modification of training data (poisoning risk) and inability to detect or rollback changes**

Unrestricted write access to production training data creates poisoning risk (intentional or accidental data corruption) and, without versioning, eliminates the ability to detect changes or rollback to a known-good state.
</details>

---

### Q13. Least Privilege for Model Service Accounts

When deploying an AI model as a containerized microservice, which principle should guide the assignment of permissions to the model's runtime service account?

- A) Grant broad permissions to ensure the model can access any data it may need at runtime
- B) Apply the principle of least privilege — grant only the specific permissions required for the model to function
- C) Use a shared service account across all AI microservices for simplified management
- D) Assign admin-level permissions temporarily and revoke them after initial deployment

<details>
<summary>Answer</summary>

**B) Apply the principle of least privilege — grant only the specific permissions required for the model to function**

Least privilege is fundamental to securing AI runtime environments. A model's service account should only have permission to read its required input data sources and write to its designated output endpoints.
</details>

---

### Q14. Data Minimization for PII

An organization trains a customer churn prediction model on a dataset containing names, email addresses, and purchase histories. A privacy impact assessment flags that the model may retain personally identifiable information in its weights. Which technique BEST mitigates this risk during training?

- A) Encrypting the dataset with AES-256 before training begins
- B) Applying data minimization and anonymization techniques to remove PII before training
- C) Using model watermarking to track if the model is redistributed
- D) Implementing rate limiting on the inference API to prevent bulk data extraction

<details>
<summary>Answer</summary>

**B) Applying data minimization and anonymization techniques to remove PII before training**

Data minimization and anonymization remove or pseudonymize PII from the training dataset before the model ever processes it. This prevents PII from being embedded in model weights.
</details>

---

### Q15. Encrypted Transit for Hybrid AI

A hybrid AI architecture trains models on an on-premises GPU cluster and serves inference in a public cloud. Which security control is MOST important at the boundary between these environments?

- A) Identical IAM policies in both on-prem and cloud environments
- B) Encrypted transit for model artifacts and API traffic crossing the boundary
- C) Replicating all training data to the cloud for redundancy
- D) Using the same GPU hardware vendor in both environments

<details>
<summary>Answer</summary>

**B) Encrypted transit for model artifacts and API traffic crossing the boundary**

Model artifacts and API traffic crossing between on-premises and cloud environments must be encrypted in transit to prevent interception or tampering.
</details>

---

### Q16. Audit Logs for Model Tampering

Which of the following audit log entries would be MOST useful for investigating a suspected model weight tampering incident in an MLOps pipeline?

- A) User login events for the data science team's laptops
- B) Model registry write events, including who promoted which model version, with timestamps and checksums
- C) Inference API latency metrics and request volume by hour
- D) Cloud billing anomalies indicating unusual GPU usage

<details>
<summary>Answer</summary>

**B) Model registry write events, including who promoted which model version, with timestamps and checksums**

Model registry write events — including who promoted a model, when, from which pipeline run, with cryptographic checksums — provide the evidence trail needed to investigate weight tampering.
</details>

---

### Q17. Excessive Agency (OWASP LLM08)

An organization is assessing the security of its LLM-powered code assistant. The tool has access to the company's internal Git repositories and can execute code snippets. An attacker could potentially use this access path to exfiltrate code or run malicious scripts. Which OWASP LLM vulnerability does this BEST represent?

- A) LLM01 – Prompt Injection
- B) LLM07 – Insecure Plugin Design
- C) LLM08 – Excessive Agency
- D) LLM03 – Training Data Poisoning

<details>
<summary>Answer</summary>

**C) LLM08 – Excessive Agency**

LLM08 describes a scenario where an LLM has been granted more permissions, tools, or capabilities than necessary. Access to Git repos and code execution is excessive agency.
</details>

---

### Q18. Separation of Duties (Scenario)

**SCENARIO:** A financial institution's fraud detection ML model is deployed in a Kubernetes cluster. During a penetration test, the red team compromises a data scientist's developer workstation and discovers the workstation has direct read/write access to the production model registry, training data S3 bucket, and the inference endpoint's admin console. Which security principle has MOST clearly been violated?

- A) Data minimization
- B) Defense in depth through network segmentation
- C) Separation of duties and least privilege across environments
- D) Encryption of data at rest and in transit

<details>
<summary>Answer</summary>

**C) Separation of duties and least privilege across environments**

A single developer workstation should never have combined access to production training data, the model registry, AND the inference admin console. Separation of duties requires that no single account or workstation can both modify training data AND promote models to production.
</details>

---

## Bank 2

### Q19. Feature Engineering Manipulation

An organization's security team is conducting a threat model of their ML pipeline. They identify that an attacker with write access to the data preprocessing scripts could modify feature engineering logic to systematically exclude fraud indicators for specific account types. At which pipeline stage and under which threat category does this fall?

- A) Inference stage; evasion attack
- B) Feature engineering stage; targeted data manipulation / indirect poisoning
- C) Model serving stage; model extraction
- D) Training stage; membership inference

<details>
<summary>Answer</summary>

**B) Feature engineering stage; targeted data manipulation / indirect poisoning**

Feature engineering manipulation is a form of indirect poisoning — rather than modifying raw data, the attacker alters the transformation logic to systematically bias what the model learns.
</details>

---

### Q20. Federated Learning vs. SMPC

A security architect must choose between federated learning and secure multi-party computation (SMPC) for protecting training data privacy. Which statement BEST characterizes their primary difference?

- A) Federated learning shares raw gradients while SMPC shares encrypted data
- B) Federated learning keeps raw data local and shares only model updates; SMPC enables joint computation over encrypted data without revealing inputs to any party
- C) Federated learning requires central coordination; SMPC is fully decentralized
- D) Federated learning is only for horizontal data partitioning; SMPC is only for vertical partitioning

<details>
<summary>Answer</summary>

**B) Federated learning keeps raw data local and shares only model updates; SMPC enables joint computation over encrypted data without revealing inputs to any party**

Federated learning keeps raw data on-device/on-premises and only shares gradient updates (which can still leak information). SMPC is a cryptographic protocol enabling multiple parties to jointly compute a function over their private inputs without revealing those inputs.
</details>

---

### Q21. Model Cards

Which of the following BEST describes the concept of 'model cards' and their relevance to AI security governance?

- A) Digital certificates used to authenticate model artifacts in a model registry
- B) Standardized documentation describing a model's intended uses, performance characteristics, limitations, and potential harms
- C) Access control cards that restrict who can query an AI model's inference endpoint
- D) Flashcards used in security awareness training for AI concepts

<details>
<summary>Answer</summary>

**B) Standardized documentation describing a model's intended uses, performance characteristics, limitations, and potential harms**

Model cards are standardized documentation that captures a model's intended use cases, performance metrics across demographic groups, known limitations, and potential harms. They are a key AI transparency and accountability artifact.
</details>

---

### Q22. Brittle Content Filtering

A penetration tester identifies that a deployed LLM application returns significantly different responses when the same question is phrased using technical security jargon versus casual language — and that the technical phrasing bypasses certain content filters. Which security control failure does this reveal?

- A) The model lacks differential privacy protections
- B) Inconsistent content filtering — the safety controls are prompt-format-dependent rather than semantically robust
- C) The model is vulnerable to membership inference attacks
- D) The inference endpoint lacks TLS encryption

<details>
<summary>Answer</summary>

**B) Inconsistent content filtering — the safety controls are prompt-format-dependent rather than semantically robust**

This reveals brittle content filtering — the safety controls trigger on surface-level patterns rather than understanding semantic intent. Robust safety controls must be semantically consistent regardless of phrasing.
</details>

---

### Q23. Excessive Agency — LLM with Tool Access

An organization deploys an LLM as an internal security knowledge assistant with access to Jira, Confluence, Slack, and the ability to send emails. A security review determines this configuration poses unacceptable risk. Which OWASP LLM vulnerability is the primary concern?

- A) LLM03 – Training Data Poisoning; retrain the model without Jira data
- B) LLM08 – Excessive Agency; apply least privilege by limiting tool access and requiring human approval for consequential actions
- C) LLM06 – Sensitive Information Disclosure; implement output filtering for PII
- D) LLM04 – Model Denial of Service; implement rate limiting on the assistant's API

<details>
<summary>Answer</summary>

**B) LLM08 – Excessive Agency; apply least privilege by limiting tool access and requiring human approval for consequential actions**

Granting an LLM access to multiple systems with write/send capabilities creates unacceptable autonomous action risk. The remediation is least privilege: grant read-only access where possible, require human approval for consequential actions, and implement action auditing.
</details>

---

### Q24. Checksum Mismatch as Tampering Evidence

Which of the following audit log entries provides the STRONGEST evidence that a model's training data was tampered with after the initial data collection phase?

- A) Unusual inference latency spikes on the production endpoint
- B) A checksum mismatch between the stored training dataset hash and the hash computed at training time, with no corresponding change log entry
- C) Increased model accuracy on the validation set following an unscheduled pipeline run
- D) A new contributor account created in the ML experiment tracking system

<details>
<summary>Answer</summary>

**B) A checksum mismatch between the stored training dataset hash and the hash computed at training time, with no corresponding change log entry**

A checksum mismatch without a corresponding authorized change log entry is direct forensic evidence of unauthorized modification to the training dataset.
</details>

---

### Q25. Container Hardening for AI Inference

A security engineer is hardening an AI inference microservice deployed in Kubernetes. Which set of controls BEST reduces the blast radius if the container is compromised?

- A) Enable GPU acceleration and increase pod memory limits
- B) Apply read-only root filesystem, drop all Linux capabilities, run as non-root, and use a NetworkPolicy to restrict egress to only required endpoints
- C) Deploy the inference service behind a WAF and enable TLS termination
- D) Store model weights in an encrypted Kubernetes secret and mount at runtime

<details>
<summary>Answer</summary>

**B) Apply read-only root filesystem, drop all Linux capabilities, run as non-root, and use a NetworkPolicy to restrict egress to only required endpoints**

Container hardening: read-only root filesystem prevents persistence, dropping capabilities reduces privilege escalation risk, running as non-root limits damage, and NetworkPolicy egress restriction prevents data exfiltration.
</details>

---

### Q26. Cryptographic Signature Verification

An organization wants to verify that a fine-tuned model downloaded from a vendor has not been modified since the vendor published it. Which technique provides the STRONGEST cryptographic assurance?

- A) Running the model on a sample dataset and comparing output accuracy to published benchmarks
- B) Verifying the model artifact against the vendor's published cryptographic signature using their public key
- C) Comparing the model's file size to the published specification
- D) Running the model through a malware scanner before deployment

<details>
<summary>Answer</summary>

**B) Verifying the model artifact against the vendor's published cryptographic signature using their public key**

Cryptographic signature verification using the vendor's public key provides mathematical proof that the model artifact has not been modified since it was signed by the vendor.
</details>

---

### Q27. EU AI Act Classification — Customer Support Routing

A compliance team is documenting AI systems for EU AI Act conformity. The organization uses an AI model to automatically route customer support tickets to departments. How should this system be classified?

- A) Unacceptable risk — automated decision systems that affect individuals are prohibited
- B) High risk — any AI making decisions about individuals requires conformity assessment
- C) Limited or minimal risk — customer support routing has limited impact and likely falls outside high-risk categories
- D) High risk only if the company has more than 500 employees

<details>
<summary>Answer</summary>

**C) Limited or minimal risk — customer support routing has limited impact and likely falls outside high-risk categories**

Under the EU AI Act, high-risk AI systems are specifically defined categories (critical infrastructure, employment, law enforcement, biometrics, etc.). Customer support ticket routing has limited impact on individuals' fundamental rights.
</details>

---

### Q28. Concept Drift

An organization discovers their production ML model's performance has degraded significantly over six months, with increasing false negative rates on new attack patterns. No changes were made to the model. What is the MOST likely cause?

- A) The model weights were modified by a supply chain attack
- B) Concept drift — the statistical distribution of production data has shifted away from the training distribution over time
- C) The inference endpoint is being attacked with adversarial examples
- D) Differential privacy noise accumulation over time has degraded model accuracy

<details>
<summary>Answer</summary>

**B) Concept drift — the statistical distribution of production data has shifted away from the training distribution over time**

Concept drift occurs when the real-world data distribution shifts over time while the deployed model remains static — common in security where attacker TTPs evolve.
</details>

---

### Q29. Shadow Mode Deployment

Which of the following BEST describes 'shadow mode deployment' as a security testing strategy for new AI models?

- A) Deploying a model exclusively in air-gapped environments for initial testing
- B) Running a new model in parallel with the production model on live traffic, logging decisions without acting on them, to compare behavior before cutover
- C) Training a model on anonymized shadow copies of production data
- D) Deploying a duplicate model as a honeypot to detect model extraction attempts

<details>
<summary>Answer</summary>

**B) Running a new model in parallel with the production model on live traffic, logging decisions without acting on them, to compare behavior before cutover**

Shadow mode deployment runs the candidate model on real production traffic in parallel with the production model, logging its decisions without acting on them. This validates model behavior on real-world data patterns before cutover.
</details>

---

### Q30. Shared Service Account Violation (Scenario)

**SCENARIO:** A large bank runs three AI models: a fraud detection model, a credit scoring model, and a customer churn prediction model. The security team discovers all three models share the same service account with broad read access to the customer database, write access to the decision database, and admin access to the model registry. Which finding should the security team prioritize?

- A) The fraud model and credit model should be merged to reduce attack surface
- B) The shared service account violates least privilege and separation of duties — each model should have a dedicated account with only the permissions required for its specific function
- C) The customer database should be replicated to a separate environment for AI access
- D) Admin access to the model registry should be revoked from all service accounts

<details>
<summary>Answer</summary>

**B) The shared service account violates least privilege and separation of duties — each model should have a dedicated account with only the permissions required for its specific function**

Shared service accounts across different AI models with broad permissions violate both least privilege and separation of duties. A compromise of any model's runtime would grant the attacker access to all three models' data and the model registry.
</details>

---

### Q31. Defense in Depth Against Model Extraction

An organization's red team successfully extracts a proprietary NLP model by querying its public API 200,000 times over 30 days. Post-incident, the security team implements output perturbation. What additional control should be implemented?

- A) Retrain the model with differential privacy to make extraction mathematically impossible
- B) Implement anomaly detection on query patterns, rate limiting by API key, and CAPTCHA for high-volume consumers in addition to output perturbation
- C) Make the model API private with certificate-based mutual TLS authentication
- D) Switch from a neural network to a decision tree model which is inherently extraction-resistant

<details>
<summary>Answer</summary>

**B) Implement anomaly detection on query patterns, rate limiting by API key, and CAPTCHA for high-volume consumers in addition to output perturbation**

Defense in depth against model extraction requires layered controls: rate limiting reduces extraction throughput, anomaly detection identifies systematic extraction patterns, and CAPTCHA deters automated querying.
</details>

---

### Q32. API Gateway for AI Inference

What is the primary purpose of implementing an AI model's inference endpoint behind an API gateway with authentication rather than exposing it directly?

- A) To improve model inference performance through caching
- B) To enforce authentication, authorization, rate limiting, input validation, and logging at a centralized boundary before requests reach the model
- C) To enable federated learning across multiple model instances
- D) To apply differential privacy to all model outputs before returning them to clients

<details>
<summary>Answer</summary>

**B) To enforce authentication, authorization, rate limiting, input validation, and logging at a centralized boundary before requests reach the model**

An API gateway provides a centralized security boundary for AI inference endpoints: enforcing authentication, authorization, rate limiting, input validation, and comprehensive logging.
</details>

---

### Q33. Suspicious Model Promotion in MLOps

A security engineer is reviewing MLflow experiment tracking logs and notices that a model with significantly better accuracy than all other candidates was promoted to production from an anonymous experiment run that bypassed the standard peer review process. What security concern does this raise?

- A) The model may have overfitted to the test set, indicating a training data leak
- B) The anomalous promotion bypassing peer review may indicate a supply chain attack — the model may contain backdoors or malicious modifications
- C) Anonymous experiment runs indicate a memory leak in the MLflow tracking server
- D) Better accuracy than peers indicates the model was trained on a larger dataset than permitted

<details>
<summary>Answer</summary>

**B) The anomalous promotion bypassing peer review may indicate a supply chain attack — the model may contain backdoors or malicious modifications**

An anonymous experiment run bypassing standard peer review is a significant red flag for supply chain attack or insider threat. MLOps security requires that all model promotions to production are traceable to authenticated, peer-reviewed pipeline runs with full audit trails.
</details>

---

### Q34. Local Differential Privacy

Which privacy-preserving technique allows a data analyst to compute the average salary in a dataset without learning any individual's salary, by having each participant add random noise to their value before submitting?

- A) Homomorphic encryption
- B) Federated learning
- C) Local differential privacy
- D) Secure multi-party computation

<details>
<summary>Answer</summary>

**C) Local differential privacy**

Local differential privacy (LDP) has each data subject add calibrated random noise to their data locally before sharing. The analyst can compute accurate aggregate statistics while learning nothing about any individual's true value.
</details>

---

### Q35. Defense-in-Depth for LLM Applications

A security team implements AI security controls using a defense-in-depth approach for a customer-facing LLM application. Which layered control stack is MOST comprehensive?

- A) Input length limits -> output caching -> TLS encryption
- B) Input validation and sanitization -> system prompt hardening -> output filtering -> rate limiting -> comprehensive audit logging -> human review for high-risk actions
- C) Authentication -> model signing -> model versioning
- D) CAPTCHA -> WAF -> DDoS protection

<details>
<summary>Answer</summary>

**B) Input validation and sanitization -> system prompt hardening -> output filtering -> rate limiting -> comprehensive audit logging -> human review for high-risk actions**

Defense-in-depth for LLM applications requires controls at every layer: input validation stops injection attempts; system prompt hardening reduces susceptibility to override; output filtering catches harmful responses; rate limiting prevents abuse; audit logging enables forensics; human review provides oversight for consequential actions.
</details>

---

### Q36. Model Owner Accountability (NIST AI RMF GOVERN)

An organization's AI governance policy requires that all production ML models have a designated 'model owner' responsible for ongoing monitoring, retraining decisions, and incident response. Which NIST AI RMF function does this policy PRIMARILY implement?

- A) MAP — contextualizing the model's risks
- B) MEASURE — quantifying model performance
- C) GOVERN — establishing roles, accountability, and organizational policies for responsible AI
- D) MANAGE — treating and mitigating identified risks

<details>
<summary>Answer</summary>

**C) GOVERN — establishing roles, accountability, and organizational policies for responsible AI**

Assigning a designated model owner with defined responsibilities implements the GOVERN function of NIST AI RMF — establishing clear accountability, roles, and organizational policies.
</details>

