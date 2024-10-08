# Networking Introduction Revision Sheet

# Chapter One 
## 1. What is Networking?

Definition: Networking refers to the practice of connecting computers and other devices to share resources and information.
Purpose: Facilitate communication, resource sharing, and collaboration among users and devices.

## 2. Types of Networks

Local Area Network (LAN): Covers a small geographic area like a home or office.
Wide Area Network (WAN): Spans larger geographical distances, often connecting multiple LANs.
Metropolitan Area Network (MAN): Covers a city or campus.
Personal Area Network (PAN): For personal devices within an individual's range.

## 3. Network Topologies

Bus Topology: All devices share a single communication line.
Star Topology: Devices are connected to a central hub.
Ring Topology: Each device is connected to two others, forming a ring.
Mesh Topology: Devices are interconnected, offering multiple paths for data.

## 4. Network Protocols

Definition: Rules and conventions for communication between network devices.
Examples:
TCP/IP (Transmission Control Protocol/Internet Protocol)
HTTP/HTTPS (HyperText Transfer Protocol / Secure)
FTP (File Transfer Protocol)

## 5. Network Devices

Router: Directs data packets between networks.
Switch: Connects devices within a LAN, filtering and forwarding data to the correct destination.
Hub: Simple device for connecting multiple Ethernet devices, making them act as a single network segment.
Modem: Modulates and demodulates analog signals for digital data transmission over telephone lines.

## 6. The OSI Model

Purpose: Framework to understand network interactions in seven layers.
Layer 1: Physical
Layer 2: Data Link
Layer 3: Network
Layer 4: Transport
Layer 5: Session
Layer 6: Presentation
Layer 7: Application

## 7. IP Addressing
Definition: Unique identifier assigned to each device connected to a network.
Types: IPV4 (32-bits), IPV6 (128-bits).

## 8. Network Security
Importance: Protect data integrity, confidentiality, and availability.
Methods: Firewalls, encryption, secure protocols (SSL/TLS).

# Chapter Two

## 1. The Importance of Network Models

Purpose: Provide a framework for understanding the complex interactions in network architecture.
Benefits:
Standardization across different manufacturers.
Ensures compatibility and interoperability between devices.

## 2. The OSI Model (Open Systems Interconnection)
Layer 1: Physical: Deals with physical connections and transmission of raw bits.
Layer 2: Data Link: Responsible for node-to-node data transfer and error detection/correction.
Layer 3: Network: Manages data routing, forwarding, and addressing (IP addresses).
Layer 4: Transport: Ensures complete data transfer (TCP/UDP).
Layer 5: Session: Manages sessions and controls connections between computers.
Layer 6: Presentation: Translates data between application and network formats, encryption.
Layer 7: Application: Interfaces with the end-user applications.

## 3. The TCP/IP Model
Also known as the Internet Protocol Suite, it's a more practical model designed for internetworking.
Network Interface Layer: Equivalent to OSI’s physical and data link layers.
Internet Layer: Corresponds to OSI's network layer; manages logical device addressing (IP).
Transport Layer: Matches OSI’s transport layer, providing reliable data transfer.
Application Layer: Combines all OSI layers above the transport layer and provides application services.

## 4. Comparison of OSI and TCP/IP Models
Layer Count: OSI has 7 layers; TCP/IP has 4.
Development: OSI developed by ISO; TCP/IP developed by ARPANET.
Usage: TCP/IP is more commonly used for real-world Internet applications.

## 5. Encapsulation and Decapsulation
Encapsulation: Process of adding headers and trailers as data passes through layers (OSI or TCP/IP).
Decapsulation: Removing headers and trailers at the receiver’s end.

## 6. Protocol Data Units (PDUs)
Definition: The form that data takes at any layer.
OSI Model examples: Frames (Data Link), Packets (Network), Segments (Transport).

## 7. Addressing in Network Models
Importance: Unique addresses (e.g., IP or MAC) ensure data is delivered to the correct destination.
IP Address: Logical address in the Network layer.
MAC Address: Physical address in the Data Link layer.

# Chapter Three

## 1. Network Hardware Components

### Routers:

Purpose: Route data packets between different networks.
Functionality: Connects LANs and WANs; intelligent decision-making for path selection.
Example: Internet routers in homes connect the local devices to the ISP's network.

### Switches:

Purpose: Connect devices within a LAN, using MAC addresses to forward data to the correct destination.
Functionality: Operates at the Data Link layer, handling inter-device communication.
Example: In an office, a switch connects computers, printers, and servers.

### Hubs:

Purpose: Basic device to connect multiple Ethernet components.
Functionality: Broadcasts incoming packets to all ports, regardless of the destination.
Example: Older network setups; less efficient due to unnecessary traffic dissemination.

### Access Points:

Purpose: Allow wireless devices to connect to a wired network using Wi-Fi, or related standards.
Example: Used in homes and enterprises to cover areas where cabling might be impractical.

## 2. Network Mediums

### Wired:

Types include twisted pair cables (Ethernet), coaxial cables, and fiber optics.
Example: Ethernet cables (CAT5, CAT6) commonly used in networking installations.

### Wireless:

Uses radio waves, microwaves for data transmission.
Example: Wi-Fi (IEEE 802.11 standards), Bluetooth for short-range communication.

## 3. Network Interfaces and Ports

### Network Interface Cards (NICs):

Purpose: Allow devices to connect to a network either via a wired or wireless medium.
Example: Ethernet NIC for wired connections; Wireless NIC for Wi-Fi.

### Ports:

Functionality: Endpoints for network communication.
Example: Port 80 is used for HTTP traffic, while Port 443 is for HTTPS.

## 4. Transmission Concepts

### Bandwidth:

Definition: Maximum rate of data transfer across a network path.
Example: Measured in bits per second (bps), Mbps, or Gbps.

### Latency:

Definition: Time taken for a data packet to travel from source to destination.
Example: A satellite internet connection may have higher latency compared to wired broadband.

### Throughput:

Definition: Actual rate of successful data transfer through a network.
Example: A network may have a bandwidth of 100 Mbps but a throughput of 80 Mbps due to overheads and congestion.

## 5. Types of Data Transmission

### Unicast:

Definition: Data sent from one sender to one receiver.
Example: Browsing a website from a personal computer.

### Broadcast:

Definition: Data sent from one sender to all possible receivers in the network or network segment.
Example: Sending an email to multiple recipients.

### Multicast:

Definition: Data sent from one sender to multiple specific receivers.
Example: Video conferencing solutions.