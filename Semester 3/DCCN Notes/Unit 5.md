# Unit 5: TCP/IP Addressing

**5.1 Concept of Physical and Logical Addressing:**
- **Physical Addressing (MAC Address)**: This refers to the unique identifier assigned to network interfaces for communications at the data link layer (Layer 2) of the OSI model. It is typically assigned by the manufacturer and is hard-coded into the hardware. Physical addresses are used for local communication within the same network.
  
- **Logical Addressing (IP Address)**: Logical addressing refers to the addresses assigned at the network layer (Layer 3) that identify devices on different networks. The most common example is the **IP address**, which is used to route data packets across networks. Logical addresses are used to facilitate communication between different networks.

---

**5.2 IPV4 Addresses – Address Space, Notations:**
- **IPv4 Address**: An IPv4 address is a 32-bit numerical label used to identify devices on a network. It is usually written in **dotted decimal notation** as four decimal numbers (each between 0 and 255) separated by periods (e.g., 192.168.1.1).
  
- **Address Space**: IPv4 has an address space of **2^32** addresses, which equals approximately **4.3 billion unique addresses**.

- **Notation**: The typical notation for an IPv4 address is **xxx.xxx.xxx.xxx**, where each "xxx" is an 8-bit value (ranging from 0 to 255). A **CIDR (Classless Inter-Domain Routing)** notation is also used to represent the subnet mask (e.g., 192.168.1.1/24, where "/24" indicates the subnet mask).

---

**5.3 Classful Addressing – Different IP Address Classes, Classes & Blocks, Net-id & Host-id, Masks, Address Depletion:**

- **Classful Addressing**: In IPv4, the IP address space was originally divided into **five classes (A, B, C, D, E)**, with Classes A, B, and C used for host addressing.
  
- **Classes & Blocks**:
  - **Class A**: Supports 128 networks (0.0.0.0 to 127.255.255.255). The default subnet mask is **255.0.0.0** (or /8).
  - **Class B**: Supports 16,384 networks (128.0.0.0 to 191.255.255.255). The default subnet mask is **255.255.0.0** (or /16).
  - **Class C**: Supports 2,097,152 networks (192.0.0.0 to 223.255.255.255). The default subnet mask is **255.255.255.0** (or /24).
  - **Class D**: Reserved for multicast addresses (224.0.0.0 to 239.255.255.255).
  - **Class E**: Reserved for experimental or future use (240.0.0.0 to 255.255.255.255).
  
- **Net-ID and Host-ID**:
  - **Net-ID**: Identifies the network to which the device belongs.
  - **Host-ID**: Identifies a specific device (host) within a network.
  
- **Subnet Masks**: The subnet mask determines how much of the IP address represents the network (Net-ID) and how much represents the host (Host-ID). It is used to create subnets and split networks into smaller segments.

- **Address Depletion**: With the rapid growth of devices connected to the internet, IPv4 address space started to become exhausted. This led to the development of **Classless Inter-Domain Routing (CIDR)** and IPv6.

---

**5.4 Classless Addressing – Address Blocks, Masks:**
- **Classless Addressing**: Unlike classful addressing, classless addressing does not divide IP addresses into fixed classes (A, B, C). Instead, it uses **CIDR notation** (e.g., 192.168.1.0/24) to define the network portion of an address.
  
- **CIDR (Classless Inter-Domain Routing)**: CIDR allows for more flexible and efficient allocation of IP addresses by using variable-length subnet masks (VLSM). It helps reduce the waste of IP addresses and address depletion by allowing networks to be allocated with more appropriate address blocks.

---

**5.5 Special IP Addresses:**
- **Private IP Addresses**: These are addresses reserved for use within private networks and are not routable on the public internet. They include:
  - Class A: 10.0.0.0 to 10.255.255.255
  - Class B: 172.16.0.0 to 172.31.255.255
  - Class C: 192.168.0.0 to 192.168.255.255
  
- **Loopback Address**: The loopback address (127.0.0.1) is used to test networking functionality on a local machine. It allows the device to send messages to itself.

- **Broadcast Address**: This address (e.g., 255.255.255.255) is used to send data to all devices within a specific network.

- **Multicast Address**: Reserved for one-to-many communication (e.g., 224.0.0.0 to 239.255.255.255).

---

**5.6 Subnetting and Supernetting:**
- **Subnetting**: The process of dividing a larger network into smaller sub-networks (subnets) by borrowing bits from the host portion of an IP address. This helps with efficient use of address space and better network management.
  - Example: Dividing a Class C network (e.g., 192.168.1.0/24) into smaller subnets like 192.168.1.0/26.

- **Supernetting**: The process of combining multiple smaller networks into a larger network by reducing the number of bits for the network portion and using larger blocks of IP addresses. It is typically used to aggregate IP address blocks in routing.

---

**5.7 Loopback Concept:**
- **Loopback Address**: The IP address **127.0.0.1** is used to refer to the local machine, allowing for internal communication testing. Any data sent to this address is looped back to the originating device.

---

**5.8 Network Address Translation (NAT):**
- **NAT** is a technique used by routers to translate private IP addresses within a local network into a single public IP address for communication with external networks (such as the internet). It helps address IPv4 address exhaustion and enables multiple devices within a local network to share a single public IP.

- **Types of NAT**:
  - **Static NAT**: Maps a specific private IP address to a specific public IP address.
  - **Dynamic NAT**: Maps a private IP address to any available public IP address from a pool.
  - **PAT (Port Address Translation)**: Maps multiple private IP addresses to a single public IP address, using different port numbers.

---

**5.9 IPV4 Header:**
- The **IPv4 header** contains essential information for routing and delivering packets, such as:
  - **Version**: Specifies the IP version (IPv4 or IPv6).
  - **Header Length**: The length of the header in 32-bit words.
  - **Type of Service (ToS)**: Specifies the priority and handling of the packet.
  - **Total Length**: The total size of the IP packet (header + data).
  - **Identification, Flags, Fragment Offset**: Used for packet fragmentation.
  - **Time to Live (TTL)**: Prevents packets from circulating endlessly in the network.
  - **Protocol**: Specifies the transport layer protocol (e.g., TCP, UDP).
  - **Source and Destination IP Addresses**: Identifies the sender and receiver of the packet.
  - **Checksum**: Used for error-checking the header.

---

**5.10 IPV6 Header:**
- The **IPv6 header** is simplified compared to IPv4 and consists of the following fields:
  - **Version**: Specifies the IP version (IPv6).
  - **Traffic Class**: Specifies the priority of the packet.
  - **Flow Label**: Used for special handling of packets in a flow.
  - **Payload Length**: The size of the data being sent.
  - **Next Header**: Identifies the transport layer protocol (e.g., TCP, UDP).
  - **Hop Limit**: The number of hops the packet can take before being discarded.
  - **Source and Destination Addresses**: 128-bit addresses for the sender and receiver.

---

**5.11 Comparison between IPV4 and IPV6:**

| **Aspect**              | **IPv4**                                | **IPv6**                                  |
|-------------------------|-----------------------------------------|-------------------------------------------|
| **Address Length**      | 32 bits (4 bytes)                      | 128 bits (16 bytes)                       |
| **Address Format**      | Dotted decimal (e.g., 192.168.1.1)     | Hexadecimal (e.g., 2001:0db8:85a3:0000::1) |
| **Address Space**       | 4.3 billion addresses                  | 340 undecillion addresses                 |
| **Header Size**         | 20-60 bytes                            | Fixed at 40 bytes                         |
| **Address Configuration**| Manual or DHCP                         | Auto-configuration (Stateless Address Autoconfiguration) |
| **Broadcast Support**   | Supports broadcast                     | Does not support broadcast; uses multicast |
| **Security**            | Optional