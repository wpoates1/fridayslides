# AI for Trust, Transparency & Inclusion: From Global Principles to Practical Controls

## Introduction: The Governance Triad

The rapid integration of Artificial Intelligence, particularly generative AI, into core business functions presents a significant challenge. While the potential for efficiency and innovation is undeniable, it is paralleled by deep-seated concerns about trust, transparency, and fairness. This has created a "Governance Triad" where organizations must simultaneously manage AI at three distinct levels: the **Societal** (navigating a complex web of global regulations), the **Corporate** (aligning AI with firm-level strategy and risk), and the **Technical** (governing the data pipelines and models themselves).

This paper explores these three levels, arguing that effective governance requires moving from high-level principles to practical, auditable frameworks. We will examine the diverging global regulatory landscape, the strategic "trilemma" facing corporate boards, and the practical controls that can build demonstrable trust, using the EDM Council's draft ADAC (AI Data and Analytics Control) framework as a key example of an industry-led, practical solution.

## 1. Regulatory Governance – Societal Level Concerns

We are in a period of intense regulatory divergence. The world's major "AI blocs" are taking fundamentally different approaches, creating a complex compliance map for any international business.

* **The European Union (EU): The "Rights-Based" Regulator**
    The EU AI Act [1] is a comprehensive, horizontal law that categorizes AI systems by risk. "Unacceptable Risk" systems (e.g., social scoring) are banned, while "High-Risk" systems (e.g., credit scoring, hiring) are heavily regulated, requiring massive compliance in data governance, human oversight, and transparency [1]. This is likely to set a global standard via the "Brussels Effect."

* **The United States (US): The "Innovation-First" Market**
    The US has a pro-innovation, market-driven stance, articulated through the NIST AI Risk Management Framework (RMF) [2] and the White House Executive Order on AI [3]. This voluntary (but influential) framework encourages companies to manage risk while letting existing regulators (like the SEC) apply their rules to AI within their sectors.

* **The United Kingdom (UK): The "Pragmatic" Middle-Ground**
    The UK has rejected a single "AI Act," fearing it would stifle innovation [4]. Its policy empowers existing regulators (like the FCA for finance) to apply a set of five core principles (e.g., Safety, Fairness, Accountability) within their own context, allowing for a more flexible, light-touch approach [4].

* **China: The "State-Centric" Controller**
    China employs a state-centric, control-oriented model with iterative, application-specific rules (e.g., on GenAI) [5]. The state is both a heavy-handed regulator and the primary customer, focusing on social stability and content control [5].

### The Key Question for Kenya

Kenya, as a tech importer using US/Chinese models and a service exporter with links to the UK/EU, must navigate this map. A heavy-handed EU-style law could stifle its world-leading fintech sector (M-PESA, Tala). The likely path is a "hybrid" or "straddle" approach: a pragmatic, risk-based framework that draws on EU principles (especially on data and bias, given Kenya's Data Protection Act of 2019 [6]) but applies them with the flexibility of the UK model [4].

## 2. Corporate Governance – Firm-Level Concerns

For a bank's board, AI governance is not just a compliance problem; it's a strategic "trilemma" [7].

1.  **Commercial Opportunity:** The fear of not acting. "If we don't use AI for credit scoring, our competitors will be faster, cheaper, and more accurate, and we will lose market share."
2.  **Reputation Risk (Customers):** The fear of public failure. "If our AI is found to be biased, it will be on the front page of The Standard." This is about public trust.
3.  **Regulatory Risk (Regulator):** The fear of non-compliance. "If the CBK audits our model and we cannot explain why it denied a loan, we will face fines." This requires Explainability (XAI) and Model Risk Management (MRM), often building on existing guidance [8].

This trilemma raises the structural question: how to organize governance? While some create "AI Ethics Councils," a more robust approach is to embed accountability directly into existing regimes, (e.g., the UK's Senior Managers and Certification Regime - SMCR) [9].

This is where a practical framework becomes essential. Trust cannot be an abstract principle; it must be an engineering and governance discipline. The EDM Council's ADAC framework provides the practical, auditable steps to manage this trilemma.



* **Addressing "Process Distrust" (The "Should We?"):** Distrust often comes from the process itself, which can feel like a "black box." **ADAC Component 2: Data & Analytics Ethics** provides a direct control. It mandates a formal, documented ethical review *before* development begins, forcing the business to answer, "Even if we *can* build this, *should* we?" This prevents uses of AI that are "creepy" or overreaching and builds public trust.

* **Addressing "Outcome Distrust" (The "Who is Responsible?"):** **ADAC Component 6: AI Governance** provides the structure for accountability. It links directly to the SMCR concept by defining clear lines of responsibility [9]. It calls for a "Model Inventory" or "Registry," which acts as a central, auditable "single source of truth" logging every model, its risks, its owner, and its validation status. This turns the abstract goal of "accountability" into a concrete, auditable system.

## 3. 'Market' Governance – Technical & Model-Level Concerns

Trust at the corporate level must be built on a foundation of technical-level controls. This is where governance moves from "what we want" to "what we do." Here again, a practical framework like ADAC connects high-level goals to on-the-ground execution.

### 3.1. Governing the Data Pipeline (The Foundation)

You cannot have trustworthy AI without trustworthy data. Distrust in AI often starts with distrust in the data. **ADAC Component 3: Data Sourcing & Handling** provides a practical checklist for this.

* **Data Provenance & Lineage:** The framework demands that data be traceable to its origin. This is a non-negotiable for any regulator.
* **Data Quality Controls:** This moves beyond "garbage in, garbage out" by requiring automated, measurable checks for data accuracy, completeness, and timeliness.
* **Privacy & Consent:** It mandates that data handling be aligned with privacy notices and consent given at collection, directly linking to regulations like Kenya's DPA [6].

Furthermore, **Privacy-Preserving Technologies (PETs)** are the technical tools to achieve these controls. They are no longer academic; they are practical solutions for sharing data while building trust.
* **Federated Learning:** Allows a central model to be trained (e.g., on fraud detection) without the raw, sensitive data ever leaving each bank's secure servers.
* **Differential Privacy:** Adds statistical "noise" to data before it's shared, making it impossible to re-identify any single individual.

### 3.2. Governing the Model (The Application)

Once the data is governed, the model itself must be. **ADAC Component 4: Model Development & Validation** turns abstract goals like "transparency" into concrete metrics.

* **Validation Beyond Accuracy:** ADAC mandates that validation *must* include:
    * **Fairness Indicators (Metric):** Actively testing the model’s outcomes across different protected demographics to *quantify* bias. This becomes a key go/no-go metric.
    * **Interpretability/Explainability (Metric):** Requiring the validation process to assess *why* a model is making its decisions (Explainability/XAI), not just *what* it decides.
    * **Data Lineage (Metric):** Connecting the final model version back to the *exact* data version it was trained on, which is essential for auditing.
* **"Fit-for-Purpose" Testing:** This requires a formal assessment of the model's robustness against real-world, "dirty" data, not just the clean training set.

This governance challenge is amplified by generative AI. Base LLMs are often "stochastic parrots" [10]—probabilistic and prone to "hallucinating" (fabricating information). The old method of "prompting and praying" with a long, brittle metaprompt is not auditable or reliable.

The new, robust approach is to "program" the LLM. Frameworks like **DSPy** from Stanford [11] separate the program logic from the LLM. A developer *declares* the steps, and a *compiler* tests hundreds of prompts to find the most reliable combination [11]. This turns a brittle prompt into a robust, optimized, and verifiable program. This is technical governance in action—it is a systematic, auditable, and testable engineering discipline for managing the AI, which can be documented and shown to a regulator.

## 4. Conclusion

Building trust, transparency, and inclusion in AI requires a multi-layered approach. The global regulatory landscape provides the high-level "rules of the road." But for an organization, real trust is built from the inside out. It starts at the corporate level by managing the strategic trilemma of opportunity, reputation, and regulation. It is then operationalized through practical, auditable frameworks like the EDM Council's ADAC, which provide specific controls for data ethics and governance. Finally, this framework is executed at the technical level through robust data pipelines, modern privacy-preserving technologies, and new engineering disciplines that can govern even the most complex generative models.

---
## References

1.  European Commission. (2024). *Artificial Intelligence Act*. (Final text adopted by the European Parliament, March 2024).
2.  National Institute of Standards and Technology (NIST). (2024). *The AI Risk Management Framework (AI RMF 1.0)*. U.S. Department of Commerce.
3.  The White House. (2023). *Executive Order on the Safe, Secure, and Trustworthy Development and Use of Artificial Intelligence*.
4.  UK Department for Science, Innovation and Technology. (2024). *A pro-innovation approach to AI regulation: government response*. (February 2024).
5.  Kania, E., & Webster, G. (2024). "China's AI Regulations and How They Get Made." Stanford University Cyber Policy Center.
6.  Government of Kenya. (2019). *The Data Protection Act, 2019*.
7.  World Economic Forum. (2023). *Governing AI: A Framework for Boards and C-Suites*.
8.  U.S. Federal Reserve System. (2011). *SR 11-7: Guidance on Model Risk Management*.
9.  Financial Conduct Authority (FCA). (2024). *AI in financial services: Feedback on Discussion Paper DP22/4*.
10. Bender, E. M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). "On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?" *FAccT '21: Proceedings of the 2021 ACM Conference on Fairness, Accountability, and Transparency*.
11. Khattab, O., Singhvi, A., El-Arini, K., Potts, C., & Zaharia, M. (2023). "DSPy: Compiling Declarative Language Model Calls into Self-Improving Pipelines." *arXiv:2310.03714*.
