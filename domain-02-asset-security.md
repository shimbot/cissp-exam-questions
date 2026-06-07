# CISSP Domain 2: Asset Security
[🏠 Home](.) ← Back to home

> Questions and tips for this domain, compiled and reviewed by subject matter experts.

---

*No questions yet for this domain.*

## Question #1

**Question:**

A security architect is designing a data protection strategy for a healthcare mobile application that stores patient records locally on devices for offline access. The architect needs to ensure that if a device is lost or stolen, the patient data remains unreadable. The application must also be able to revoke access to previously downloaded records after a patient's treatment ends. Which combination of controls BEST addresses these requirements?

- **A)** Full disk encryption on the device + TLS for data in transit
- **B)** File-level encryption using a per-record key + Information Rights Management (IRM)
- **C)** Database-level transparent data encryption (TDE) + VPN tunnel
- **D)** Data masking + SSL certificate pinning

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** When data is stored on a mobile device and needs post-download access revocation, file-level encryption with per-record keys combined with IRM allows authorized viewing while enabling remote revocation — even for offline files. IRM policies can check licenses when the device reconnects.

🔥 **Key Takeaway:** Information Rights Management (IRM) protects data in use and can enforce access revocation policies even after the data has been distributed to endpoints.

---


## Question #2

**Question:**

A healthcare organization must share a large dataset of patient records with a research partner for statistical analysis. The data must remain usable for aggregate trend analysis while ensuring that individual patients cannot be re-identified. The CISO rules out simple encryption because the research partner needs to run queries against the data directly. Which technique BEST addresses this requirement?

- **A)** Data masking — replace all patient names with random characters but keep exact birth dates
- **B)** Tokenization — replace all sensitive identifiers with unique tokens stored in a secure mapping table
- **C)** Anonymization — remove all direct and indirect identifiers so re-identification is impossible
- **D)** Data retention policies — limit how long the research partner can store the dataset

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** Anonymization permanently removes direct identifiers (names, SSNs) AND indirect/quasi-identifiers (ZIP codes, birth dates) so that re-identification is computationally infeasible. Tokenization preserves the ability to re-map data via the token vault, which is useful for operational needs but doesn't prevent re-identification — the researcher could still reconstruct the original data through the token mapping. Data masking obscures data but often preserves format and may still allow re-identification through quasi-identifiers. For research where re-identification must be impossible, anonymization is the appropriate choice.

🔥 **Key Takeaway:** Anonymization irreversibly removes both direct and indirect identifiers to prevent re-identification, while tokenization and masking preserve some ability to reconstruct or re-map the original data.

---


## Question #3

**Question:**

A security architect is designing a data governance program for a multinational corporation that processes customer PII across multiple jurisdictions. The architect needs to ensure that data is created, stored, used, shared, archived, and destroyed in a controlled manner that aligns with legal retention requirements. Which of the following frameworks BEST describes this structured approach?

- **A)** Data classification schema
- **B)** Data lifecycle management
- **C)** Information rights management
- **D)** Data leakage prevention program

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** The data lifecycle covers all phases from creation through destruction, including storage, usage, sharing, and archival. While classification (A) labels data, IRM (C) protects rights, and DLP (D) prevents leaks — none alone governs the full lifecycle end-to-end with retention compliance.

🔥 **Key Takeaway:** Data lifecycle management defines policies for each phase of data from inception to secure disposal, ensuring legal and regulatory compliance throughout.

---


## Question #4

**Question:**

A financial services company is migrating its legacy application data to a new cloud-based platform. As part of the migration, the CISO requires data that has exceeded its legally mandated retention period to be permanently destroyed from the legacy systems. During the disposal process, an auditor discovers that some magnetic tapes containing client financial records were sent to a third-party shredding vendor without a chain-of-custody log or verification of destruction. Which of the following concepts was MOST directly violated?

- **A)** Data classification
- **B)** Data remanence
- **C)** Data ownership
- **D)** Data retention and disposal

*Think about it before scrolling...*

📌 **Answer: D**

💡 **Tip:** Data retention and disposal policies must define not just how long data is kept, but also the secure destruction methods and verification procedures. Chain-of-custody documentation is critical when third-party vendors handle media destruction.

🔥 **Key Takeaway:** A proper data disposal policy includes documented methods, chain-of-custody tracking, and verification of destruction (such as certificates of destruction).

---


## Question #5

**Question:**

A multinational corporation collects personal data from users across the EU. The CISO wants to ensure privacy is embedded into every stage of system development — from requirements gathering through deployment and eventual decommissioning. The privacy team recommends a proactive approach that considers privacy risks before they materialize. Which privacy framework principle does this BEST describe?

- **A)** Data minimization — collect only what is strictly necessary
- **B)** Privacy by design — integrating privacy controls into system architecture from the outset
- **C)** Purpose limitation — using data only for the specified purpose
- **D)** Accountability — demonstrating compliance through documentation

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** Privacy by design (PbD) is a proactive framework requiring privacy considerations to be embedded into systems and processes from the initial design stage, not bolted on afterward. It's a foundational requirement under GDPR Article 25.

🔥 **Key Takeaway:** Privacy by design means building privacy into systems proactively — it's not an afterthought or a checkbox.

---


## Question #6

**Question:**

A multinational corporation is migrating its customer relationship management (CRM) system to a public cloud provider. The CISO has approved the migration on the condition that all customer data remain encrypted both at rest and in transit, and that the organization retains the ability to manage its own encryption keys. The cloud provider offers a Hardware Security Module (HSM) service for key management. Which of the following BEST describes the shared responsibility model in this scenario?

- **A)** The cloud provider is responsible for securing the physical infrastructure, while the organization is responsible for managing access to the CRM application and customer data.
- **B)** The cloud provider is solely responsible for all security controls, including encryption key management, because it owns the HSM.
- **C)** The organization is responsible for everything above the hypervisor, including application security, while the provider manages the physical data center only.
- **D)** The organization must deploy its own on-premises HSM and cannot use the cloud provider's key management service under any circumstances.

*Think about it before scrolling...*

📌 **Answer: A**

💡 **Tip:** In the cloud shared responsibility model, the provider always secures the physical layer (data centers, hardware, network), while the customer secures data, access, and configurations. Even when using provider-managed HSMs, the customer retains responsibility for how keys are used and who has access to them — this is a classic CISSP distinction.

🔥 **Key Takeaway:** In any cloud deployment, the customer never fully offloads responsibility for data classification, access management, and encryption governance — security of the cloud vs. security in the cloud.

---


## Question #7

**Question:**

A financial institution is implementing a Data Loss Prevention (DLP) solution to prevent sensitive customer information from being transmitted outside the corporate network. The security team has identified that employees frequently email spreadsheets containing personally identifiable information (PII) to external partners. Which type of DLP control would be MOST effective at inspecting and blocking these outbound emails at the network perimeter?

- **A)** Endpoint DLP agent monitoring clipboard operations
- **B)** Network DLP inspecting SMTP traffic for content patterns
- **C)** Storage DLP scanning databases for unencrypted data
- **D)** Discovery DLP classifying data at rest on file servers

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** Network DLP operates at the network perimeter, inspecting traffic in motion (SMTP, HTTP, FTP) for sensitive content patterns like SSNs or credit card numbers. Endpoint DLP covers local actions (USB, clipboard), storage DLP protects data at rest, and discovery DLP finds unclassified data stores.

🔥 **Key Takeaway:** DLP controls are categorized by where data lives—Network DLP monitors data in motion, Endpoint DLP monitors data in use, and Storage/Discovery DLP monitors data at rest.

---


## Question #8

**Question:**

An organization uses Microsoft Azure Information Protection (AIP) to classify and protect sensitive documents. When a user emails a classified document to an external partner, the recipient can open the file but cannot forward it, print it, or take screenshots — even after downloading it to their local device. The protection persists regardless of where the file is stored. Which technology BEST describes this capability?

- **A)** Digital rights management (DRM) via information rights management (IRM)
- **B)** Data loss prevention (DLP) policy enforcement
- **C)** Full-disk encryption (FDE) with key management
- **D)** Transport layer security (TLS) for email encryption

*Think about it before scrolling...*

📌 **Answer: A**

💡 **Tip:** IRM (also called enterprise DRM or IPP) applies persistent usage policies that travel with the file — restricting actions like forward, print, copy, and screenshot — regardless of the file's storage location. DLP detects and blocks data in motion, but does not enforce persistent restrictions after delivery.

🔥 **Key Takeaway:** Information Rights Management (IRM) enforces persistent usage controls on documents that remain in effect no matter where the file is stored or forwarded.

---


## Question #9

**Question:**

A security architect is designing an access control policy for a healthcare organization's electronic health record (EHR) system. The organization requires that data can be labeled with sensitivity levels (e.g., Public, Internal, Confidential, Restricted) and that users can only access records based on their clearance level and formal need-to-know. Which access control model BEST meets these requirements?

- **A)** Discretionary Access Control (DAC)
- **B)** Role-Based Access Control (RBAC)
- **C)** Mandatory Access Control (MAC)
- **D)** Attribute-Based Access Control (ABAC)

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** MAC uses security labels (classifications) assigned to both subjects and objects, enforced by the system — not the data owner. This is critical in environments like military or healthcare where label-based access is legally required.

🔥 **Key Takeaway:** MAC enforces access based on system-assigned classification labels and clearance levels, preventing users from overriding security policies.

---


## Question #10

**Question:**

A large healthcare organization is implementing a new data governance program. The CIO assigns a senior doctor to classify patient health records, a database administrator to implement technical access controls, and an IT manager to maintain the data's accuracy and availability on a daily basis. Which of the following correctly identifies these roles?

- **A)** Doctor = Data Owner, DBA = Data Custodian, IT Manager = Data Steward
- **B)** Doctor = Data Steward, DBA = Data Owner, IT Manager = Data Custodian
- **C)** Doctor = Data Owner, DBA = Data Steward, IT Manager = Data Custodian
- **D)** Doctor = Data Custodian, DBA = Data Owner, IT Manager = Data Steward

*Think about it before scrolling...*

📌 **Answer: A**

💡 **Tip:** In data governance, the Data Owner (typically a senior business leader) classifies data and determines who can access it. The Data Steward ensures data quality and manages day-to-day accuracy, while the Data Custodian (typically IT) implements and maintains the technical security controls.

🔥 **Key Takeaway:** Data Owner classifies/authorizes, Data Custodian implements controls (IT), Data Steward maintains data quality — these three roles are distinct and commonly tested on the CISSP exam.

---

