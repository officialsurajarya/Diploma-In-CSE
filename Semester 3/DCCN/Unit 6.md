# Unit 6: Network Architecture

**Ethernet Specification and Standardization:**

Ethernet is a widely used networking technology for local area networks (LANs). It defines the physical and data link layers of the OSI model. Over time, Ethernet has evolved in terms of speed, standards, and media types. Below are the key Ethernet specifications and their standardization for different speeds:

---

**1. Traditional Ethernet (10 Mbps):**
- **Standard**: **IEEE 802.3**
- **Speed**: 10 Mbps (10 Megabits per second)
- **Media**: Initially, Ethernet used **coaxial cables** (Thicknet and Thinnet) for networking, but later shifted to twisted-pair cables (Cat5) and fiber optics.
- **Frame Format**: The basic Ethernet frame format for 10 Mbps Ethernet includes fields for destination MAC address, source MAC address, length/type, data, and a CRC (Cyclic Redundancy Check) for error checking.
- **Maximum Distance**: 
  - For coaxial cable: Up to **500 meters** (for Thicknet).
  - For twisted-pair cables (Cat5): Up to **100 meters**.
  
Ethernet at 10 Mbps was the original standard for local area networking, and it remains foundational for understanding modern Ethernet technologies.

---

**2. Fast Ethernet (100 Mbps):**
- **Standard**: **IEEE 802.3u**
- **Speed**: 100 Mbps (Fast Ethernet)
- **Media**: Initially, **Cat5 twisted-pair cables** were used for Fast Ethernet. Fiber optic cables (e.g., **100BASE-FX**) were also used for longer distances.
- **Transmission Method**: Fast Ethernet uses **Baseband transmission** (digital signals transmitted directly).
- **Frame Format**: The frame format is the same as Traditional Ethernet, but with higher data transfer speed capabilities.
- **Maximum Distance**:
  - For Cat5 twisted-pair cables: **100 meters**.
  - For fiber optic cables: Can support much longer distances, up to **2 kilometers** with multimode fiber and over **100 kilometers** with single-mode fiber.
  
Fast Ethernet (100BASE-TX) improved the speed and performance of traditional Ethernet, making it suitable for environments with higher bandwidth demands.

---

**3. Gigabit Ethernet (1000 Mbps):**
- **Standard**: **IEEE 802.3ab** (for copper twisted-pair cables) and **IEEE 802.3z** (for fiber optic cables)
- **Speed**: 1000 Mbps (1 Gbps or Gigabit Ethernet)
- **Media**: 
  - **Cat5e or Cat6 twisted-pair cables** (for distances up to 100 meters) for Gigabit Ethernet over copper.
  - **Fiber optic cables** for long-distance transmission (e.g., **1000BASE-LX** for single-mode fiber and **1000BASE-SX** for multimode fiber).
- **Transmission Method**: Like Fast Ethernet, Gigabit Ethernet uses **Baseband transmission** but supports a much higher data rate.
- **Frame Format**: Gigabit Ethernet maintains the same frame format as previous Ethernet standards but has mechanisms for achieving higher speed, such as **Auto-negotiation** to adjust to the best possible speed.
- **Maximum Distance**:
  - For Cat5e or Cat6 cables: **100 meters** (over twisted-pair).
  - For fiber optic cables: **550 meters** for multimode fiber and up to **40 kilometers** for single-mode fiber.
  
Gigabit Ethernet is commonly used in modern networks due to its high-speed capability and compatibility with existing Ethernet infrastructure.

---

### Key Differences Between Ethernet, Fast Ethernet, and Gigabit Ethernet:

| **Parameter**               | **Traditional Ethernet (10 Mbps)** | **Fast Ethernet (100 Mbps)** | **Gigabit Ethernet (1000 Mbps)** |
|-----------------------------|------------------------------------|-----------------------------|----------------------------------|
| **Speed**                   | 10 Mbps                            | 100 Mbps                    | 1000 Mbps (1 Gbps)              |
| **Standard**                | IEEE 802.3                        | IEEE 802.3u                 | IEEE 802.3ab (copper), IEEE 802.3z (fiber) |
| **Cable Type**              | Coaxial, twisted-pair (Cat5)       | Twisted-pair (Cat5e or Cat6) | Twisted-pair (Cat5e, Cat6), fiber optic |
| **Distance (Copper)**       | 100 meters                         | 100 meters                  | 100 meters (Cat5e or Cat6)      |
| **Distance (Fiber Optic)**  | N/A                                | Up to 2 km                   | Up to 40 km (single-mode fiber) |
| **Frame Format**            | Same as Ethernet                   | Same as Ethernet             | Same as Ethernet                |
| **Usage**                   | Basic LAN networks                 | Higher-speed LAN networks    | High-performance, data-intensive networks |

