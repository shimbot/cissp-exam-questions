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

