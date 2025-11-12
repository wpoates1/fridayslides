# Presentation Research: "AI for Trust, Transparency & Inclusion"

### 1. Regulatory Governance – Societal Level Concerns

**Slide Title:** The Global AI Rulebook: A Diverging Map

**Core Idea:** We are in a period of intense regulatory divergence. The world's major "AI blocs" are taking fundamentally different approaches, creating a complex compliance map for any international business, including Kenyan banks that may use US models, have EU/UK partners, or follow global compliance standards.

**Research & Key Points:**

* **The European Union (EU): The "Rights-Based" Regulator**
    * **Framework:** The **EU AI Act** [1].
    * **Approach:** A comprehensive, horizontal (all-sector) law that is **risk-based**.
    * **How it Works:** It categorizes AI systems:
        * **Unacceptable Risk:** Banned (e.g., social scoring, real-time biometric surveillance).
        * **High-Risk:** Heavily regulated (e.g., credit scoring, hiring, critical infrastructure). These require massive compliance, including data governance, human oversight, and transparency [1].
        * **Limited Risk:** Light-touch transparency rules (e.g., a chatbot must disclose it's an AI).
    * **Impact:** The "Brussels Effect"—this will likely become a global standard, much like GDPR. Any bank *touching* EU citizens (even abroad) will need to comply.

* **The United States (US): The "Innovation-First" Market**
    * **Framework:** **NIST AI Risk Management Framework (RMF)** [2] & The White House **Executive Order on AI** [3].
    * **Approach:** A **pro-innovation, market-driven, and sectoral** stance. There is no single "AI Act."
    * **How it Works:** The Executive Order [3] and NIST RMF [2] provide a *voluntary* (but highly influential) framework for companies to manage AI risk. The government's stance is to let existing regulators (like the Securities and Exchange Commission) apply their *existing* rules (e.g., on market manipulation or bias) to AI.
    * **Impact:** Focus is on leadership and competition. This creates a more "permissive" environment, but also regulatory uncertainty.

* **The United Kingdom (UK): The "Pragmatic" Middle-Ground**
    * **Framework:** A **"pro-innovation," principles-based, and context-specific** policy (Feb 2024 White Paper response) [4].
    * **Approach:** The UK has *explicitly rejected* a single "AI Act," fearing it would stifle innovation.
    * **How it Works:** It empowers existing regulators (like the FCA for finance) to apply a set of five core principles (e.g., Safety, Fairness, Accountability) *within their own context* [4]. This is seen as a more flexible, "light-touch" approach than the EU's.

* **China: The "State-Centric" Controller**
    * **Framework:** Iterative, application-specific rules (e.g., on GenAI, algorithms) [5].
    * **Approach:** A **state-centric, control-oriented** model.
    * **How it Works:** China is regulating *specific applications* very quickly, with a focus on **social stability, content control, and algorithmic security** [5]. The state is both a heavy-handed regulator and the primary funder/customer for its national AI champions.

**Key Question for Kenya:**
* **Where will Kenya land?** Kenya is a tech *importer* (using US/Chinese models) and a service *exporter* (with links to UK/EU). It also has its own GDPR-inspired **Data Protection Act (2019)** [6].
* **The Likely Path:** A "hybrid" or "straddle" approach. Kenya cannot afford to stifle its world-leading fintech sector (M-PESA, Tala, M-KOPA) with a heavy-handed EU-style law.
* **Prediction:** Expect a **pragmatic, risk-based framework** that draws inspiration from the EU's *principles* (especially on data and bias, given the DPA [6]) but applies them with the *flexibility* of the UK model [4] to protect innovation. The CBK will play a central role.

---

### 2. Corporate Governance – Firm-Level Concerns

**Slide Title:** The New Governance Trilemma: Balancing Risk & Opportunity

**Core Idea:** For a bank's board, AI governance is not just a compliance problem; it's a strategic "trilemma." You must balance three competing pressures simultaneously [7].



**Research & Key Points:**

* **The Trilemma (The 3 Pressures) [7]:**
    1.  **Commercial Opportunity:** The fear of *not* acting. "If we don't use AI for credit scoring, our competitors will. They will be faster, cheaper, and more accurate, and we will lose market share." This drives the business to move quickly.
    2.  **Reputation Risk (Customers):** The fear of *public failure*. "If we use this AI and it is found to be biased against a certain group, it will be on the front page of *The Standard*." This is about *Trust*. This is where **FAIR** principles (Fairness, Accountability, Transparency) are crucial as a public-facing commitment.
    3.  **Regulatory Risk (Regulator):** The fear of *non-compliance*. "If the CBK audits our AI model and we cannot explain *why* it denied a loan, we will face fines and sanctions." This is about *Explainability (XAI)* and *Model Risk Management (MRM)*, often building on existing guidance [8].

* **The Structural Question: How to Organize Governance?**
    * **Option 1: The "New AI Board" (or AI Ethics Council).**
        * **Pros:** Creates deep, specialist focus. Sends a strong signal to the market and regulators [7].
        * **Cons:** Can become a silo ("ethics-washing") with no real power, or it can be a bottleneck that slows down innovation.
    * **Option 2: "Embed in Existing Regimes."**
        * **Concept:** Use what you have. In the UK, this is the **SMCR (Senior Managers and Certification Regime)**. The Head of Credit is made *personally accountable* for the credit-scoring AI, just as they are for the human underwriting team. The UK's Financial Conduct Authority (FCA) has explicitly linked AI governance to the SMCR [9].
        * **Pros:** Creates *direct, personal accountability*, which regulators love. It integrates AI risk into existing business risk.
        * **Cons:** Is the Senior Manager *equipped* to understand the AI? This places a massive burden on existing execs.
    * **The Likely Outcome (Hybrid):** A central **AI Center of Excellence (CoE)** provides expert guidance, sets standards, and audits models, while the *ultimate accountability* for the AI's *output* and *risk* remains embedded with the business line owner (the Senior Manager) [9].

---

### 3. 'Market' Governance – Technical & Model-Level Concerns

**Slide Title:** Governing the "Black Box": From Prompting to Programming

**Core Idea:** The old governance model was based on validating *code you wrote*. The new model is about governing *models you don't own* (e.g., using a Gemini or GPT API). This requires a new set of technical controls.

**Research & Key Points:**

* **The Problem:** Base models (LLMs) are often called "stochastic parrots" [10]. They are trained on the internet, have inherent biases, and can "hallucinate" (fabricate information). Your "prompt" is a fragile instruction, not a deterministic command.

* **The "Old" Way (Brittle): Manual Prompt Engineering**
    * **What it is:** A developer writes a 10-page "meta-prompt" (`"You are a helpful bank assistant. You must be polite. You must not give financial advice. If the user asks X, you must do Y..."`).
    * **The Governance Risk:** It's a "dark art." It's not auditable, not reliable, and can break with a small change in the user's query or the base model's update. You are "prompting and praying."

* **The "New" Way (Robust): Programmatic Frameworks**
    * **Concept:** Stop "prompting" and start "programming." Use frameworks that *manage* the LLM as part of a larger, auditable system.
    * **Example (as you mentioned): DSPy (from Stanford)** [11]
        * **What it is:** A framework that separates the *program logic* from the *LLM*.
        * **How it Works:**
            1.  **Declare:** You define the *steps* you want (e.g., `Step 1: Check query for toxic language. Step 2: Retrieve customer's account balance. Step 3: Draft an answer.`).
            2.  **Compile:** You give DSPy a few examples of "good" answers. The **DSPy compiler** *itself* then experiments with hundreds of different prompts for each step (and for different LLMs) to find the *most reliable and optimal combination* to get the right answer [11].
            3.  **Result:** It turns a brittle prompt into a *robust, optimized, and verifiable program*.
    * **Why this is "Governance":** This approach is **systematic, auditable, and testable**. You are no longer at the mercy of a single prompt. You have an engineering *discipline* for managing the AI, which you can document and show to a regulator. It's the key to building reliable systems on top of unreliable (but powerful) base models.



---

### References

1.  European Commission. (2024). *Artificial Intelligence Act*. (Final text adopted by the European Parliament, March 2024).
2.  National Institute of Standards and Technology (NIST). (2024). *The AI Risk Management Framework (AI RMF 1.0)*. U.S. Department of Commerce.
3.  The White House. (2023). *Executive Order on the Safe, Secure, and Trustworthy Development and Use of Artificial Intelligence*.
4.  UK Department for Science, Innovation and Technology. (2024). *A pro-innovation approach to AI regulation: government response*. (February 2024).
5.  Kania, E., & Webster, G. (2024). "China's AI Regulations and How They Get Made." *Stanford University Cyber Policy Center*.
6.  Government of Kenya. (2019). *The Data Protection Act, 2019*.
7.  World Economic Forum. (2023). *Governing AI: A Framework for Boards and C-Suites*.
8.  U.S. Federal Reserve System. (2011). *SR 11-7: Guidance on Model Risk Management*.
9.  Financial Conduct Authority (FCA). (2024). *AI in financial services: Feedback on Discussion Paper DP22/4*. (This feedback directly links AI accountability to the Senior Managers and Certification Regime - SMCR).
10. Bender, E. M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). "On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?" *FAccT '21: Proceedings of the 2021 ACM Conference on Fairness, Accountability, and Transparency*.
11. Khattab, O., Singhvi, A., El-Arini, K., Potts, C., & Zaharia, M. (2023). "DSPy: Compiling Declarative Language Model Calls into Self-Improving Pipelines." *arXiv:2310.03714*.
---END OF MARKDOWN---
