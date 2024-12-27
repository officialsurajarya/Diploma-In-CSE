# Unit 7: Network Connectivity

**7.1 Network Connectivity Devices:**
Network connectivity devices are essential for establishing, managing, and maintaining communication between different devices in a network. They facilitate the transfer of data and ensure that data reaches its intended destination.

---

**7.2 NICs (Network Interface Cards):**
- **Definition**: A Network Interface Card (NIC) is a hardware component that connects a computer or other device to a network. It allows the device to communicate over the network by providing the physical interface for the transmission of data.
- **Types**:
  - **Wired NICs**: Use Ethernet cables (usually through a **RJ45 port**) to connect to a network.
  - **Wireless NICs**: Use Wi-Fi to connect to wireless networks, often integrated into laptops and mobile devices.
- **Functions**:
  - **Physical Layer**: NICs operate at the physical layer of the OSI model, providing the hardware interface for communication.
  - **Data Link Layer**: NICs also function at the data link layer, where they frame data for transmission over the network.
  - **MAC Address**: NICs are assigned a unique **MAC (Media Access Control)** address that identifies them on a network.
  
- **Common Use**: NICs are found in almost all devices that need network connectivity, including desktops, laptops, servers, and even some printers.

---

**7.3 Hubs, Switches, Routers, Repeaters, Modem, Gateway:**
These are essential devices that help in establishing and maintaining network communication.

- **Hubs**:
  - **Function**: A hub is a simple networking device that broadcasts data to all devices connected to it. It operates at the **Physical Layer** of the OSI model.
  - **Limitation**: Hubs do not manage traffic effectively and lead to collisions, which can reduce network efficiency.
  - **Usage**: Hubs are largely obsolete today, replaced by more intelligent devices like switches.

- **Switches**:
  - **Function**: A switch operates at the **Data Link Layer** (Layer 2) and is used to forward data to specific devices based on their **MAC addresses**. It is more efficient than a hub because it does not broadcast data to all connected devices.
  - **Usage**: Switches are commonly used in modern Ethernet networks to create LANs and connect devices within a local network.

- **Routers**:
  - **Function**: Routers operate at the **Network Layer** (Layer 3) and are used to forward data between different networks, such as between a local network (LAN) and the internet. They determine the best path for data transmission.
  - **Usage**: Routers are critical in connecting different networks, for example, connecting a home or office network to the internet.

- **Repeaters**:
  - **Function**: A repeater is used to amplify or regenerate signals in a network to extend the transmission distance. It operates at the **Physical Layer**.
  - **Usage**: Repeaters are often used in long-distance communications (e.g., fiber optic cables) to prevent signal degradation.

- **Modem** (Modulator-Demodulator):
  - **Function**: A modem converts digital signals from a computer into analog signals that can be transmitted over phone lines or cable systems (modulation), and vice versa (demodulation). It operates at the **Physical Layer**.
  - **Usage**: Modems are used to provide internet connectivity over telephone lines or cable systems. Examples include **DSL modems** and **cable modems**.

- **Gateway**:
  - **Function**: A gateway operates at multiple layers of the OSI model and is used to connect two different types of networks that use different protocols (e.g., a TCP/IP network with an older system).
  - **Usage**: Gateways perform protocol translation, enabling communication between networks that otherwise wouldn't be able to communicate (e.g., connecting a LAN to the internet).

---

**7.4 Configuration of Routers & Switches:**

- **Router Configuration**:
  - **Accessing Router**: Routers are typically configured via a **command-line interface (CLI)** using a terminal application like **PuTTY** or via a **web-based interface**.
  - **Basic Steps**:
    1. **Assign IP addresses** to the router's interfaces (internal and external).
    2. **Configure routing protocols** (e.g., **RIP, OSPF, EIGRP**) for dynamic routing, or set static routes.
    3. **Configure NAT (Network Address Translation)** for converting private IP addresses to public ones (usually on the external interface).
    4. **Enable security features** such as **Access Control Lists (ACLs)** to restrict network access.
    5. **Set up DHCP** (Dynamic Host Configuration Protocol) to automatically assign IP addresses to devices on the network.
    6. **Configure firewall settings** to protect the network from unauthorized access.

  - **Example**: Configuring a router with a static IP address:
    ```bash
    Router> enable
    Router# configure terminal
    Router(config)# interface gigabitEthernet 0/1
    Router(config-if)# ip address 192.168.1.1 255.255.255.0
    Router(config-if)# no shutdown
    Router(config-if)# exit
    ```

- **Switch Configuration**:
  - **Accessing Switch**: Like routers, switches can be configured via CLI or web-based interface.
  - **Basic Steps**:
    1. **Assign VLANs (Virtual Local Area Networks)** to segment traffic and improve network efficiency.
    2. **Configure trunking** between switches if multiple VLANs need to pass through a single link.
    3. **Set up port security** to restrict access based on MAC addresses.
    4. **Enable Spanning Tree Protocol (STP)** to prevent network loops in a switched network.
    5. **Configure DHCP snooping** to prevent unauthorized DHCP servers from assigning IP addresses.

  - **Example**: Configuring a switch with VLAN:
    ```bash
    Switch> enable
    Switch# configure terminal
    Switch(config)# vlan 10
    Switch(config-vlan)# name Sales
    Switch(config-vlan)# exit
    Switch(config)# interface range fa0/1 - 24
    Switch(config-if-range)# switchport mode access
    Switch(config-if-range)# switchport access vlan 10
    Switch(config-if-range)# exit
    ```

---

