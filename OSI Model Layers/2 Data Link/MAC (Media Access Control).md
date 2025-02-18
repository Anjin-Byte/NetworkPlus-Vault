---
aliases: [MAC Sublayer, IEEE 802.x]
tags: [Networking Fundamentals, Data Link]
---

# Media Access Control (MAC)

**Context:** In the OSI model, **Layer 2** (Data Link) is often split into two sublayers:
- **LLC (Logical Link Control)** — IEEE 802.2
- **MAC (Media Access Control)** — Defined within various IEEE 802.x standards (e.g., 802.3 for Ethernet, 802.11 for Wi-Fi, 802.15 for Bluetooth)

The **MAC** sublayer is the **lower** portion of the Data Link layer and is responsible for:

1. **Physical Addressing**: Uses MAC addresses (often called hardware or burned-in addresses) to identify devices uniquely on a local network.  
2. **Frame Construction & Delivery**: Defines how frames are structured (headers, trailers) and handles sending/receiving at the local segment level.  
3. **Media Access**: Controls how devices gain access to the transmission medium (e.g., **CSMA/CD** for Ethernet, **CSMA/CA** for Wi-Fi).

---

## Functions of the MAC Sublayer

1. **Addressing**  
   - Inserts **source** and **destination** MAC addresses into the frame header.  
   - Uses unique MAC addresses (48-bit typically, e.g., `00:1A:2B:3C:4D:5E`) assigned by manufacturers.

2. **Framing & Error Detection**  
   - Builds **data frames** (Ethernet frames, Wi-Fi frames, etc.) by encapsulating the Network layer packet.  
   - Implements **Frame Check Sequence (FCS)** for error detection (e.g., CRC in Ethernet).

3. **Media Access Control**  
   - **Ethernet** (802.3) uses **CSMA/CD** (Carrier Sense Multiple Access/Collision Detection).  
   - **Wi-Fi** (802.11) uses **CSMA/CA** (Collision Avoidance).  
   - Other IEEE 802.x standards may use token passing or other methods.

4. **Segmentation Boundaries**  
   - Defines **maximum frame size** (e.g., 1518 bytes for standard Ethernet frames) and minimum size constraints.

---

## MAC Sublayer Examples

- **802.3 Ethernet**:  
  Uses MAC addresses, Ethernet headers, and CSMA/CD to manage access to the wired medium.
- **802.11 Wi-Fi**:  
  Uses wireless MAC frames, MAC addresses, and CSMA/CA to avoid collisions on the shared RF channel.
- **802.5 Token Ring** (now largely obsolete):  
  Used token passing to control access to a ring topology.

---

## Relationship with LLC

- The **LLC sublayer** (IEEE 802.2) sits **above** MAC.  
- **LLC** handles protocol multiplexing (identifying which Network layer protocol is in the frame), while **MAC** deals with the physical addressing and transmission rules.

```mermaid
flowchart TB
    A(Application Layer - 7)
    B(Presentation Layer - 6)
    C(Session Layer - 5)
    D(Transport Layer - 4)
    E(Network Layer - 3)
    F(LLC Sublayer)
    G(MAC Sublayer)
    H(Physical Layer - 1)

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
