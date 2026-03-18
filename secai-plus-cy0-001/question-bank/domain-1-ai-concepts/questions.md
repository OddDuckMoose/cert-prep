# Domain 1 — Basic AI Concepts Related to Cybersecurity (17%)

## Bank 1

### Q1. Overfitting in Intrusion Detection

A security team is evaluating an AI model that was trained on historical network logs to detect intrusions. The model performs well on the training data but fails to identify novel attack patterns not seen during training. Which machine learning concept best describes this limitation?

- A) Underfitting
- B) Overfitting
- C) Reinforcement learning bias
- D) Feature drift

<details>
<summary>Answer</summary>

**B) Overfitting**

Overfitting occurs when a model learns the training data too closely — including its noise — and fails to generalize to new, unseen data. A model that performs well in training but poorly on novel inputs is a textbook case of overfitting.
</details>

---

### Q2. Neural Network Architecture for Sequential Data

Which neural network architecture is most appropriate for processing sequential data such as network log entries where temporal context matters?

- A) Convolutional Neural Network (CNN)
- B) Generative Adversarial Network (GAN)
- C) Recurrent Neural Network (RNN)
- D) Decision Tree

<details>
<summary>Answer</summary>

**C) Recurrent Neural Network (RNN)**

RNNs (and their variants like LSTMs) are designed for sequential data where order and temporal context matter. CNNs are optimized for spatial data like images. GANs generate synthetic data. Decision trees handle tabular classification.
</details>

---

### Q3. RAG for Proprietary Threat Intelligence

An organization wants to deploy a large language model (LLM) for internal security queries but needs it to answer questions grounded in their proprietary threat intelligence database without retraining the model. Which technique best addresses this requirement?

- A) Fine-tuning
- B) Transfer learning
- C) Retrieval-Augmented Generation (RAG)
- D) Federated learning

<details>
<summary>Answer</summary>

**C) Retrieval-Augmented Generation (RAG)**

RAG allows an LLM to retrieve relevant documents from an external knowledge base at inference time, grounding responses in proprietary or up-to-date data without the cost of retraining. Fine-tuning modifies model weights and requires retraining on new data.
</details>

---

### Q4. Embeddings in NLP

What term describes the numerical vector representation of a word or phrase that captures its semantic meaning and enables similarity comparisons in NLP models?

- A) Token
- B) Embedding
- C) Hyperparameter
- D) Gradient

<details>
<summary>Answer</summary>

**B) Embedding**

An embedding is a dense numerical vector that encodes the semantic meaning of text. Similar words have vectors that are close together in vector space. Tokens are raw input units (words/subwords). Hyperparameters configure training. Gradients drive weight updates.
</details>

---

### Q5. Data Poisoning Attack Target

A machine learning pipeline takes raw packet captures, extracts features such as byte frequencies and connection durations, trains a classifier, and deploys it to a production inference endpoint. Which phase of this pipeline would a data poisoning attack most directly target?

- A) Inference endpoint
- B) Feature extraction
- C) Training data collection
- D) Model deployment

<details>
<summary>Answer</summary>

**C) Training data collection**

Data poisoning attacks target the training data collection phase by injecting malicious or mislabeled samples so the model learns incorrect behaviors. Evasion attacks target the inference endpoint. Feature extraction and deployment are downstream phases.
</details>

---

### Q6. Supervised vs. Unsupervised Learning

Which of the following statements BEST describes the difference between supervised and unsupervised learning in a security context?

- A) Supervised learning requires labeled data; unsupervised learning finds patterns in unlabeled data
- B) Supervised learning is faster; unsupervised learning is more accurate
- C) Supervised learning detects known threats; unsupervised learning cannot be used for anomaly detection
- D) Supervised learning requires GPUs; unsupervised learning runs on CPUs only

<details>
<summary>Answer</summary>

**A) Supervised learning requires labeled data; unsupervised learning finds patterns in unlabeled data**

Supervised learning uses labeled examples (e.g., known malicious vs. benign traffic) to train a classifier. Unsupervised learning finds patterns in unlabeled data — making it well-suited for anomaly detection where 'normal' is the only label available.
</details>

---

### Q7. LLM Hallucination

An LLM security assistant confidently states that a CVE was patched in 2023 but the security team's research shows it was actually patched in 2024. What AI phenomenon does this behavior BEST represent?

- A) Model inversion
- B) Prompt injection
- C) Hallucination
- D) Adversarial evasion

<details>
<summary>Answer</summary>

**C) Hallucination**

Hallucination refers to an LLM generating plausible-sounding but factually incorrect output. This is a significant risk when using LLMs in security contexts where precision matters. The model has not been attacked — it is simply generating incorrect information with high confidence.
</details>

---

### Q8. Temperature in LLMs

Which of the following BEST describes the role of temperature in large language model output?

- A) Controls the maximum number of tokens the model can generate
- B) Determines the computational resources allocated to inference
- C) Controls the randomness and creativity of model outputs
- D) Sets the threshold for classifying outputs as malicious

<details>
<summary>Answer</summary>

**C) Controls the randomness and creativity of model outputs**

Temperature is a parameter that controls output randomness. A low temperature (near 0) makes the model more deterministic and conservative. A high temperature increases diversity and creativity. It does not affect token limits or resource allocation.
</details>

---

### Q9. Distribution Shift

An organization trains a sentiment analysis model using customer emails. The model learns that emails mentioning 'invoice' are 90% likely to be neutral because most invoices in the training set happened to come from a single low-volume period. This results in poor production performance. What ML problem does this describe?

- A) Model inversion
- B) Distribution shift
- C) Membership inference
- D) Gradient explosion

<details>
<summary>Answer</summary>

**B) Distribution shift**

Distribution shift (also called dataset shift) occurs when the statistical properties of training data differ from production data. The model learned a spurious correlation that does not hold in the real distribution.
</details>

---

### Q10. Transformer Architecture Advantage

Which of the following BEST describes a transformer architecture's key advantage over earlier RNN-based models for NLP tasks?

- A) Transformers require less training data than RNNs
- B) Transformers process sequences in parallel using attention mechanisms, enabling better context capture
- C) Transformers are only used for image classification tasks
- D) Transformers eliminate the need for tokenization

<details>
<summary>Answer</summary>

**B) Transformers process sequences in parallel using attention mechanisms, enabling better context capture**

Transformers use self-attention mechanisms that process all tokens in a sequence simultaneously, capturing long-range dependencies more effectively than RNNs which process tokens sequentially. This parallelism also enables efficient GPU utilization during training.
</details>

---

## Bank 2

### Q11. Temporal Leakage and Overfitting

A data science team discovers their intrusion detection model achieves 99% accuracy on the test set but only 54% accuracy in production. Investigation reveals the test set was randomly sampled from the same time window as training data, while production data comes from a later period with evolved attacker behavior. Which problem does this BEST describe?

- A) Overfitting to the training distribution with temporal leakage in the test set
- B) Underfitting due to insufficient model complexity
- C) Class imbalance causing the model to always predict the majority class
- D) Gradient vanishing in the deep layers of the network

<details>
<summary>Answer</summary>

**A) Overfitting to the training distribution with temporal leakage in the test set**

This describes temporal leakage — the test set was drawn from the same distribution as training data, so it didn't reveal the model's inability to generalize to future data. In security, where attacker behavior evolves, this is a critical evaluation mistake.
</details>

---

### Q12. Reinforcement Learning in Security

Which of the following BEST describes reinforcement learning and a realistic security application of this approach?

- A) Learning from labeled examples; used to classify malware families
- B) Learning patterns in unlabeled data; used for network anomaly detection
- C) Learning by receiving rewards or penalties from an environment; used to train autonomous penetration testing agents
- D) Learning from a pre-trained model; used to adapt threat intelligence models to new environments

<details>
<summary>Answer</summary>

**C) Learning by receiving rewards or penalties from an environment; used to train autonomous penetration testing agents**

Reinforcement learning trains an agent to take actions in an environment to maximize cumulative reward. In security, this maps to autonomous penetration testing agents that explore networks and discover vulnerabilities through trial and reward feedback.
</details>

---

### Q13. Transfer Learning via Fine-Tuning

A security team deploys a pre-trained BERT model and fine-tunes it on their internal security incident reports to classify ticket severity. Which machine learning technique does this represent?

- A) Federated learning
- B) Transfer learning via fine-tuning
- C) Unsupervised clustering
- D) Generative adversarial training

<details>
<summary>Answer</summary>

**B) Transfer learning via fine-tuning**

Transfer learning reuses a model trained on a large general dataset (BERT trained on massive text corpora) and fine-tunes it on a smaller domain-specific dataset. This is highly effective in security NLP tasks where labeled data is scarce but pre-trained representations are powerful.
</details>

---

### Q14. Context Window

In the context of large language models, what does 'context window' refer to?

- A) The maximum number of layers in the transformer architecture
- B) The maximum number of tokens the model can process as input and output in a single inference call
- C) The time window during which the model's training data was collected
- D) The security boundary separating user prompts from system instructions

<details>
<summary>Answer</summary>

**B) The maximum number of tokens the model can process as input and output in a single inference call**

The context window is the maximum number of tokens an LLM can process at once — encompassing both the input (prompt, conversation history, retrieved documents) and the output (generated response).
</details>

---

### Q15. Generative vs. Discriminative Models

Which statement BEST distinguishes a generative AI model from a discriminative AI model in a security context?

- A) Generative models classify inputs into categories; discriminative models generate new data
- B) Generative models learn the data distribution and can create new samples; discriminative models learn decision boundaries between classes
- C) Generative models require labeled data; discriminative models do not
- D) Generative models are always more accurate than discriminative models for threat detection

<details>
<summary>Answer</summary>

**B) Generative models learn the data distribution and can create new samples; discriminative models learn decision boundaries between classes**

Generative models (GANs, VAEs, LLMs) learn the underlying data distribution and can produce new samples. Discriminative models (classifiers) learn to distinguish between classes — better suited for malware classification and anomaly detection.
</details>

---

### Q16. Semantic Similarity in Embeddings

A threat intelligence team uses a word embedding model where 'ransomware', 'encryption', and 'extortion' cluster closely in vector space, while 'patch' and 'vulnerability' cluster separately. What property of embeddings does this demonstrate?

- A) Token frequency normalization
- B) Semantic similarity encoding — words with related meanings have similar vector representations
- C) Positional encoding for transformer attention
- D) Gradient-based feature importance scoring

<details>
<summary>Answer</summary>

**B) Semantic similarity encoding — words with related meanings have similar vector representations**

Word embeddings encode semantic relationships — words used in similar contexts have similar vector representations. This allows NLP models to understand conceptual relationships, enabling better threat intelligence clustering, incident report analysis, and entity extraction.
</details>

---

### Q17. Precision vs. Recall in SOC

An organization evaluates two malware classifiers. Model A has 95% precision and 60% recall. Model B has 70% precision and 92% recall. For a SOC where missing actual malware is a critical failure, which model is preferable and why?

- A) Model A, because higher precision means fewer false positives and less analyst workload
- B) Model B, because higher recall means fewer false negatives — actual malware is less likely to be missed
- C) Model A, because precision is always more important than recall in security
- D) Model B, because accuracy is determined solely by recall in binary classification

<details>
<summary>Answer</summary>

**B) Model B, because higher recall means fewer false negatives — actual malware is less likely to be missed**

Recall measures the proportion of actual positives (real malware) that the model correctly identifies. Low recall means actual threats are missed — the worst outcome in a SOC. Model B's 92% recall makes it preferable despite more false positives.
</details>

---

### Q18. Attention Mechanism in Transformers

Which of the following BEST describes the purpose of the attention mechanism in transformer-based models?

- A) To reduce model size by pruning low-importance weights
- B) To allow the model to weigh the relevance of different positions in the input sequence when generating each output token
- C) To encrypt attention scores to prevent model inversion attacks
- D) To normalize gradient updates during training to prevent vanishing gradients

<details>
<summary>Answer</summary>

**B) To allow the model to weigh the relevance of different positions in the input sequence when generating each output token**

The self-attention mechanism allows transformers to weigh the relevance of every input token relative to every other token when processing a sequence. This enables the model to capture long-range dependencies far more effectively than RNNs.
</details>

---

### Q19. False Negative Rate

A CISO asks why the organization's AI-based phishing URL detector has high accuracy but the security team still reports significant phishing breaches. Which metric would provide the MOST insight into this discrepancy?

- A) Model training loss and validation loss curves
- B) False negative rate — the proportion of actual phishing URLs the model failed to detect
- C) Model inference latency and throughput capacity
- D) Precision — the proportion of flagged URLs that were actually phishing

<details>
<summary>Answer</summary>

**B) False negative rate — the proportion of actual phishing URLs the model failed to detect**

If phishing emails are getting through, the issue is false negatives — actual phishing URLs classified as benign. The false negative rate (1 - recall) directly measures this. High overall accuracy can mask poor recall in imbalanced datasets where benign URLs vastly outnumber phishing URLs.
</details>

---

### Q20. Security Risks of Public Foundation Model APIs

What is the PRIMARY security concern with using a publicly available foundation model API for processing internal security incident reports?

- A) Foundation models are less accurate than custom-trained models for security tasks
- B) Sensitive incident data sent to third-party APIs may be retained, used for training, or exposed in a data breach
- C) Foundation models cannot process structured log data formats
- D) API-based models have higher latency than locally deployed models, slowing incident response

<details>
<summary>Answer</summary>

**B) Sensitive incident data sent to third-party APIs may be retained, used for training, or exposed in a data breach**

Sending sensitive incident data — containing vulnerability details, affected systems, and attack TTPs — to third-party LLM APIs introduces data privacy and confidentiality risks. The provider may retain data for training, and the data may be exposed if the provider is breached.
</details>

