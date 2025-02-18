---
title: OSI Model
tags:
  - Networking
  - Concepts
  - OSI
  - ISO
aliases:
  - Open Systems Interconnection
  - ISO/IEC 7498-1
---
> [!quote]
> The **Open Systems Interconnection** (**OSI**) **model** is a _reference model_ from the [International Organization for Standardization](https://en.wikipedia.org/wiki/International_Organization_for_Standardization "International Organization for Standardization") (ISO) that "provides a common basis for the coordination of standards development for the purpose of systems interconnection."
## Overview

The **Open Systems Interconnection (OSI) model** is a conceptual framework used to understand and standardize the functions of a networking system. It divides network communication into **seven layers**, each with distinct roles and protocols.

> **Purpose:**  
> - Provide a common language for discussing network architecture  
> - Help troubleshoot networking issues by isolating problems at specific layers  

---

## The 7 Layers of the OSI Model

1. **[[Physical (Layer 1)]]**  
   - Handles the transmission and reception of raw bit streams over a physical medium  
   - Examples: Cables (Ethernet, Fiber), Connectors (RJ-45), Voltage, Light, Radio Frequencies

2. **[[Data Link (Layer 2)]]**  
   - Provides node-to-node data transfer and handles **MAC addressing**, **framing**, **error detection**  
   - Examples: Ethernet frames, MAC addresses, Switches, Bridges

3. **[[Network (Layer 3)]]**  
   - Responsible for **logical addressing** and **routing** of packets between subnets  
   - Examples: IP addressing, Routers, ICMP (ping, traceroute)

4. **[[Transport (Layer 4)]]**  
   - Ensures end-to-end communication; handles **segmentation**, **flow control**, and **error recovery**  
   - Examples: TCP (reliable), UDP (unreliable), Port numbers

5. **[[Session (Layer 5)]]**  
   - Manages sessions or **connections** between applications; sets up, maintains, and terminates sessions  
   - Examples: Session management for RPC, SQL sessions

6. **[[Presentation (Layer 6)]]**
   - Translates data from lower layers into a format usable by the application; handles **encryption**, **compression**, **encoding**  
   - Examples: SSL/TLS encryption, data format conversion (e.g., ASCII, EBCDIC)

7. **[[Application (Layer 7)]]**  
   - Closest to the end-user; provides **network services** for applications  
   - Examples: HTTP, FTP, SMTP, DNS, DHCP

---

## Mnemonics

- **Top-Down:** “**All People Seem To Need Data Processing**”  
  (Application, Presentation, Session, Transport, Network, Data Link, Physical)

- **Bottom-Up:** “**Please Do Not Throw Sausage Pizza Away**”  
  (Physical, Data Link, Network, Transport, Session, Presentation, Application)

---

## How it Compares to the TCP/IP Model

While the **OSI model** has 7 layers, the **[[TCP & IP|TCP/IP model]]** is typically described as 4 or 5 layers (e.g., **Link**, **Internet**, **Transport**, **Application**). Despite the different layer names and groupings, they serve the same conceptual purpose—defining how data moves across a network.

| OSI Model Layer                          | TCP/IP Equivalent |
| ---------------------------------------- | ----------------- |
| [[Application (Layer 7)\|Application]]   | Application       |
| [[Presentation (Layer 6)\|Presentation]] | Application       |
| Session (5)                              | Application       |
| Transport (4)                            | Transport         |
| Network (3)                              | Internet          |
| [[Data Link (Layer 2)\|Data Link]]       | Link              |
| Physical (1)                             | Link              |

---
## [[OSI Layers & Relevant Protocols]]

---
## Key Points & Tips

- **Isolation & Troubleshooting:**  
  By identifying which layer a problem occurs at, you can narrow down the root cause quickly (e.g., a bad cable at Layer 1 vs. a misconfigured IP address at Layer 3).

- **Protocols & Devices:**  
  Each layer is associated with specific protocols (e.g., IP at Layer 3, TCP/UDP at Layer 4) and devices (e.g., routers operate at Layer 3, switches at Layer 2).

- **Exam Relevance:**  
  You should be comfortable matching common protocols and devices to each layer, as well as explaining how data flows from one layer to another.

---

## Related Notes

- `[[01_Networking-Fundamentals/1.1_Protocols-and-Ports]]` – Learn about common network protocols and their port numbers.
- `[[01_Networking-Fundamentals/1.3_Network-Topology-Types]]` – Compare different physical and logical topologies.
- `[[05_Network-Troubleshooting/5.1_Troubleshooting-Methodology]]` – Using the OSI layers to diagnose network issues systematically.

---

## External References

- **CompTIA Official Page:** [CompTIA Network+ (N10-009)](https://www.comptia.org/certifications/network)  
- **ISO/IEC 7498-1 Standard**: [ISO Store (Paywalled)](https://www.iso.org/standard/20269.html)  
- **OSI Model Wikipedia Entry:** [Wikipedia: OSI Model](https://en.wikipedia.org/wiki/OSI_model)

---
