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

