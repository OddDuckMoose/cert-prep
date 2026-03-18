# Domain 4 — AI-Assisted SecOps (~17%)

## Bank 1

### Q1. AI-Based Alert Triage

A SOC team is evaluating AI tools to reduce alert fatigue. Their SIEM currently generates 10,000 alerts per day, of which analysts confirm only 200 are true positives. Which AI application would MOST directly address this problem?

- A) Using an LLM to generate threat hunting queries
- B) Deploying AI-based alert triage to prioritize and de-duplicate alerts using behavioral context
- C) Training a generative AI model on past incident reports to draft response playbooks
- D) Implementing NLP-based log parsing to normalize event formats

<details>
<summary>Answer</summary>

**B) Deploying AI-based alert triage to prioritize and de-duplicate alerts using behavioral context**

AI-based alert triage uses ML models to score, correlate, and prioritize alerts based on behavioral context, reducing false positives before analysts see them. This directly addresses alert fatigue.
</details>

---

### Q2. UEBA

What does UEBA (User and Entity Behavior Analytics) primarily use to detect threats?

- A) Signature-based pattern matching against known threat indicators
- B) Static analysis of executable files and scripts
- C) Machine learning to establish behavioral baselines and flag statistically anomalous deviations
- D) Threat intelligence feeds correlated with firewall logs

<details>
<summary>Answer</summary>

**C) Machine learning to establish behavioral baselines and flag statistically anomalous deviations**

UEBA uses ML to build behavioral baselines for users and entities (servers, applications) and then flags statistically anomalous deviations from those baselines. Unlike signature-based tools, UEBA can detect novel insider threats and unknown attacks.
</details>

---

### Q3. SOAR with AI-Driven Playbooks

An organization wants to use AI to automate the initial containment steps during a ransomware incident — specifically, to automatically isolate affected hosts and block C2 IP addresses within seconds of detection. Which technology category best describes this capability?

- A) AI-enhanced SIEM for log correlation
- B) SOAR (Security Orchestration, Automation, and Response) with AI-driven playbook execution
- C) NLP-based threat intelligence aggregation
- D) Explainable AI (XAI) for incident documentation

<details>
<summary>Answer</summary>

**B) SOAR (Security Orchestration, Automation, and Response) with AI-driven playbook execution**

SOAR platforms orchestrate automated response actions — like host isolation and firewall rule changes — triggered by detection events. AI enhances SOAR by enabling dynamic decision-making in playbooks rather than purely rule-based triggers.
</details>

---

### Q4. Unsupervised Anomaly Detection for APT

A threat hunter is using an AI-powered platform to analyze six months of network flow data looking for signs of a long-term APT. The AI identifies a cluster of hosts that periodically communicate with an external IP at 3 AM with consistent 847-byte payloads — behavior never flagged by existing rules. Which AI capability enabled this discovery?

- A) Supervised classification of known malware families
- B) Generative AI drafting of threat hunting hypotheses
- C) Unsupervised anomaly detection and behavioral clustering
- D) Signature-based intrusion detection enhanced with ML

<details>
<summary>Answer</summary>

**C) Unsupervised anomaly detection and behavioral clustering**

This scenario describes unsupervised anomaly detection and clustering — the AI found unusual patterns in unlabeled data without being given examples of what to look for.
</details>

---

### Q5. AI Limitations in SecOps

Which of the following represents a significant LIMITATION of using AI in security operations that analysts must account for when building AI-assisted workflows?

- A) AI cannot process more than 1,000 log events per second
- B) AI models can be fooled by adversarial inputs and may produce unexplainable decisions, requiring human oversight
- C) AI tools are incompatible with cloud-based SIEM platforms
- D) AI-based detection requires signature updates like traditional antivirus

<details>
<summary>Answer</summary>

**B) AI models can be fooled by adversarial inputs and may produce unexplainable decisions, requiring human oversight**

Two critical AI limitations in SecOps: (1) adversarial vulnerability — AI models can be fooled by crafted inputs; and (2) explainability — black-box model decisions are difficult to document in incident reports.
</details>

---

### Q6. Detection and Analysis Phase (NIST IR)

A security analyst uses an AI tool that automatically enriches alerts with threat intelligence, identifies the affected user's role and data access, assesses the potential blast radius, and suggests containment steps. Which stage of the incident response lifecycle does this capability PRIMARILY support?

- A) Preparation
- B) Detection and Analysis
- C) Post-Incident Activity
- D) Recovery

<details>
<summary>Answer</summary>

**B) Detection and Analysis**

Automated alert enrichment, user context, blast radius assessment, and containment suggestions all fall within the Detection and Analysis phase (NIST IR lifecycle).
</details>

---

### Q7. Fine-Tuning NLP for New Log Sources

An organization's AI-enhanced SIEM uses NLP to parse and normalize unstructured log data from 50+ different source types. A new log source generates entries in an unusual format, and the NLP model begins misclassifying these events, causing critical alerts to be missed. What is the MOST appropriate response?

- A) Disable the new log source until a traditional parser is available
- B) Retrain or fine-tune the NLP model with representative samples from the new log source and validate before production deployment
- C) Increase the alert threshold to compensate for the misclassification rate
- D) Replace the NLP model with signature-based parsing for all log sources

<details>
<summary>Answer</summary>

**B) Retrain or fine-tune the NLP model with representative samples from the new log source and validate before production deployment**

When an NLP model encounters an out-of-distribution log format, the appropriate ML response is to fine-tune the model with labeled examples from the new source and validate performance before production deployment.
</details>

---

### Q8. Low-and-Slow Evasion

A red team discovers that the target organization's AI-based network anomaly detection system can be bypassed by slowly increasing exfiltration rate over 72 hours rather than performing bulk data transfer at once. Which concept does this bypass technique exploit?

- A) The model's reliance on static thresholds rather than learned behavioral baselines
- B) The model's inability to process encrypted traffic
- C) Membership inference vulnerabilities in the detection model
- D) Model hallucination under high-load conditions

<details>
<summary>Answer</summary>

**A) The model's reliance on static thresholds rather than learned behavioral baselines**

This is a low-and-slow evasion technique that exploits detection models tuned on short time windows or static thresholds. It highlights a key limitation of AI anomaly detectors that don't account for long-duration behavioral trends.
</details>

---

### Q9. Explainable AI (XAI) — SHAP and LIME

Which of the following BEST describes the value of explainable AI (XAI) techniques like SHAP and LIME specifically in a security operations context?

- A) They improve model accuracy by reducing false positive rates
- B) They allow analysts to understand why a model flagged an alert, enabling better investigation and defensible documentation
- C) They encrypt model decisions to prevent adversarial exploitation
- D) They automatically generate SOAR playbooks from model outputs

<details>
<summary>Answer</summary>

**B) They allow analysts to understand why a model flagged an alert, enabling better investigation and defensible documentation**

XAI methods like SHAP and LIME identify which features most influenced a specific model decision. In SecOps, this enables analysts to understand why an alert was generated, validate the finding, and document the reasoning in incident reports.
</details>

---

### Q10. Precision vs. Recall Tradeoff (Scenario)

**SCENARIO:** A financial services firm's AI fraud detection system flags 500 transactions per day as potentially fraudulent and routes them to analysts for review. Analysis shows the model has a 15% false positive rate. An analyst proposes lowering the detection threshold to reduce false positives. The risk team pushes back. Which tradeoff does this tension represent?

- A) Precision vs. recall — lowering the threshold increases precision but reduces recall, potentially missing more actual fraud
- B) Model accuracy vs. computational efficiency
- C) Supervised vs. unsupervised learning approaches
- D) Data poisoning risk vs. evasion risk

<details>
<summary>Answer</summary>

**A) Precision vs. recall — lowering the threshold increases precision but reduces recall, potentially missing more actual fraud**

This is a precision-recall tradeoff. Lowering the detection threshold (making the model more conservative) increases precision (fewer false positives) but reduces recall (more false negatives — missed fraud).
</details>

---

## Bank 2

### Q11. Named Entity Recognition (NER) for CTI

A threat intelligence team uses an NLP model to automatically extract threat actor names, malware families, TTPs, and targeted sectors from 500 unstructured threat intelligence reports per day. Which NLP task BEST describes what the model is performing?

- A) Sentiment analysis
- B) Named entity recognition (NER) for cyber threat intelligence
- C) Text summarization
- D) Semantic similarity scoring

<details>
<summary>Answer</summary>

**B) Named entity recognition (NER) for cyber threat intelligence**

NER identifies and classifies named entities in text — in this case, cyber-specific entities like threat actor names, malware families, TTPs, and sectors.
</details>

---

### Q12. UEBA for Insider Threat Detection

A SOC implements an AI model that analyzes user behavior and flags a finance employee who has been downloading large files from SharePoint at 11 PM on weekdays — behavior that deviates significantly from their established baseline. The model correctly identifies this as data exfiltration preparation. Which AI security application does this represent?

- A) Signature-based intrusion detection enhanced with ML
- B) UEBA detecting insider threat through behavioral anomaly detection
- C) AI-powered vulnerability scanning of the SharePoint environment
- D) NLP analysis of the employee's communication patterns

<details>
<summary>Answer</summary>

**B) UEBA detecting insider threat through behavioral anomaly detection**

This is UEBA — the model has established a behavioral baseline for the user and flagged a statistically significant deviation. UEBA is particularly effective against insider threats because it detects anomalous behavior rather than requiring known attack signatures.
</details>

---

### Q13. Graph-Based ML for Lateral Movement

An organization wants to use AI to continuously monitor their network for signs of lateral movement by correlating authentication events, network connections, and process execution across thousands of endpoints in real time. Which AI/ML approach is MOST appropriate?

- A) Supervised classification of individual events as malicious or benign
- B) Graph-based ML analyzing relationships between entities to detect anomalous movement patterns across the network
- C) Generative AI summarizing daily network activity reports
- D) Regression models predicting network bandwidth utilization

<details>
<summary>Answer</summary>

**B) Graph-based ML analyzing relationships between entities to detect anomalous movement patterns across the network**

Graph-based ML is ideal for lateral movement detection because it models relationships between entities (users, machines, processes) rather than analyzing individual events in isolation.
</details>

---

### Q14. Over-Automation Risk

A SOAR platform's AI-driven playbook is configured to automatically block any IP address that generates more than 50 failed authentication attempts in 5 minutes. During a major product launch, legitimate users from a corporate partner experience mass authentication failures due to a directory sync issue and all their IPs are automatically blocked. Which risk does this scenario illustrate?

- A) The SOAR platform is misconfigured and vulnerable to prompt injection
- B) Over-automation risk — AI-driven automated response without sufficient context or human oversight can cause operational impact
- C) The authentication system is vulnerable to a denial-of-service attack
- D) The AI model has been poisoned to incorrectly classify partner traffic

<details>
<summary>Answer</summary>

**B) Over-automation risk — AI-driven automated response without sufficient context or human oversight can cause operational impact**

This illustrates over-automation risk — automated AI-driven responses acting without contextual understanding or human oversight can cause significant operational impact. Best practice requires contextual enrichment and human-in-the-loop approval for high-impact automated actions.
</details>

---

### Q15. LLMs for Threat Hunting (Human-in-the-Loop)

A security operations team wants to use generative AI to accelerate threat hunting. Which of the following represents the MOST appropriate and effective use of an LLM in this workflow?

- A) Trusting LLM-generated threat hypotheses as confirmed intelligence without analyst validation
- B) Using the LLM to generate structured threat hunting queries and hypotheses based on analyst-provided context, with all results validated by human analysts before action
- C) Automating LLM-based threat hunting without human review to maximize speed
- D) Having the LLM access production systems directly to execute hunting queries

<details>
<summary>Answer</summary>

**B) Using the LLM to generate structured threat hunting queries and hypotheses based on analyst-provided context, with all results validated by human analysts before action**

LLMs excel at generating structured query language, hypothesis formation, and summarizing research — but their outputs must be validated by human analysts before execution or action. Human-in-the-loop validation is non-negotiable.
</details>

---

### Q16. Operational SOC Metrics for AI

Which metric BEST measures the operational effectiveness of an AI-based alert triage system in a SOC environment?

- A) Model training accuracy on the validation dataset
- B) Mean time to detection (MTTD) and false positive rate reduction compared to the pre-AI baseline
- C) Number of training epochs required to converge
- D) GPU utilization percentage during inference

<details>
<summary>Answer</summary>

**B) Mean time to detection (MTTD) and false positive rate reduction compared to the pre-AI baseline**

Operational SOC metrics measure real-world outcomes, not training performance. MTTD reduction shows the AI is helping analysts find threats faster. False positive rate reduction demonstrates improved signal-to-noise ratio.
</details>

---

### Q17. AI-Assisted Vulnerability Prioritization (EPSS)

A security architect is evaluating AI-assisted vulnerability management tools. One tool uses ML to predict the exploitability of newly disclosed CVEs based on historical exploitation data, code characteristics, and threat actor activity. What is the PRIMARY security benefit of this capability?

- A) It eliminates the need for manual penetration testing
- B) It enables risk-based prioritization of patching, focusing resources on vulnerabilities most likely to be exploited
- C) It automatically generates and applies patches without analyst review
- D) It replaces CVSS scoring as the authoritative vulnerability severity standard

<details>
<summary>Answer</summary>

**B) It enables risk-based prioritization of patching, focusing resources on vulnerabilities most likely to be exploited**

ML-based exploitability prediction (like EPSS) enables risk-based prioritization: organizations can focus limited patching resources on the small percentage of CVEs that are actually likely to be exploited in the wild.
</details>

---

### Q18. Spurious Correlation — LOLBins

During a post-incident review, a security team identifies that their AI-based endpoint detection system missed the initial compromise because the attacker used a legitimate signed binary (LOLBin) for execution. The AI model had learned to trust signed binaries based on training data. Which AI limitation contributed to this failure?

- A) The model was overfitting to adversarial examples during training
- B) The model learned a spurious correlation (signed = trusted) that attackers could exploit by abusing legitimate signed tools
- C) The model suffered from gradient vanishing, reducing detection sensitivity
- D) The model was unable to process binary file formats

<details>
<summary>Answer</summary>

**B) The model learned a spurious correlation (signed = trusted) that attackers could exploit by abusing legitimate signed tools**

The model learned a spurious correlation — 'signed binary = legitimate' — that was exploited by attackers using LOLBins. Models learn statistical patterns from training data, and attackers can craft TTPs that exploit those learned correlations.
</details>

---

### Q19. Unsupervised Anomaly Detection for Cloud Misconfigurations

A CISO wants to implement AI for continuous monitoring of cloud environments at scale, specifically to detect misconfiguration patterns that traditional CSPM tools miss through static rules. Which AI approach is MOST appropriate?

- A) Supervised classification trained on known misconfigurations only
- B) Anomaly detection using unsupervised ML to identify deviations from established baseline configuration patterns
- C) Generative AI to create new cloud configurations based on security best practices
- D) Reinforcement learning to automatically remediate misconfigurations

<details>
<summary>Answer</summary>

**B) Anomaly detection using unsupervised ML to identify deviations from established baseline configuration patterns**

Unsupervised anomaly detection is most appropriate because misconfigurations are diverse and novel — supervised models would miss unknown configuration risks not seen in training.
</details>

---

### Q20. AI as Force Multiplier (Scenario)

**SCENARIO:** A mature SOC has deployed AI-enhanced threat detection across their SIEM, EDR, and network monitoring tools. Despite high investment, a red team exercise reveals that a determined APT still successfully dwells for 23 days before detection. The CISO asks what this result demonstrates about AI-assisted SecOps. Which answer BEST represents an accurate assessment?

- A) All AI security tools are ineffective and should be replaced with traditional signature-based tools
- B) AI enhances detection capabilities significantly but does not eliminate the need for threat hunting, proactive TTPs-based detection, and adversarial simulation exercises
- C) The red team must have used AI-powered evasion tools specifically designed to defeat ML-based detection
- D) 23-day dwell time proves the AI models have been poisoned by the red team

<details>
<summary>Answer</summary>

**B) AI enhances detection capabilities significantly but does not eliminate the need for threat hunting, proactive TTPs-based detection, and adversarial simulation exercises**

AI-enhanced SecOps substantially improves detection but does not guarantee elimination of dwell time against sophisticated adversaries. AI is a force multiplier, not a complete replacement for proactive security programs.
</details>

