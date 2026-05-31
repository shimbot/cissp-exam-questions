# CISSP Domain 1: Security and Risk Management
[🏠 Home](.) ← Back to home

> Questions and tips for this domain. Updated automatically when new questions are posted.

---

## Question #1


**Question:**

A security manager at a financial institution is tasked with creating a document that specifies the mandatory encryption algorithms and minimum key lengths required for all data-at-rest across the enterprise. The CISO wants this document to be **enforceable and non-negotiable** — every system must comply. Which type of document should be created?

- **A)** **Policy** — it expresses high-level management direction and strategic intent
- **B)** **Standard** — it specifies mandatory technical requirements that must be followed
- **C)** **Guideline** — it provides flexible recommendations that can be adapted per system
- **D)** **Procedure** — it outlines detailed step-by-step implementation instructions

*Think about the hierarchy before scrolling...*

📌 **Answer: B) Standard**

💡 **Tip:** The CISSP document hierarchy is tested frequently. **Policies** = board-level *what & why* (e.g., "We shall encrypt data at rest"). **Standards** = mandatory *specific technical requirements* (e.g., "AES-256 with minimum 256-bit keys required"). **Procedures** = detailed step-by-step *how-to* (e.g., "Open BitLocker, select drive, enable encryption"). **Guidelines** = *flexible recommendations* (e.g., "Consider post-quantum algorithms for long-term storage"). If the document is enforceable and prescribes specific technology parameters, it's always a **standard**, not a policy.

🔥 **Key Takeaway:** On exam day, remember: *Policies are broad and mandatory, Standards are specific and mandatory, Guidelines are flexible, Procedures are step-by-step.* When you see "specific mandatory requirements" — pick **Standard**.

---

## Question #2


**Question:**

As the new CISO of a publicly traded financial services firm, you're tasked with selecting an IT governance framework that aligns IT security objectives with enterprise business goals. The Board specifically wants a framework that integrates with the COSO internal control model and supports SOX compliance. The framework must define 37 high-level control objectives across four domains: *Plan and Organize, Acquire and Implement, Deliver and Support,* and *Monitor and Evaluate.*

Which framework BEST meets these requirements?

- **A)** ISO 27001 — Information Security Management System
- **B)** COBIT 2019 — Control Objectives for Information and Related Technologies
- **C)** NIST SP 800-53 — Security and Privacy Controls
- **D)** ITIL 4 — Information Technology Infrastructure Library

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** COBIT is the only framework that explicitly bridges IT governance with business goals through 37 control objectives across 4 domains (P/O, A/I, D/S, M/E). Its design aligns with COSO's internal control model, making it the go-to framework for SOX compliance in finance. ISO 27001 focuses on ISMS certification, NIST 800-53 catalogs US federal security controls, and ITIL governs IT service management — none provide the business-aligned governance COBIT does.

🔥 **Key Takeaway:** COBIT = IT governance + business alignment + SOX/COSO integration. ISO 27001 = ISMS certification. NIST 800-53 = US federal control catalog. ITIL = IT service delivery/operations. Know which fits which scenario.

---

## Question #3


**Question:**

A multinational corporation has just acquired a fast-growing SaaS startup. The CISO is tasked with integrating the startup's security operations into the parent company's environment. After the close of the acquisition, which action should the CISO take FIRST to manage the resulting security risk?

- **A)** Conduct a full penetration test of the startup's internal network
- **B)** Discover and inventory the startup's assets, data flows, and existing controls
- **C)** Migrate all startup email accounts to the parent company's mail servers
- **D)** Mandate the startup's employees complete the parent's security awareness training immediately

---

*Think about your answer before reading on...*

---

📌 **Answer: B**

💡 **Tip:** In mergers & acquisitions, the critical first step is always **discovery** — you cannot protect what you don't know exists. Jumping to a penetration test (A) assumes you already know the attack surface; migrating email (C) or mandating training (D) puts operational cart before the discovery horse. The correct order is: *discover → classify → assess risk → integrate*. This mirrors the "establish context" phase from risk management frameworks — understand the environment before treating risk.

🔥 **Key Takeaway:** M&A security = discovery first, integration second. Always begin with asset inventory, data flow mapping, and control identification before any remediation or migration.

---

## Question #4


**Question:**

Your organization has mandated annual security awareness training with a 95% completion rate across all departments. The board asks whether this investment is truly reducing risk. After reviewing the program, what metric would BEST demonstrate that the training is driving measurable security improvement?

- **A)** The percentage of employees who completed the training module within the first 30 days of the fiscal year
- **B)** A year-over-year reduction in the organizational phishing simulation click-through rate
- **C)** The total number of security policy violations recorded by the internal audit team
- **D)** An increase in the volume of help desk tickets categorized as "security-related"

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** Completion rates measure throughput, not effectiveness. The whole point of security awareness is to change *behavior*. A phishing simulation click-through rate declining over time directly demonstrates that employees are applying what they learned — they're recognizing and reporting suspicious emails instead of clicking. Don't confuse "training completed" with "training effective."

🔥 **Key Takeaway:** Security awareness programs must be measured by behavioral outcomes (e.g., reduced phishing clicks, increased reporting of incidents), not just administrative metrics like completion percentages. The ISC2 exam loves this distinction.

---

## Question #5


**Question:**

A large hospital network is adopting the NIST Cybersecurity Framework (CSF) to strengthen its security program. The CISO insists the framework must drive continuous improvement rather than serve as a one-time compliance exercise. Which approach BEST aligns with the NIST CSF's intended use?

- **A)** Implement all five functions (Identify, Protect, Detect, Respond, Recover) simultaneously across every department within a rigid 6-month timeline
- **B)** Perform a current-state assessment against the Framework Core, develop a prioritized Target Profile using the appropriate Implementation Tier, and repeat the process on a regular cycle
- **C)** Map existing HIPAA regulatory obligations directly to CSF categories, conduct a single gap analysis, and develop a remediation plan for all identified gaps
- **D)** Adopt NIST's Informative References as mandatory organization-wide controls and measure success through annual third-party audit scores

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** The NIST CSF is not a compliance checklist — it's a risk-based framework. The **Current Profile** reflects where you are today; the **Target Profile** reflects your desired security posture based on business risk tolerance. **Implementation Tiers** (1–4) describe organizational maturity, from Partial to Adaptive. Regular iteration of the profile process is what drives continuous improvement, not a single pass.

🔥 **Key Takeaway:** NIST CSF uses a cyclical "Current Profile → Target Profile → Gap Analysis → Action Plan" process tied to Implementation Tiers — the goal is *continuous improvement*, not checkbox compliance.

---

## Question #6


**Question:**

A security architect leads a threat modeling exercise for a new cloud-based payment application. The team identifies that an attacker could intercept a customer's session cookie after authentication and reuse it to impersonate that user in subsequent API calls. Using the STRIDE threat classification model, which threat category best describes this attack scenario?

- **A)** Elevation of Privilege
- **B)** Tampering
- **C)** Information Disclosure
- **D)** Spoofing

*Think about it before scrolling...*

📌 **Answer: D) Spoofing**

💡 **Tip:** STRIDE is Microsoft's threat modeling mnemonic: **S**poofing (impersonating a user/identity), **T**ampering (modifying data or code), **R**epudiation (denying an action), **I**nformation Disclosure (exposing data), **D**enial of Service (disrupting availability), **E**levation of Privilege (gaining unauthorized access). Session hijacking and cookie theft fall under **Spoofing** because the attacker *masquerades* as a legitimate user — they aren't elevating privilege, they're stealing an existing valid identity.

🔥 **Key Takeaway:** On exam day, map each attack to STRIDE by asking "what is the attacker's primary benefit?" — impersonation = Spoofing, reading data = Information Disclosure, modifying = Tampering, getting more access = Elevation of Privilege.

---

## Question #7


**Question:**

A regional bank discovers a SQL injection vulnerability in its legacy online loan application. The risk assessment gives it a HIGH likelihood (score 4/5) and HIGH impact (score 5/5), with an annualized loss expectancy of $2.8M. The application was deprecated and is scheduled for a full cloud migration in 10 months. The CIO wants to keep the application running to avoid losing 4,000 monthly loan applications. Which risk treatment strategy represents the **most prudent** first step in this scenario?

- **A)** **Risk acceptance** — formally document the risk and allocate a reserve fund for potential losses since migration is already planned

- **B)** **Risk transfer** — purchase a cyber insurance policy to cover the full $2.8M ALE

- **C)** **Risk avoidance** — take the application offline immediately until the cloud migration is complete

- **D)** **Risk mitigation** — deploy a Web Application Firewall (WAF) with virtual patching and initiate a code hardening sprint

*Think about it before scrolling...*

📌 **Answer: D**

💡 **Tip:** The four risk treatment strategies are **avoid**, **transfer**, **mitigate**, and **accept**. On the CISSP exam, **mitigation** (implementing compensating controls) is almost always the preferred first response to a high-severity risk. Risk acceptance is only appropriate *after* controls have been applied to reduce residual risk to an acceptable level — not as the sole response to a critical SQL injection risk. Insurance (transfer) covers financial loss but does nothing to prevent a breach or protect customer data. Avoidance (shutting down) would be appropriate if no controls could reduce risk, but here WAF + patching is a viable option.

🔥 **Key Takeaway:** Always reduce risk through mitigation first; only accept the *residual* risk that remains after controls are in place. Mitigation ≠ elimination — residual risk …

---

## Question #8


**Question:**

As the CISO of a financial services firm, you review quarterly metrics and notice that employees pass phishing simulations at a 92% rate — well above the industry benchmark. However, three actual data loss incidents occurred this quarter caused by insiders emailing customer PII to personal email accounts "to work from home." Your risk register still flags human error as the highest residual risk. Which of the following BEST addresses this gap?

- **A)** Deploy a DLP solution that blocks emails containing PII patterns to external domains
- **B)** Update the Acceptable Use Policy to explicitly prohibit sending customer data to personal accounts
- **C)** Conduct mandatory, role-based training on proper data handling procedures for customer PII
- **D)** Terminate the three offending employees and publish the terminations as a deterrent

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** This question tests the critical distinction between *security awareness* (building general consciousness — phishing, password hygiene) and *security training* (building specific job competencies). A 92% phishing pass rate proves awareness is working, but data loss through mishandling reveals a *training* gap — employees don't know the *how* of proper data handling. Option A (DLP) is a compensating technical control, not a root-cause fix. Option B (policy update) is necessary but insufficient without instruction. Option D is punitive and doesn't remediate the skill gap across the organization.

🔥 **Key Takeaway:** The CISSP exam expects you to know: **Awareness** = "what" (changes behavior through consciousness), **Training** = "how" (builds specific skills), **Education** = "why" (deeper understanding). Don't confuse them!

---

## Question #9


**Question:**

After a ransomware incident caused $2.3M in losses, your organization's board asks whether cyber insurance would have helped. The CISO explains that the current cyber policy does not cover ransom payments and has a $500K deductible covering only third-party liability. The board wants a risk treatment recommendation. **Which risk treatment strategy does cyber insurance represent?**

- **A)** Risk mitigation, because insurance reduces the likelihood of an attack
- **B)** Risk avoidance, because insured organizations avoid security controls
- **C)** Risk acceptance, because the premium cost is a budgeted operating expense
- **D)** Risk transference, because financial liability shifts to the insurer

---

*Think about it before scrolling...*

---

📌 **Answer: D**

💡 **Tip:** The four risk treatment strategies are **Avoid, Mitigate, Transfer, and Accept** (often remembered as AMTA). Cyber insurance is a classic example of **risk transference** — you pay a premium to shift the financial impact of a loss to a third party (the insurer). A common exam trap: insurance does NOT reduce likelihood (eliminates A), it doesn't replace controls (eliminates B), and paying a premium is not the same as accepting the risk (eliminates C). Insurance transfers the *financial consequence*, not the *responsibility*.

🔥 **Key Takeaway:** On the CISSP exam, if a question involves shifting financial liability to another party via contract or insurance, that is **risk transference** — never confuse it with acceptance or mitigation.

---

## Question #10


**Question:**

A financial services firm is hiring a new senior database administrator who will have elevated access to customer financial records. During the background investigation, the HR department discovers that the candidate was convicted of misdemeanor computer fraud 12 years ago but has a clean record since then. The hiring manager wants to proceed, citing the candidate's strong technical skills. As the security manager, what is your BEST course of action?

- **A)** Allow the hire but implement enhanced monitoring and logging for this employee
- **B)** Deny the hire unconditionally due to the criminal record
- **C)** Conduct a risk assessment weighing the severity and recency of the offense against the sensitivity of the role
- **D)** Proceed with the hire since the conviction is over 7 years old and legally cannot be considered

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** Personnel security requires a risk-based approach, not absolute rules. While background checks are essential for positions handling sensitive data, the CISSP emphasizes evaluating the *totality of circumstances* — including the nature, severity, recency, and relevance of any offense to the job duties. A 12-year-old misdemeanor with no subsequent issues may be acceptable when balanced against compensating controls, but you shouldn't ignore it (ruling out A and B). The 7-year lookback applies to *credit* reporting in some jurisdictions, not criminal history disclosure.

🔥 **Key Takeaway:** Personnel screening decisions must balance security risk, legal constraints, and business needs — treat each case individually through a documented risk assessment rather than applying blanket policies.

---

## Question #11


**Question:**

A large retail company has completed a risk assessment on its new e-commerce platform, identifying a high-severity vulnerability in the payment processing module. After implementing compensating controls, the residual risk level remains above the CISO's stated risk appetite of $50,000 per incident. The CISO presents the risk register to the board of directors, recommending that a $45,000 annual cyber insurance policy be purchased. The board approves the budget. Which of the following BEST describes this risk treatment?

- **A)** Risk mitigation — the controls reduced the risk to an acceptable level
- **B)** Risk transference — the financial liability is shifted to an insurer
- **C)** Risk acceptance — management formally acknowledged and accepted the residual risk
- **D)** Risk avoidance — the company decided not to accept the residual exposure

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** This is a classic CISSP trap. Just because cyber insurance was purchased (which looks like transference), the key phrase is that the *residual risk remains above the risk appetite*. By approving the budget for insurance without further technical controls, the board is formally **accepting** the residual risk. The insurance is a tool that helps them accept it, but the decision itself is risk acceptance. Always identify the *primary risk decision* — not the support mechanism.

🔥 **Key Takeaway:** When management is aware of residual risk exceeding appetite and formally approves the situation (by budget, waiver, or signature), that is **risk acceptance** — even if insurance or other risk-handling mechanisms are also in place.

---

## Question #12


**Question:**

As the CISO for a mid-sized financial firm, you are leading the annual enterprise risk assessment. Your team has gathered extensive data on asset values, threat frequencies, and historical loss magnitudes across 40 business units. The board wants a clear, defensible risk prioritization for budget allocation but also needs to account for subjective factors like reputational damage and regulatory scrutiny that are difficult to monetize. Which approach BEST balances these requirements?

- **A)** Perform a purely quantitative analysis using ALE/SLE/ARO calculations for every asset
- **B)** Conduct a qualitative assessment using red/amber/green ratings based on expert interviews
- **C)** Use quantitative analysis for assets with reliable financial data, then overlay qualitative rankings for intangible risks
- **D)** Rely exclusively on a single Delphi-method roundtable with senior executives

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** The CISSP exam tests your understanding that quantitative risk analysis (ALE = SLE × ARO) gives defensible dollar figures for tangible assets, but qualitative analysis is better for intangible risks like reputation. In practice and on the exam, the best answer is almost always a **hybrid approach** — use quantitative where you have good data, and supplement with qualitative judgment where data is unreliable or risks are subjective. Never pick an answer that insists on *only* one method when the scenario involves both financial and non-financial factors.

🔥 **Key Takeaway:** ALE/SLE/ARO formulas are pure quantitative; Delphi and red/green matrices are pure qualitative; when a scenario includes both hard-dollar assets AND intangible risks, the **combined/hybrid** approach is the correct CISSP answer.

---

## Question #13


**Question:**

A multinational financial services firm headquartered in Frankfurt operates data centers in Germany, India, and the United States. The EU subsidiary needs to transfer employee HR records — including salary data, performance reviews, and disciplinary actions — to the US headquarters for centralized payroll processing via the company's ERP system. The European Commission has not issued an adequacy decision for the United States. Under the GDPR, which mechanism MOST appropriately provides a lawful basis for this ongoing cross-border data transfer?

- **A)** Standard Contractual Clauses (SCCs) adopted by the European Commission, supplemented by a Transfer Impact Assessment (TIA)
- **B)** Binding Corporate Rules (BCRs) approved solely by the US headquarters' Data Protection Officer
- **C)** Obtaining informed written consent from each of the 12,000 affected employees individually
- **D)** An intra-company data sharing agreement designating the US entity as a joint data controller

*Think about it before scrolling...*

📌 **Answer: A**

💡 **Tip:** GDPR Chapter V (Articles 44-49) strictly regulates cross-border data transfers to "third countries" without an adequacy decision. The three primary lawful transfer mechanisms are: (1) an **Adequacy Decision** from the European Commission, (2) **Standard Contractual Clauses (SCCs)** plus a **Transfer Impact Assessment (TIA)** to evaluate the destination country's legal protections, and (3) **Binding Corporate Rules (BCRs)** — but BCRs require formal approval from the lead EU supervisory authority, not just internal sign-off. Individual consent is strongly discouraged for employer-employee data transfers because of the inherent power imbalance; employees can rarely withhold consent freely without fear of repercussions.

🔥 **Key Takeaway:** For ongoing routine cross-border data transfers without an adequacy dec…

---

## Question #14


**Question:**

Your organization is launching a new patient-facing mobile health application that will collect personal health information (PHI), geolocation data, and biometric readings. As the security manager, you recommend conducting a Privacy Impact Assessment (PIA) before development begins. The product owner pushes back, arguing this will delay the release. Which of the following BEST describes why a PIA is critical in this scenario?

- **A)** It ensures the application meets all functional security requirements before deployment
- **B)** It identifies and mitigates privacy risks early, ensuring compliance with privacy regulations and building trust by design
- **C)** It replaces the need for a full data protection impact assessment under GDPR requirements
- **D)** It calculates the financial ROI of privacy controls to justify the security budget

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** A Privacy Impact Assessment (PIA) is a proactive governance tool that systematically evaluates how personally identifiable information (PII) is collected, used, stored, and shared. It's conducted *early* in a project — ideally during the requirements phase — so privacy risks can be identified and addressed before system design is locked in. Many regulations (GDPR Article 35, PIPEDA, HIPAA) either require or strongly recommend PIAs for high-risk processing. A PIA is *not* a replacement for functional testing, nor does it substitute for a regulatory-required DPIA — in fact, a DPIA is a specific type of PIA required under GDPR.

🔥 **Key Takeaway:** Privacy by Design isn't optional for modern CISSPs — a PIA ensures privacy risks are identified and mitigated **before** you build the system, not bolted on afterwards.

---

## Question #15


**Question:**

A security administrator, while troubleshooting a network connectivity issue, accidentally misconfigures a firewall rule, exposing an internal database containing protected health information (PHI) to the internet for approximately three hours. An attacker discovers and exfiltrates 8,000 patient records. The Data Protection Authority (DPA) issues a substantial fine, and affected patients file a class-action lawsuit alleging negligence.

Which of the following BEST characterizes the legal framework involved in the patients' lawsuit?

- **A)** Criminal negligence — the administrator's actions must be proven guilty beyond a reasonable doubt
- **B)** Civil tort liability — the patients must prove the organization failed in its duty of care by a preponderance of the evidence
- **C)** Strict liability — the organization is automatically liable for any data exposure regardless of intent or negligence
- **D)** Administrative liability — both the DPA fine and the patient lawsuit are considered administrative proceedings

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** The patients' lawsuit is a civil tort (negligence) claim. In civil court, the standard of proof is **preponderance of the evidence** (more likely than not), NOT "beyond a reasonable doubt" — that's the criminal standard. The DPA fine is a *regulatory/administrative* action, not civil. Strict liability (Choice C) does not generally apply to data breaches; negligence or intent must be shown. Criminal charges (Choice A) require *mens rea* (guilty mind) and a much higher burden of proof.

🔥 **Key Takeaway:** CISSP tests three bodies of law: **Criminal** (intent, beyond reasonable doubt), **Civil/Tort** (negligence/failure of due care, preponderance of evidence), and **Administrative/Regulatory** (agency rules and fines). Always match the plaintiff's claim to the correct…

---

## Question #16


**Question:**

A multinational corporation wants to formally demonstrate to clients and regulators that it has implemented a comprehensive information security management system (ISMS) with third-party audited controls, a defined scope, and continuous improvement cycles. The board specifically wants a certifiable standard.

Which framework BEST meets this requirement?

- **A)** NIST Cybersecurity Framework — provides voluntary risk-based guidance but offers no certification mechanism
- **B)** ISO/IEC 27001 — specifies mandatory ISMS requirements and supports third-party certification against them
- **C)** COBIT 2019 — focuses on IT governance and control objectives, primarily used for audit alignment
- **D)** SABSA — a methodology for developing security architectures, not a certifiable standard

---

*Think about it... the key distinction here is **certifiability vs. guidance**...*

📌 **Answer: B) ISO/IEC 27001**

💡 **Tip:** The CISSP exam expects you to know the difference between frameworks that are certifiable vs. advisory. ISO 27001 is the *only* globally recognized ISMS framework you can get certified against via an accredited third-party registrar. NIST CSF, COBIT, and SABSA are all guidance or governance frameworks — valuable but not certifiable. Remember: **ISO 27001 = Requirements (certifiable)**, **ISO 27002 = Implementation guidance/controls (not certifiable)**.

🔥 **Key Takeaway:** On the exam, if a question mentions "certification" or "auditable ISMS," your answer is almost always ISO 27001 — it's the only standard in Domain 1 built around formal, certifiable compliance.

---

## Question #17


**Question:**

A security officer has completed a risk assessment on a new cloud-based customer portal. The inherent risk was rated **High** (likelihood 4, impact 5 on a 5-point scale). After implementing encryption, a WAF, and quarterly penetration testing, the residual risk remains **Medium** (likelihood 3, impact 3). The CIO wants to launch on schedule and accept the residual risk. However, the board has formally documented a risk appetite of **"Low"** — meaning they will only accept risks rated Low or below. What should the security officer recommend?

- **A)** Accept the residual risk since compensating controls have been applied
- **B)** Implement additional controls to reduce residual risk to match the board's risk appetite
- **C)** Transfer the remaining risk through cyber insurance
- **D)** Avoid the risk entirely by canceling the cloud portal project

---

*Think about it before scrolling...*

---

📌 **Answer: B**

💡 **Tip:** There's a critical distinction between *inherent risk* (risk before controls) and *residual risk* (risk remaining after controls). Management can accept, mitigate, transfer, or avoid residual risk — but acceptance is only valid when residual risk falls within the organization's documented **risk appetite**. Here, Medium exceeds Low, so acceptance is off the table until more controls bring it down. Risk transfer (insurance) doesn't reduce the residual risk level; it just shifts financial impact.

🔥 **Key Takeaway:** Residual risk must be at or below the risk appetite threshold for acceptance to be a valid option — always compare the post-control risk level to the stated appetite, not just the improvement over inherent risk.

---

## Question #18


**Question:**
Your organization is outsourcing its customer help desk operations to a third-party provider in a different country. As the security manager, you are reviewing the draft contract. Which of the following is the MOST critical security requirement to include in the service-level agreement (SLA)?

- **A)** The provider agrees to conduct annual tabletop exercises with your incident response team.
- **B)** The provider must grant your organization the right to audit their security controls and access relevant logs.
- **C)** The provider will maintain a 99.9% uptime SLA for their ticketing system.
- **D)** The provider commits to using AES-256 encryption for all stored customer data.

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** While encryption (D), uptime guarantees (C), and joint exercises (A) are all good practices, the most critical right you need in an outsourcing contract is the **right to audit**. Without contractual audit rights, you cannot independently verify the provider's security posture — you're relying entirely on their word. Remember: you can outsource the work, but you cannot outsource the accountability. The SLA should include specific audit frequency, scope, and costs.

🔥 **Key Takeaway:** Always negotiate contractual right-to-audit clauses in third-party agreements — it's your only independent verification mechanism when outsourcing critical operations.

---

## Question #19


**Question:**
Your organization's data retention policy mandates deletion of all emails and documents after 90 days. The legal department notifies the security team that a lawsuit has been filed against the company and certain communications must be preserved. Several shared mailboxes containing potentially relevant messages are scheduled for automated purging next week. What is the BEST course of action?

- **A)** Proceed with the automated 90-day deletion since the retention policy was established before the lawsuit
- **B)** Suspend all deletion activity for data potentially relevant to the litigation until the legal hold is formally released
- **C)** Delete only the messages from employees not named in the lawsuit to reduce storage overhead
- **D)** Encrypt the relevant emails and allow the deletion schedule to proceed since encryption preserves admissibility

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** A legal hold (also called a litigation hold) overrides all standard retention and deletion schedules once litigation is "reasonably anticipated" or has been filed. If data covered by the hold is destroyed — even by an automated script following policy — it's considered spoliation of evidence. Courts can impose severe sanctions (monetary penalties, adverse inference instructions to juries, or even default judgments) against companies that fail to preserve relevant information.

🔥 **Key Takeaway:** Legal holds ALWAYS preempt standard data retention/deletion policies during active or reasonably anticipated litigation — never let automated purges destroy discoverable evidence.

---

## Question #20


**Question:**

Your organization's manufacturing division relies on a critical third-party supplier for embedded firmware. The supplier just passed the initial onboarding security assessment six months ago. During a routine contract review, you discover the supplier has since been acquired by a foreign entity, relocated its development team, and subcontracted testing to an unvetted firm. What is the *most critical* gap in your current vendor risk program?

- **A)** The initial security questionnaire did not include financial stability questions
- **B)** The contract lacks a right-to-audit clause for the supplier's subcontractors
- **C)** The vendor risk program lacks a continuous monitoring requirement for material changes
- **D)** The SLA does not specify minimum encryption standards for firmware delivery

📌 **Answer: C**

💡 **Tip:** A common CISSP trap is focusing on *initial* due diligence while ignoring *ongoing* oversight. Vendor risk management under Domain 1 requires continuous monitoring — not just a one-time assessment. Material changes (acquisition, relocation, subcontracting) should trigger a re-assessment. Answer B is tempting and also important, but the fundamental programmatic gap is the absence of a requirement to detect and respond to material changes *as they occur*. Without continuous monitoring, you may not even know about the acquisition or subcontracting until it's too late.

🔥 **Key Takeaway:** Vendor risk isn't a point-in-time checkbox — build continuous monitoring triggers (M&A, relocation, subcontracting, leadership changes) into your third-party risk management program.

---


## Question #21

**Question:**

As the CISO of a global financial firm, you receive daily threat briefings from your SOC team. The CEO asks for a high-level summary of geopolitical risks that could affect the organization's strategic investments over the next 12 months. Separately, your network defense team needs specific IP addresses, domains, and malware hashes to update firewall rules and IOC feeds. Which statement BEST describes the relationship between these two threat intelligence needs?

- **A)** Both needs can be satisfied by a single commercial threat intelligence feed if it provides adequate technical context.
- **B)** The CEO needs tactical intelligence while the network team needs operational intelligence, so different feeds and analysts are required.
- **C)** The CEO requires strategic intelligence for long-term decision-making, and the network team requires operational/tactical intelligence for immediate defense—each serves a different tier in the organization.
- **D)** Strategic intelligence is derived directly from tactical intelligence through automated correlation, so one platform can serve both needs without human analysis.


*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** The CISSP divides threat intelligence into four tiers — **Strategic** (executive/board level, long-term trends, geopolitical), **Operational** (campaign-level insight into upcoming attacks, TTPs), **Tactical** (IOCs like IPs, hashes, domains for immediate defense), and **Technical** (detailed exploit signatures, malware analysis). Mixing these up is a common exam trap — the question will test if you know who consumes each type and at what organizational level.

🔥 **Key Takeaway:** Map intelligence types to organizational levels — strategic = executives/board, tactical/operational = SOC/network defenders, technical = malware analysts/forensic teams.

---


## Question #22

**Question:**

As the new CISO of a multinational corporation, you are preparing your first quarterly risk briefing for the Board of Directors. The board members are primarily finance and legal professionals with limited technical backgrounds. During the meeting, you need to present the organization's current risk posture and justify a proposed $2M investment in a new SIEM platform. Which of the following approaches would be MOST effective for communicating security risk to this audience?

- **A)** Present detailed technical specifications of the SIEM, including log ingestion rates, correlation engine capabilities, and integration architecture diagrams
- **B)** Frame the discussion using business language — translate technical vulnerabilities into financial exposure, present risk in terms of likelihood and business impact, and use risk registers showing residual vs. inherent risk
- **C)** Walk through the complete CVSS scores of the top 20 critical vulnerabilities identified in the latest scan, explaining the attack vector complexity for each
- **D)** Distribute the full NIST SP 800-53 control assessment report and ask the board to approve the SIEM purchase based on the number of control deficiencies found

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** The Board of Directors cares about business outcomes, not technical details. CISSP emphasizes that security professionals must "speak the language of the business" — translating risk into financial terms (potential dollar loss, probability, ROI) enables informed decision-making by non-technical stakeholders. Framing security investments using risk management principles (inherent risk, residual risk, cost-benefit analysis) is the hallmark of effective security governance.

🔥 **Key Takeaway:** Always communicate security risk to executive leadership and the board in business terms — translate technical vulnerabilities into financial exposure and risk-based decisions.

---


## Question #23

**Question:**

A security manager is presenting a proposal to executive leadership for a new data loss prevention (DLP) system. The DLP solution costs $500,000 to implement and $75,000 per year for maintenance and licensing. Historical data shows that a single significant data breach costs the organization approximately $2.5 million in fines, remediation, and reputational damage, and such breaches have occurred roughly once every two years. Which of the following BEST provides a business-justified rationale for approving this investment?

- **A)** The DLP system will eliminate all data breach risk, making the organization fully compliant with industry regulations
- **B)** The annualized loss expectancy (ALE) of $1.25 million exceeds the total cost of ownership, making the investment financially justified
- **C)** Industry peers and competitors all deploy DLP technology, so the organization must follow best practices to remain competitive
- **D)** Existing security policies mandate implementation of DLP for any organization handling sensitive customer data

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** This question tests cost-benefit analysis for security controls. Calculate ALE = SLE ($2.5M) × ARO (0.5) = $1.25M per year. Compare to the control's annual cost (~$125K-$200K amortized). When ALE exceeds the control cost, the investment is financially justified. Trap choices: A is wrong because no control eliminates all risk (residual risk always remains); C is "bandwagon fallacy" — peer pressure is not business justification; D conflates policy with financial analysis — policies don't automatically justify any price tag. CISSP expects you to use quantitative risk analysis to make business cases.

🔥 **Key Takeaway:** When given a cost vs. historical loss scenario, always compute ALE (SLE × ARO) and compare to the control's annual cost — if ALE > cost, the investment is financially justified.

---


## Question #24

**Question:**

A large multinational organization is establishing an Information Security Steering Committee to improve oversight of its security program. The committee includes the CISO, CTO, heads of legal and HR, and business unit VPs. Which of the following is the PRIMARY responsibility of this steering committee?

- **A)** Approving and prioritizing security initiatives and ensuring alignment with business objectives
- **B)** Conducting daily security incident response operations
- **C)** Writing detailed firewall and access control policies for the network team
- **D)** Performing technical vulnerability scans on critical systems

*Think about it before scrolling...*

📌 **Answer: A**

💡 **Tip:** The information security steering committee is a senior management governance body, not an operational or technical team. Its role is to align security strategy with business goals, approve major initiatives, review risk posture, and secure funding — not to execute hands-on technical tasks. Operational tasks (incident response, writing technical policies, vulnerability scanning) belong to the security operations team, not the steering committee.

🔥 **Key Takeaway:** A steering committee provides governance, prioritization, and business alignment — it does not perform day-to-day security operations.

---


## Question #25

**Question:**

An information security manager implemented a new security awareness program that includes annual computer-based training modules, quarterly phishing simulations, and a monthly newsletter. Despite these efforts, a recent internal audit shows that 40% of employees still fail to report suspicious emails, and click-through rates on phishing simulations remain above 25%. Which of the following would BEST address this gap?

- **A)** Replace the phishing simulations with a more restrictive technical control, such as blocking all external email links
- **B)** Increase the frequency of phishing simulations to weekly and double the consequence for employees who click
- **C)** Shift the focus from awareness to security education by providing personalized, role-based learning that reinforces behavior change through ongoing engagement
- **D)** Outsource the entire security awareness program to a third-party vendor that guarantees lower click-through rates

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** The ISC2 Common Body of Knowledge distinguishes between security awareness (attention/reminders), training (skill building), and education (deeper understanding). When awareness alone fails to change behavior, the solution is to move up the maturity model toward education with role-based, personalized learning. Technical controls (A) bypass the human element, punishment (B) creates fear not understanding, and outsourcing (D) doesn't address the root cause of the program's ineffectiveness.

🔥 **Key Takeaway:** Security awareness builds attention, training builds skills, and education builds judgment — each is necessary and they exist on a continuum, not as interchangeable alternatives.

---

