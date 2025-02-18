---
aliases:
  - Wi-Fi MAC
  - 802.11 LLC
  - Data Link Sublayers
tags:
  - Networking
  - Fundamentals
  - Data
  - Link
  - Wi-Fi
---

# Wi-Fi MAC/LLC

**Context:** In the OSI model, the **Data Link layer (Layer 2)** is often split into two sublayers:
- **[[Logical Link Control (LLC)|LLC (Logical Link Control)]]**
- **[[MAC (Media Access Control)|MAC (Media Access Control)]]**

For Wi-Fi (IEEE 802.11), these sublayers govern how wireless frames are created, managed, and transmitted over the air.

---

## Overview

1. **IEEE 802.11 Standard**  
   - Defines **Wi-Fi** at both the **Physical Layer** (Layer 1) and **MAC** (sub-layer of Layer 2).  
   - The **LLC** sublayer is governed by **IEEE 802.2**, providing an interface to higher-layer protocols (e.g., IP).

2. **Purpose**  
   - **MAC Sublayer**: Responsible for frame delivery, addressing, collision avoidance (CSMA/CA), and coordination of channel access.  
   - **LLC Sublayer**: Provides a standard way to identify the protocol at the Network layer (e.g., IPv4, IPv6) and enable multiplexing/demultiplexing of data.

---

## MAC Sublayer (Media Access Control)

- **802.11 MAC Frames**:  
  - Contains **MAC addresses** (source, destination, BSSID, etc.).  
  - Manages control frames (RTS/CTS), management frames (Beacon, Probe), and data frames.
- **CSMA/CA** (Carrier Sense Multiple Access with Collision Avoidance):  
  - Wi-Fi’s method for coordinating access to the shared medium (the RF channel).  
  - Devices listen before transmitting, use acknowledgments (ACKs), and sometimes RTS/CTS to reduce collisions.
- **Security Enhancements**:  
  - **WPA2/WPA3** operate at higher layers but also interact with MAC sublayer for frame encryption (WPA uses 802.11i standard, which influences MAC framing).

---

## LLC Sublayer (Logical Link Control)

- **IEEE 802.2**:  
  - Defines the LLC sublayer, which is consistent across different 802 networks (Ethernet, Wi-Fi, etc.).
- **SAPs (Service Access Points)**:  
  - The LLC sublayer uses Service Access Points to identify the upper-layer protocol (like IP or ARP).
- **Multiplexing**:  
  - LLC allows multiple protocols to coexist over a single MAC-layer technology by tagging each frame with the relevant protocol information.
- **Error Checking & Flow Control**:  
  - While modern networks often rely on higher-layer protocols (like TCP) for error correction, LLC can provide basic flow control and error notification.

---

## Data Encapsulation in 802.11

1. **MAC Header**  
   - Includes addresses, sequence control, frame control bits (type/subtype), and other management info.
2. **LLC Header**  
   - Identifies the upper-layer protocol with DSAP (Destination SAP) and SSAP (Source SAP).
3. **Network Layer Data**  
   - For example, an IPv4 or IPv6 packet.
4. **FCS (Frame Check Sequence)**  
   - Used by the MAC sublayer to detect transmission errors.

---

## Key Takeaways

1. **Layer 2 Sublayers:**  
   - MAC: Deals with framing, addressing, and medium access.  
   - LLC: Handles protocol multiplexing and service access points for upper layers.
2. **CSMA/CA**:  
   - Essential for collision avoidance on wireless networks; different from **CSMA/CD** used by wired Ethernet.  
3. **Security**:  
   - 802.11 includes management and control frames that can be encrypted for secure Wi-Fi environments (WPA2, WPA3).  
4. **Interoperability**:  
   - Because LLC is standardized (802.2), it ensures consistent communication across various IEEE 802 networks (Wi-Fi, Ethernet, etc.).

---

## Related Notes

- `[[01_Networking-Fundamentals/1.2_OSI-Model]]` – General OSI model overview.  
- `[[01_Networking-Fundamentals/Ethernet-Data-Link-Layer]]` – Parallel structure for wired Ethernet MAC/LLC.  
- `[[02_Networking-Implementations/Wireless-Networking-Standards]]` – More detail on 802.11 a/b/g/n/ac/ax.  
- `[[04_Network-Security/Wireless-Security]]` – Encryption methods and best practices at the MAC level (WPA2/WPA3).

---

## External References

- **IEEE 802.11 Standard**: [IEEE Get Program](https://standards.ieee.org/standard/802_11.html) (official specs for Wi-Fi)  
- **IEEE 802.2**: Defines the LLC sublayer for LAN standards  
- **CompTIA Network+ Objectives**: [CompTIA Network+ (N10-009)](https://www.comptia.org/certifications/network)  

> **Note:** Real-world Wi-Fi implementations bundle many of these details under “WLAN drivers” or “chipset firmware,” but understanding MAC/LLC helps you troubleshoot at Layer 2.
