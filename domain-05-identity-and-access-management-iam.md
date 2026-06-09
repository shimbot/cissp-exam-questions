# CISSP Domain 5: Identity and Access Management (IAM)
[🏠 Home](.) ← Back to home

> Questions and tips for this domain, compiled and reviewed by subject matter experts.

---

*No questions yet for this domain.*

## Question #1

**Question:**

A multinational organization is implementing a single sign-on (SSO) solution to allow employees to access multiple cloud-based SaaS applications using their corporate Active Directory credentials. The security architect recommends using Security Assertion Markup Language (SAML) 2.0 for this integration. Which of the following BEST describes how authentication is handled in a typical SAML-based federation with an external identity provider (IdP)?

- **A)** The service provider (SP) authenticates the user directly and passes a signed assertion to the IdP for authorization.
- **B)** The identity provider (IdP) authenticates the user and generates a signed SAML assertion that the service provider (SP) trusts for access decisions.
- **C)** The user authenticates separately to each SP, and a SAML broker synchronizes the session tokens between them.
- **D)** The IdP authenticates the user and stores the session locally, while each SP independently verifies credentials through a shared LDAP directory.

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** In SAML 2.0 federation, the IdP handles authentication and creates a digitally signed assertion containing the user's identity and attributes. The SP trusts this assertion and makes access control decisions based on it — the user never authenticates directly to the SP.

🔥 **Key Takeaway:** SAML uses a "push" model where the IdP authenticates once and passes a trusted assertion to the SP; the user does not need separate credentials for each service.

---


## Question #2

**Question:**

A security architect is designing an access control system for a healthcare application where patient records must be classified by sensitivity (Public, Internal, Confidential, Restricted). Each provider's access to a record is determined by their role (Doctor, Nurse, Admin) combined with patient consent flags. To enforce this, the architect implements a system that evaluates rules against both the subject's role attributes and the resource's sensitivity label. Which combination of access control models is being implemented?

- **A)** MAC with RBAC
- **B)** RBAC with DAC
- **C)** DAC with MAC
- **D)** ABAC with RBAC

*Think about it before scrolling...*

📌 **Answer: D**

💡 **Tip:** Attribute-Based Access Control (ABAC) evaluates policies against multiple attributes (subject, resource, environment), and Role-Based Access Control (RBAC) assigns permissions based on job roles. In this scenario, access is determined by both the user's role (RBAC element) and the resource's sensitivity label along with patient consent flags (ABAC-style attribute evaluation). This hybrid ABAC/RBAC approach is common in modern healthcare systems where complex, multi-variable access decisions are needed.

🔥 **Key Takeaway:** ABAC provides fine-grained, policy-driven access decisions by evaluating multiple attributes, making it ideal for complex environments like healthcare where role alone is insufficient.

---


## Question #3

**Question:**

A security architect is implementing an authentication system for a healthcare organization that must comply with HIPAA. The solution requires users to authenticate using something they know (password), something they have (smart card), and something they are (fingerprint scan). The architect is concerned about the fingerprint scanner's false acceptance rate (FAR). Which of the following describes the most significant risk associated with a high FAR in this multi-factor authentication setup?

- **A)** Legitimate users will be frequently denied access, reducing productivity
- **B)** An unauthorized individual could be mistakenly authenticated as a valid user, compromising patient data
- **C)** The smart card reader will fail to communicate with the authentication server
- **D)** Password complexity requirements will need to be reduced to compensate for biometric errors

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** FAR (False Acceptance Rate) measures the likelihood that a biometric system incorrectly authenticates an unauthorized user. A high FAR means imposters may be accepted, which directly threatens data confidentiality — a critical concern under HIPAA. FRR (False Rejection Rate) is the opposite: legitimate users being rejected.

🔥 **Key Takeaway:** High FAR increases the risk of unauthorized access; high FRR impacts usability — understanding the trade-off between FAR and FRR is essential for balancing security with user experience.

---

