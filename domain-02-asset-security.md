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

