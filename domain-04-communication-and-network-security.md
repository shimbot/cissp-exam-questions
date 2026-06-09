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


## Question #6

**Question:**

A security analyst notices anomalous outbound traffic from the internal network to an unknown external IP address during a routine log review. Further investigation reveals that a server in the DMZ is sending encrypted data to this IP every 30 seconds. The company uses a stateful firewall at the perimeter, but no internal segmentation between the DMZ and internal network. Which of the following would BEST detect and prevent this type of exfiltration in the future?

- **A)** Deploying a honeypot on the same subnet as the compromised server
- **B)** Implementing an IPS with signature-based and anomaly-based detection rules inline on the DMZ segment
- **C)** Replacing the stateful firewall with a packet-filtering firewall
- **D)** Enabling port security on the DMZ switch ports

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** An Intrusion Prevention System (IPS) operates inline and can both detect suspicious outbound traffic via anomaly-based rules and actively block it — something a firewall alone or passive detection cannot do. Honeypots can attract attackers but won't prevent active exfiltration from a real server.

🔥 **Key Takeaway:** IPS provides inline detection AND prevention, making it critical for catching data exfiltration that firewalls alone may miss due to encrypted traffic.

---


## Question #7

**Question:**

A security analyst observes unusual traffic on the corporate network. Several internal workstations are sending large volumes of ICMP echo requests to a single external server, each with a spoofed source IP address belonging to the company's public-facing web server. The external server is responding with ICMP echo replies back to the web server, overwhelming its network interface. Which type of network attack is being executed from within the organization?

- **A)** Smurf attack
- **B)** Fraggle attack
- **C)** SYN flood
- **D)** DNS amplification attack

*Think about it before scrolling...*

📌 **Answer: A**

💡 **Tip:** A Smurf attack uses ICMP echo requests with a spoofed source IP (the victim) sent to a broadcast address, causing all devices on that network to reply to the victim. This has largely been mitigated by disabling directed broadcast forwarding on routers.

🔥 **Key Takeaway:** Smurf attacks are reflection-based DDoS attacks leveraging ICMP and directed broadcasts to amplify traffic against a target.

---


## Question #8

**Question:**

A security architect is designing a new data center network and recommends deploying Software-Defined Networking (SDN) with a centralized controller. The network team raises concerns about a single point of failure and potential attack surface. Which security control BEST addresses these concerns while preserving SDN benefits?

- **A)** Implementing micro-segmentation at the virtual switch level
- **B)** Deploying redundant, clustered SDN controllers with encrypted communications
- **C)** Moving the control plane functions to each individual switch
- **D)** Using VLANs to separate traffic instead of SDN architecture

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** In SDN, the controller is the "brain" of the network. A single controller is a critical point of failure and a high-value target. Clustering controllers (active-active or active-standby) with encrypted East/West communication between them provides both high availability and protection against compromise, while preserving the centralized SDN benefits.

🔥 **Key Takeaway:** SDN controllers must be clustered for redundancy and use encrypted channels between them to avoid controller hijacking or DoS of the centralized control plane.

---


## Question #9

**Question:**

A security analyst is reviewing the architecture of a VoIP deployment in a corporate environment. She notices that all voice traffic between the IP phones and the PBX server is transmitted without encryption, and the phones use DHCP to obtain their network configuration. Which of the following attack vectors poses the MOST significant risk in this configuration?

- **A)** ARP spoofing to redirect VoIP traffic to an attacker's device for eavesdropping
- **B)** SQL injection against the PBX server's web management interface
- **C)** Rainbow table attack on hashed voicemail passwords
- **D)** Buffer overflow in the phone's firmware update mechanism

*Think about it before scrolling...*

📌 **Answer: A**

💡 **Tip:** VoIP traffic is highly sensitive and should be protected using protocols like SRTP (encryption) and TLS for signaling. Without encryption, unauthenticated DHCP and ARP interactions make man-in-the-middle attacks trivial. Combining VLAN segmentation (voice VLAN) with 802.1X port security adds critical layers of defense.

🔥 **Key Takeaway:** Unencrypted VoIP traffic over a flat network segment is extremely vulnerable to ARP spoofing and eavesdropping; always segment voice traffic into a dedicated VLAN and enforce SRTP/TLS.

---


## Question #10

**Question:**

A security analyst is troubleshooting a Voice over IP (VoIP) deployment in a corporate environment. Users report choppy audio and occasional call drops. The network team confirms that voice and data traffic share the same VLAN without any prioritization. The VoIP phones use DHCP for addressing but rely on a central call manager with TLS signaling. Which of the following issues is MOST likely degrading the VoIP quality?

- **A)** Lack of TLS encryption between VoIP endpoints
- **B)** Absence of a VLAN dedicated to voice traffic with QoS enabled
- **C)** Use of DHCP instead of static IP addressing for VoIP phones
- **D)** The call manager is not configured with a redundant failover

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** VoIP traffic is latency-sensitive and requires Quality of Service (QoS) mechanisms. Placing voice on a separate VLAN with QoS prioritization prevents data traffic from competing for bandwidth and causing jitter or dropped packets. TLS encryption protects signaling but does not address bandwidth contention, DHCP is acceptable for phones, and redundancy helps availability but not quality.

🔥 **Key Takeaway:** VoIP and multimedia traffic must be isolated with QoS to ensure consistent call quality and prevent data traffic from causing latency or jitter.

---


## Question #11

**Question:**

A security architect is designing a network for a government facility that processes classified information. To mitigate the risk of electromagnetic eavesdropping (compromising emanations), the architect needs to select controls for the physical network infrastructure in areas where cables pass through unsecured zones. Which of the following is the MOST effective physical-layer countermeasure against this threat?

- **A)** Implementing Faraday cages around cable pathways
- **B)** Using fiber-optic cabling instead of copper
- **C)** Encrypting all data traversing the network
- **D)** Installing conduit shielding on all cable runs

*Think about it before scrolling...*

📌 **Answer: B**

💡 **Tip:** Fiber-optic cables do not emit electromagnetic radiation, making them immune to TEMPEST-style eavesdropping. While Faraday cages and conduit shielding reduce emanations from copper cables, fiber entirely eliminates the emissions at the physical layer. Encryption (C) protects data content but does nothing to prevent signal interception via physical emanations.

🔥 **Key Takeaway:** Fiber-optic cabling is the definitive physical-layer countermeasure against electromagnetic eavesdropping because it produces no measurable electromagnetic radiation.

---

