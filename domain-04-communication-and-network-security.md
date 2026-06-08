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

