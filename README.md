# CSE421_Project
Computer Network

This project presents the design and implementation of a multi-zone Pasadena campus network using Cisco Packet Tracer. The topology connects five organizational LANs—Sheldon, Leonard, Penny, Howard, and Raj—along with a secure apartment committee network to enable reliable end-to-end communication across all zones.

A hierarchical IP addressing scheme was developed using VLSM to efficiently allocate addresses while meeting the specific host requirements of each network segment. Each character zone is equipped with its own local DHCP server for automated IP configuration, whereas the apartment committee LAN uses static addressing due to its sensitive nature.

The apartment network serves as the core service hub, hosting a DNS server for cross-zone name resolution and a web server (pasadena.com). It also includes a dedicated CaltechSupport server configured to display the message “Bazinga! We’ve got your back!” upon successful access. Additionally, email services (SMTP and POP/IMAP within Packet Tracer capabilities) are implemented in Sheldon’s and Raj’s networks to support secure research data exchange.

Inter-zone connectivity is achieved through a minimal router architecture while maintaining required direct router-level links between Leonard–Howard and Penny–Sheldon across separate routers. Network routing is implemented using a combination of OSPF dynamic routing and carefully configured static routes, without relying on default routes for inter-zone communication. To enhance resilience, a floating static backup route (Administrative Distance 25) is configured between the apartment network and Raj’s network via Leonard’s network.

The topology was fully validated through successful end-to-end connectivity tests, confirming correct addressing, routing, and service configurations across all zones.
