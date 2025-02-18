---
aliases: [LLC, IEEE 802.2]
tags: [Networking Fundamentals, Data Link]
---

# Logical Link Control (LLC)

**Context:** The **Data Link layer (Layer 2)** of the OSI model is often broken into two sublayers:
- **LLC (Logical Link Control)** – Defined in IEEE 802.2
- **MAC (Media Access Control)** – Defined in various IEEE 802.x standards (e.g., 802.3 for Ethernet, 802.11 for Wi-Fi)

---

## Purpose & Function

1. **Protocol Multiplexing**  
   - LLC provides a method to identify which Network layer protocol (IP, IPX, AppleTalk, etc.) is being carried.  
   - Uses **Service Access Points (SAPs)** like DSAP (Destination SAP) and SSAP (Source SAP).

2. **Flow Control & Error Checking**  
   - LLC can offer basic **flow control** and **error detection** (though modern networks often rely on higher-layer protocols like TCP).

3. **Consistency Across IEEE 802.x**  
   - LLC is a **common interface** for various MAC sublayer implementations (e.g., 802.3 Ethernet, 802.11 Wi-Fi, 802.5 Token Ring).  
   - Ensures that upper layers can interact with multiple data link technologies in a standardized way.

---

## Key Concepts

- **DSAP and SSAP**: Identify what kind of traffic or protocol is in use (e.g., IPv4 vs. IPv6).  
- **LLC Header**: Typically added on top of the MAC header before the Network layer payload.  
- **Single LLC Sublayer**: Manages logical connections that can be shared among multiple MAC sublayers (wired, wireless, etc.).

---

## Relation to MAC Sublayer

- **LLC vs. MAC**:  
  - The **MAC** sublayer handles physical addressing (MAC addresses), framing, and media access methods (CSMA/CD, CSMA/CA).  
  - The **LLC** sublayer **abstracts** these specifics, ensuring upper-layer protocols see a uniform interface regardless of the underlying hardware.

---

## Exam Tips

- **OSI Layer**:  
  - LLC is part of **Layer 2** (Data Link), specifically the **upper sublayer**.  
- **IEEE 802.2**:  
  - The formal standard for LLC; if you see references to 802.2, that’s about LLC.  
- **Common Confusions**:  
  - ARP is often said to be “between” Layer 2 and Layer 3; LLC specifically operates *within* Layer 2.  

---

## Related Notes

- `[[Wi-Fi-MAC-LLC]]` – Discusses LLC in the context of 802.11 wireless networks.  
- `[[Ethernet-Data-Link-Layer]]` – Covers the MAC sublayer in Ethernet.  
- `[[01_Networking-Fundamentals/1.2_OSI-Model]]` – OSI model overview.

---

## External References

- [IEEE 802.2 Standard](https://standards.ieee.org/) – Official documentation for LLC.  
- [CompTIA Network+ Objectives](https://www.comptia.org/certifications/network) – For N10-009 exam references to Data Link layer operations.

