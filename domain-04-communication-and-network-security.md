# CISSP Domain 4: Communication and Network Security
[🏠 Home](.) ← Back to home

> Questions and tips for this domain, compiled and reviewed by subject matter experts.

---

*No questions yet for this domain.*

## Question #1

**Question:**

A security architect is designing a network for a financial services company that requires strict isolation between the customer-facing web servers and the internal database servers containing sensitive financial records. The architect needs a solution that allows the web servers to communicate with the database servers on a specific port while completely preventing any direct external access to the database tier. Which of the following is the BEST approach to meet these requirements?

- **A)** Place both web and database servers on the same VLAN with a host-based firewall on the database servers
- **B)** Use a DMZ architecture with web servers in the DMZ and database servers on the internal network, connected through a firewall with stateful inspection
- **C)** Implement air-gapped database servers that are physically disconnected from all networks
- **D)** Configure a VPN tunnel directly between the web servers and database servers

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** A DMZ architecture places public-facing servers in a separate, less-trusted network segment while keeping sensitive internal resources (like databases) behind additional firewalls. Stateful inspection firewalls track connection states and only allow return traffic for established sessions initiated from the DMZ, providing defense in depth.

🔥 **Key Takeaway:** Network segmentation using DMZ architecture with stateful firewall inspection is the standard approach for isolating multi-tier web applications while still allowing necessary controlled communication.

---


## Question #2

**Question:**

A security architect is designing a multi-tier web application that must be accessible from the internet while protecting the database server from direct external access. The application server needs to initiate outbound connections to external payment gateways. Which network architecture BEST meets these requirements?

- **A)** Place the web server, application server, and database server all in the same VLAN behind a single firewall
- **B)** Deploy the web server in a DMZ, the application server in an internal segmented VLAN, and the database server in a protected VLAN with restrictive ACLs, using NAT for outbound traffic
- **C)** Connect all servers directly to the internet and rely on host-based firewalls on each system
- **D)** Place the database server in the DMZ behind the web server so it can be directly managed remotely

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** The DMZ hosts internet-facing web servers that accept inbound traffic. Internal tiers (app and database) should be in separate, increasingly restrictive VLANs. NAT allows the application server to initiate outbound connections to external services without exposing internal IP addresses. This layered (defense-in-depth) approach minimizes the attack surface.

🔥 **Key Takeaway:** A DMZ provides a buffer zone between the internet and internal networks, while layered VLANs with ACLs and NAT enforce defense-in-depth for multi-tier applications.

---


## Question #3

**Question:**

A security architect is reviewing wireless network configurations for a corporate headquarters. The organization requires strong mutual authentication between wireless clients and the RADIUS server, with per-user encryption keys. Which of the following configurations BEST meets this requirement?

- **A)** WPA2-PSK with AES encryption and MAC address filtering
- **B)** WPA3-SAE with OWE enabled for all clients
- **C)** WPA2-Enterprise using EAP-TLS with certificate-based authentication
- **D)** WPA3-Personal with Simultaneous Authentication of Equals

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** WPA2-Enterprise (IEEE 802.1X) with EAP-TLS provides mutual authentication through X.509 certificates on both the supplicant (client) and the authentication server (RADIUS). Unlike pre-shared key methods (PSK/SAE) which use a shared passphrase, EAP-TLS generates unique, per-session encryption keys via the 4-way handshake. This is the gold standard for enterprise wireless security because both parties prove their identity independently, preventing man-in-the-middle attacks and rogue access point threats.

🔥 **Key Takeaway:** For strong mutual authentication in enterprise Wi-Fi, use 802.1X/EAP-TLS — certificate-based authentication on both client and server provides far stronger assurance than any shared-key method.

---


## Question #4

**Question:**

A security analyst is troubleshooting a connectivity issue where traffic between two subnets is failing. The analyst verifies that the physical cables and switches are operational, and that the IP addressing and routing tables are correctly configured. However, packets are still being dropped. At which layer of the OSI model should the analyst focus next to identify the issue?

- **A)** Layer 5 — Session Layer
- **B)** Layer 2 — Data Link Layer
- **C)** Layer 4 — Transport Layer
- **D)** Layer 6 — Presentation Layer

*Think about it before scrolling...*

📌 **Answer: B) Layer 2 — Data Link Layer**

💡 **Tip:** The OSI model breaks networking into seven layers. If physical (Layer 1) is verified and network (Layer 3) is correct, then the problem might be at Layer 2, which handles framing, MAC addressing, and switching. Troubleshooting should follow the OSI layers sequentially.

🔥 **Key Takeaway:** When troubleshooting OSI model issues, always verify each layer bottom-up — physical (L1), data link (L2), network (L3) — before moving higher.

---


## Question #5

**Question:**

A security analyst is reviewing network traffic logs and notices an unusually high volume of TCP SYN packets sent to a web server from multiple spoofed source IP addresses, none of which complete the three-way handshake. The server is becoming unresponsive to legitimate clients. This attack exploits which characteristic of the TCP/IP protocol suite?

- **A)** TCP sequence number prediction vulnerability
- **B)** The stateless nature of the IP protocol at Layer 3
- **C)** The TCP three-way handshake requiring server-side state allocation before authentication
- **D)** The lack of encryption in the TCP header

*Think about it before scrolling...*

📌 **Answer: C**

💡 **Tip:** A SYN flood attack leverages the TCP three-way handshake design — the server allocates memory and state (the TCB) upon receiving a SYN segment before the handshake completes. Spoofed SYNs cause the server to exhaust resources waiting for ACKs that never arrive, making this a classic resource exhaustion attack at Layer 4.

🔥 **Key Takeaway:** SYN flood attacks exploit the asymmetric resource commitment in TCP's connection establishment — the server commits resources before the client authenticates.

---

