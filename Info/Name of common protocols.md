
1. **HTTP (Hypertext Transfer Protocol)**: Used for transferring web pages and other resources on the internet.
2. **HTTPS (Hypertext Transfer Protocol Secure)**: A secure version of HTTP, encrypting data for secure communication.
3. **FTP (File Transfer Protocol)**: Used for transferring files between a client and a server.
4. **SFTP (Secure File Transfer Protocol)**: A secure version of FTP, using SSH for encryption.
5. **SSH (Secure Shell)**: Provides secure remote login and command execution over a network.
6. **SMTP (Simple Mail Transfer Protocol)**: Used for sending and relaying emails.
7. **IMAP (Internet Message Access Protocol)**: Used for retrieving and managing emails from a mail server.
8. **POP3 (Post Office Protocol version 3)**: Another protocol for retrieving email, simpler than IMAP.
9. **DNS (Domain Name System)**: Translates domain names into IP addresses.
10. **TCP (Transmission Control Protocol)**: Ensures reliable communication between hosts.
11. **UDP (User Datagram Protocol)**: A faster, connectionless protocol used for low-latency, time-sensitive applications.
12. **IP (Internet Protocol)**: Used for routing data across networks.
13. **ICMP (Internet Control Message Protocol)**: Used for network diagnostics, such as ping tests.
14. **DHCP (Dynamic Host Configuration Protocol)**: Assigns IP addresses to devices on a network.

Network protocols are often grouped into layers according to the **OSI (Open Systems Interconnection)** model and the **TCP/IP model**. Here's a breakdown of the layers and protocols associated with each model:

### 1. **OSI Model (7 Layers)**

- **Layer 7: Application Layer**
  - Protocols: HTTP, HTTPS, FTP, SMTP, IMAP, POP3, DNS, Telnet, SSH
  - Function: Interfaces directly with user applications to provide network services like email, file transfer, and web browsing.

- **Layer 6: Presentation Layer**
  - Protocols: SSL/TLS (encryption), MIME (for emails), JPEG/PNG (image formats)
  - Function: Ensures data is in a usable format (encryption, data translation, and compression).

- **Layer 5: Session Layer**
  - Protocols: PPTP (Point-to-Point Tunneling Protocol), L2TP (Layer 2 Tunneling Protocol), RPC (Remote Procedure Call)
  - Function: Manages sessions between applications, keeping track of connections, and ensuring synchronization.

- **Layer 4: Transport Layer**
  - Protocols: TCP, UDP
  - Function: Ensures data is transferred error-free (TCP) or quickly (UDP) between hosts. Handles flow control, error correction, and data segmentation.

- **Layer 3: Network Layer**
  - Protocols: IP (IPv4/IPv6), ICMP, RIP (Routing Information Protocol), OSPF (Open Shortest Path First)
  - Function: Handles logical addressing (IP addresses) and routes data between devices across networks.

- **Layer 2: Data Link Layer**
  - Protocols: Ethernet, PPP (Point-to-Point Protocol), HDLC, ARP (Address Resolution Protocol)
  - Function: Handles physical addressing (MAC addresses), error detection, and flow control within a local network.

- **Layer 1: Physical Layer**
  - Protocols: Ethernet (physical layer aspects), IEEE 802.11 (Wi-Fi), Bluetooth, USB, Fiber
  - Function: Transmits raw bitstream over the physical medium (cables, radio frequencies).

### 2. **TCP/IP Model (4 Layers)**

- **Layer 4: Application Layer**
  - Protocols: HTTP, HTTPS, FTP, DNS, SMTP, IMAP, POP3, SSH, Telnet
  - Function: Similar to OSI’s Application, Presentation, and Session layers combined. Handles high-level protocols and communication with applications.

- **Layer 3: Transport Layer**
  - Protocols: TCP, UDP
  - Function: Manages end-to-end communication, providing reliable data transfer (TCP) or fast, connectionless communication (UDP).

- **Layer 2: Internet Layer**
  - Protocols: IP (IPv4/IPv6), ICMP, IGMP (Internet Group Management Protocol)
  - Function: Routes packets across networks, providing logical addressing and error handling at the network level.

- **Layer 1: Network Access Layer (Link Layer)**
  - Protocols: Ethernet, Wi-Fi (802.11), ARP, PPP
  - Function: Deals with physical hardware transmission (physical and data link layer combined), converting IP packets into frames for physical transmission.

### **Mapping Between OSI and TCP/IP Models**
| OSI Model        | TCP/IP Model            | Example Protocols           |
|------------------|-------------------------|-----------------------------|
| Layer 7: Application | Application Layer       | HTTP, HTTPS, FTP, SMTP       |
| Layer 6: Presentation | (part of Application)   | SSL/TLS, JPEG, PNG           |
| Layer 5: Session       | (part of Application)   | PPTP, L2TP, RPC              |
| Layer 4: Transport     | Transport Layer        | TCP, UDP                     |
| Layer 3: Network       | Internet Layer         | IP, ICMP, RIP, OSPF          |
| Layer 2: Data Link     | Network Access Layer   | Ethernet, Wi-Fi, ARP         |
| Layer 1: Physical      | (part of Network Access)| Fiber, Bluetooth, IEEE 802.3 |

Each layer serves a specific function in the process of transmitting and receiving data across networks.
