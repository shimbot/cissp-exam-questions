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

