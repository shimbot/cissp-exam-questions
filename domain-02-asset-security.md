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

