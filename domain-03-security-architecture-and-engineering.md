# CISSP Domain 3: Security Architecture and Engineering
[🏠 Home](.) ← Back to home

> Questions and tips for this domain, compiled and reviewed by subject matter experts.

---

*No questions yet for this domain.*

## Question #1

**Question:**

A security architect is evaluating access control models for a government system that processes classified documents. Users have varying clearance levels (Top Secret, Secret, Confidential), and documents are labeled with corresponding sensitivity levels. The architect needs a model that prevents users from reading documents above their clearance level while also preventing users from writing classified data to lower-level documents. Which security model enforces BOTH of these restrictions simultaneously?

- **A)** Clark-Wilson model
- **B)** Biba model
- **C)** Bell-LaPadula model
- **D)** Brewer-Nash model

*Think about it before scrolling...*

📌 **Answer: B) Biba model**

💡 **Tip:** Bell-LaPadula focuses on *confidentiality* (no read up, no write down). Biba, on the other hand, focuses on *integrity* (no read down, no write up). The question describes an integrity concern — preventing classified data from being improperly written to lower-level documents — which is the "no write down" property of the Biba model.

🔥 **Key Takeaway:** Bell-LaPadula protects confidentiality; Biba protects integrity — know which "no read/write up/down" rules apply to each.

---


## Question #2

**Question:**

A security architect is designing a new centralized authentication service for a large enterprise that must ensure non-repudiation of digital transactions between internal departments. The solution must allow recipients to verify the integrity and origin of messages without sharing a symmetric key with every possible sender. Which cryptographic approach BEST meets these requirements?

- **A)** Use a shared HMAC key distributed to all departments via a secure key management system
- **B)** Implement digital signatures where each sender signs messages with their private key and recipients verify with the sender's public key  
- **C)** Deploy TLS 1.3 with mutual authentication using pre-shared keys between each department pair
- **D)** Use symmetric encryption with a key derived from a Diffie-Hellman exchange per session

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** Non-repudiation requires asymmetric cryptography — only the sender possesses their private key, so they cannot deny having signed the message. Digital signatures provide both integrity (via hashing) and origin authentication (via public-key verification). HMAC and symmetric approaches lack non-repudiation because both parties share the same secret key.

🔥 **Key Takeaway:** Digital signatures using asymmetric cryptography (private key to sign, public key to verify) are the only approach that provides non-repudiation — the sender cannot deny the action since only they hold their private key.

---


## Question #3

**Question:**

A security architect is evaluating trusted platform module (TPM) technology for a new fleet of laptops used by employees handling classified data. Which PRIMARY purpose does a TPM serve in this scenario?

- **A)** It encrypts the entire hard drive using hardware-based AES-256 encryption
- **B)** It provides a hardware root of trust for securely storing cryptographic keys and attesting platform integrity
- **C)** It acts as a hardware firewall blocking unauthorized network connections at boot time
- **D)** It virtualizes the operating system to create isolated secure enclaves for sensitive applications

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** The TPM is a dedicated microcontroller that securely stores cryptographic keys (e.g., BitLocker keys) and performs platform integrity measurements (boot attestation) by hashing firmware/OS components. While it can be used with full-disk encryption, the TPM itself does not perform the encryption — it secures the keys.

🔥 **Key Takeaway:** A TPM's fundamental role is hardware-anchored trust — it protects keys from software-based attacks and verifies that the system hasn't been tampered with during boot.

---


## Question #4

**Question:**

A security architect is selecting an evaluation standard for a new government system that requires verifying the system meets specific security functional and assurance requirements through formal analysis and testing. The system will handle classified data and must undergo rigorous evaluation. Which evaluation framework is MOST appropriate for this scenario?

- **A)** ITSEC, which provides a comprehensive, flexible approach to security evaluation independent of the target's origin
- **B)** TCSEC (Orange Book), which focuses exclusively on confidentiality policies for military systems
- **C)** Common Criteria, which standardizes evaluation across nations using Protection Profiles and Security Targets
- **D)** FIPS 140-3, which validates cryptographic module implementations

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** The Common Criteria (ISO/IEC 15408) is the internationally recognized framework for security evaluation. It uses Protection Profiles (PPs) to define security requirements for specific types of products and Security Targets (STs) to describe the specific implementation. EAL levels (1–7) define assurance rigor. TCSEC is obsolete, ITSEC was a European precursor, and FIPS 140-3 is only for cryptographic modules.

🔥 **Key Takeaway:** Common Criteria is the gold-standard international framework for evaluating security products across multiple assurance levels with government recognition.

---


## Question #5

**Question:**

A large financial institution is adopting a security architecture framework to align its business strategy with IT security. The chosen framework categorizes the architecture into six layers: Contextual, Conceptual, Logical, Physical, Component, and Operational. It heavily uses a metamodel approach focusing on "who, what, when, why, and how" of enterprise architecture. Which security architecture framework is being described?

- **A)** SABSA
- **B)** TOGAF
- **C)** Zachman Framework
- **D)** ISO 27001

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** The Zachman Framework is an enterprise architecture ontology that organizes artifacts into six rows (Contextual, Conceptual, Logical, Physical, Detailed/Component, Operational) and six columns (Data, Function, Network, People, Time, Motivation). TOGAF provides a process (ADM) for developing architectures, while SABSA is specifically a security architecture framework derived from Zachman. The clue here is the six-layer categorization and the "who, what, when, why, how" interrogatives — those are hallmarks of the Zachman Framework.

🔥 **Key Takeaway:** Zachman = What/How/Where/Who/When/Why ontology matrix; SABSA = Zachman adapted for security; TOGAF = a process/methodology (ADM) for building architectures.

---


## Question #6

**Question:**

A security architect is designing access controls for a critical financial application. The architect implements multiple security layers so that if one control fails, others continue to protect the asset. The design also ensures that when a system fails, it defaults to a locked-down state denying access rather than permitting it. Which security design principles are being applied in this scenario?

- **A)** Separation of duties and job rotation
- **B)** Defense in depth and fail secure
- **C)** Least privilege and need-to-know
- **D)** Abstract layering and data hiding

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** Defense in depth (layered security) ensures multiple overlapping controls protect an asset, while fail secure means the system defaults to a denied/secure state on failure. These are foundational secure design principles. Fail secure is often confused with fail safe — fail safe prioritizes safety (e.g., doors unlock on fire), while fail secure prioritizes security (e.g., doors stay locked on power loss).

🔥 **Key Takeaway:** Defense in depth provides layered protection, and fail secure ensures failures don't compromise security — combining these creates resilient, secure system designs.

---


## Question #7

**Question:**

A security architect is designing an access control system for a distributed application where subjects directly hold unforgeable tokens that grant specific privileges to objects (e.g., a user's ticket granting read access to FileA and write access to FileB). The architect needs to ensure the system supports least privilege by allowing subjects to present only the specific tokens needed for each operation. Which access control model is BEST suited for this design?

- **A)** Role-Based Access Control (RBAC)
- **B)** Discretionary Access Control (DAC)
- **C)** Capability-based access control
- **D)** Mandatory Access Control (MAC)

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** A capability-based system uses unforgeable tokens (capabilities) that a subject holds to directly access objects. Unlike ACL-based models where the system checks a list on the object, capability-based access control puts control in the hands of the subject and naturally supports least privilege — the subject presents only the capabilities needed. This is a key differentiator from RBAC (role-based), DAC (owner-controlled), and MAC (system-enforced labels).

🔥 **Key Takeaway:** Capability-based access control uses subject-held, unforgeable tokens granting specific object privileges, enabling fine-grained least privilege by default.

---


## Question #8

**Question:**

A financial services company hires a security firm to perform a penetration test on their new online banking web application. The testers discover that the application uses unsalted MD5 hashing for storing user passwords, and the login page is vulnerable to SQL injection. Additionally, the application does not implement proper session management, allowing session IDs to be captured via XSS. Which of the following OWASP Top 10 categories best describes the **most critical** vulnerability that should be addressed first?

- **A)** Broken Authentication
- **B)** Injection
- **C)** Broken Access Control
- **D)** Security Misconfiguration

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** While unsalted MD5 hashes fall under Broken Authentication (A), and XSS could lead to session hijacking, the SQL injection is an Injection vulnerability (B) that directly allows attackers to bypass authentication, extract sensitive data, or execute arbitrary commands. Injection flaws are often rated as the most critical because they can lead to complete compromise of the backend database.

🔥 **Key Takeaway:** Injection attacks, particularly SQL injection, remain a top web application risk because they directly target the data layer and can bypass all other security controls.

---


## Question #9

**Question:**

A security architect is reviewing a web application that stores sensitive customer data. The development team implemented input validation on the client side using JavaScript, but the server does not independently validate or sanitize user-supplied input. Which OWASP Top 10 risk is the application MOST vulnerable to?

- **A)** Security Misconfiguration
- **B)** Broken Access Control
- **C)** Injection (e.g., SQL, NoSQL, OS command)
- **D)** Cryptographic Failures

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** Client-side validation provides a better user experience but offers zero security protection — an attacker can easily bypass it using tools like cURL or Burp Suite. Server-side input validation, parameterized queries, and output encoding are essential defenses against injection attacks.

🔥 **Key Takeaway:** Never rely on client-side validation for security; all input must be validated and sanitized on the server side to prevent injection attacks.

---


## Question #10

**Question:**

A security architect is designing access controls for a high-security data center that processes classified government contracts. The facility requires a layered physical security approach. Which of the following would BEST describe the use of a mantrap in this environment?

- **A)** A mantrap replaces the need for card readers by using biometric authentication at all entry points
- **B)** A mantrap is a physical barrier that prevents tailgating by allowing only one person to pass through at a time using interlocking doors
- **C)** A mantrap is a software-based access control that monitors for piggybacking after authentication
- **D)** A mantrap is a type of perimeter fence designed to detect intrusion attempts before reaching the building

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** A mantrap (or access control vestibule) uses two interlocking doors so that the first door must close and lock before the second opens, preventing unauthorized tailgating or piggybacking. It is a physical, not logical, control.

🔥 **Key Takeaway:** Mantraps are physical deterrents that enforce one-person-per-authentication to prevent tailgating at sensitive facility entry points.

---

