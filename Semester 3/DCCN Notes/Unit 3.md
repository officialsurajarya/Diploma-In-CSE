# Unit 3: Network Basics

**3.1 Concept of Network:**
- A **network** is a collection of interconnected devices (such as computers, printers, routers, etc.) that share resources and communicate with each other.
- Networks can vary in size from small local networks (e.g., in a home or office) to large global networks (e.g., the Internet).
- A network allows data to be exchanged, and resources like files, printers, and internet connections to be shared.

**3.2 Models of Network Computing:**
- **Centralized Computing**: All computing is done on a central system, with users accessing it remotely (e.g., mainframe computing).
- **Distributed Computing**: Computing is distributed across multiple devices, which share tasks and resources (e.g., cloud computing).
- **Peer-to-Peer (P2P)**: Every device in the network can act as both a server and a client, sharing resources directly with each other.

**3.3 Networking Models:**
- **OSI Model (Open Systems Interconnection)**: A conceptual framework that standardizes network protocols into seven layers:
  1. **Physical Layer**: Deals with the transmission of raw data bits over the physical medium (e.g., cables, radio waves).
  2. **Data Link Layer**: Responsible for node-to-node data transfer and error correction (e.g., Ethernet, Wi-Fi).
  3. **Network Layer**: Handles data routing and forwarding between devices on different networks (e.g., IP).
  4. **Transport Layer**: Manages end-to-end communication and error handling (e.g., TCP, UDP).
  5. **Session Layer**: Manages sessions between applications (e.g., managing connections).
  6. **Presentation Layer**: Ensures data is in a usable format (e.g., encryption, data compression).
  7. **Application Layer**: The layer closest to the user, responsible for network services (e.g., HTTP, FTP, SMTP).

- **TCP/IP Model**: A simpler four-layer model that corresponds closely to the OSI model:
  1. **Link Layer**: Combines the OSI’s Physical and Data Link Layers.
  2. **Internet Layer**: Corresponds to the OSI’s Network Layer (e.g., IP).
  3. **Transport Layer**: Corresponds to the OSI’s Transport Layer (e.g., TCP, UDP).
  4. **Application Layer**: Corresponds to the OSI’s Session, Presentation, and Application Layers.

**3.4 Peer-to-Peer Network:**
- In a **peer-to-peer (P2P)** network, each device (peer) can act as both a client and a server. Peers share resources directly with one another without a central server.
- **Advantages**: Simple setup, low cost, decentralized.
- **Disadvantages**: Difficult to manage at scale, less security, no centralized control.

**3.5 Client-Server Network:**
- In a **client-server** network, there are dedicated servers that provide resources or services (like file storage, applications, or internet access), and clients (user devices) that request and use those services.
- **Advantages**: Centralized management, better security, scalability.
- **Disadvantages**: High setup and maintenance costs, reliance on servers.

**3.6 LAN, MAN, and WAN:**
- **LAN (Local Area Network)**: A network confined to a small geographic area, like a home, office, or building. It allows devices to share resources (e.g., printers, files) at high speed.
- **MAN (Metropolitan Area Network)**: A network that spans a city or large campus, connecting multiple LANs. MANs are often used by businesses or governments to connect their branches.
- **WAN (Wide Area Network)**: A network that spans large geographical areas, often a country or continent. The Internet is an example of a WAN. WANs are usually composed of multiple LANs or MANs connected via public or private networks.

**3.7 Network Services:**
- **Network services** provide functionalities that allow users and devices to interact with the network and each other. Common services include:
  - **File Sharing**: Allows multiple users to access and share files over the network.
  - **Email Services**: Facilitates communication through email.
  - **DNS (Domain Name System)**: Translates domain names (like www.example.com) into IP addresses.
  - **FTP (File Transfer Protocol)**: A method for transferring files between devices over the network.
  - **DHCP (Dynamic Host Configuration Protocol)**: Automatically assigns IP addresses to devices on the network.

**3.8 Switching Techniques:**
- **Circuit Switching**: A dedicated communication path is established between two devices for the entire duration of the communication. Traditional telephone networks use this technique.
  - **Advantages**: Guaranteed bandwidth and low latency.
  - **Disadvantages**: Inefficient use of resources, as the channel remains dedicated even when no data is being transmitted.
  
- **Packet Switching**: Data is broken down into packets and sent independently across the network. The packets may take different paths to reach the destination and are reassembled in order at the receiver.
  - **Advantages**: Efficient use of network resources, scalable, and supports bursty data transmission.
  - **Disadvantages**: Can introduce delays and requires complex reassembly of packets.

- **Message Switching**: Similar to packet switching, but larger messages are stored and forwarded in their entirety between switches, rather than being split into smaller packets.
  - **Advantages**: Suitable for long-distance communication and unreliable networks.
  - **Disadvantages**: Higher latency and the need for larger storage capacity at each switch.

