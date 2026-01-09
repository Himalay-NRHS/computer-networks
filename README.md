# Computer Networks - Complete Guide

A comprehensive guide to understanding computer networks, from basic infrastructure to the OSI and TCP/IP models.

---

## 📡 Internet Infrastructure

**Submarine Cables**: The backbone of the internet consists of cables laid under the sea, connecting continents and enabling global communication.

---

## 🔌 Network Media

**Media** in computer networks refers to the physical or wireless medium through which data is transmitted between devices (e.g., cables, fiber optics, radio waves).

---

## 📮 Address Types

| Address Type | Description | Example |
|--------------|-------------|---------|
| **Logical Address** | IP Address - Used for routing packets across networks | 192.168.1.1 |
| **Physical Address** | MAC Address - Unique hardware identifier | 00:1A:2B:3C:4D:5E |

---

## 🖥️ Network Devices

### Modem
Converts digital signals to analog signals (modulation) and vice versa (demodulation), enabling communication over telephone lines or cable systems.

### Router
Routes data packets between networks based on IP addresses, determining the best path for data transmission.

---

## 🌐 ISP (Internet Service Provider)

An **ISP** is a company that provides internet access to customers. ISPs are interconnected in a hierarchical structure.

### ISP Tier Structure in India

```
Tier-1 (Top Level)
└── TATA
    │
Tier-2 (Regional/National)
└── JIO, Airtel, VI, BSNL
    │
Tier-3 (Local)
└── Hathway, ACT Cable, Local broadband providers
```

- **Tier-1**: Backbone providers with global reach
- **Tier-2**: National/regional providers connected to Tier-1
- **Tier-3**: Local ISPs providing last-mile connectivity

---

## 🔢 IP Addresses & Ports

### IP Address (Internet Protocol)

**Format**: `x.x.x.x` where each x ranges from 0 to 255 (8 bits = 1 byte)

**Example**: `192.168.1.100`

**Find your IP**: 
```bash
curl ifconfig.me
```

### Ports

Think of ports as **doorways** to a house (computer). Just as a house has multiple doors, a computer has multiple ports.

- **Range**: 0 to 65,535 (~65k ports)
- **Purpose**: IP address identifies the device, port number identifies the specific application

#### Port Number Allocation

| Range | Purpose | Examples |
|-------|---------|----------|
| **0 - 1023** | System/Well-known ports | HTTP (80), HTTPS (443), FTP (21) |
| **1024 - 49151** | Registered ports | MongoDB (27017), MySQL (3306) |
| **49152 - 65535** | Dynamic/Private ports | Available for user applications |

**Common Ports**:
- HTTP → 80
- HTTPS → 443
- SSH → 22
- FTP → 21

---

## 📚 OSI Model (Open Systems Interconnection)

A **reference model** that standardizes communication between different computer systems by breaking it into **7 layers**.

### The 7 Layers (Bottom to Top)

```
7. APPLICATION LAYER    - User interfaces, web browsers
6. PRESENTATION LAYER   - Data formatting, encryption
5. SESSION LAYER        - Connection management
4. TRANSPORT LAYER      - End-to-end communication (TCP/UDP)
3. NETWORK LAYER        - Routing, IP addressing
2. DATA LINK LAYER      - Frame handling, MAC addresses
1. PHYSICAL LAYER       - Physical transmission (cables, signals)
```

### 🧠 Memory Trick

**Top to Bottom**:
```
All          - APPLICATION
People       - PRESENTATION
Should       - SESSION
Try          - TRANSPORT
New          - NETWORK
Dominos      - DATA LINK
Pizza        - PHYSICAL
```

**Bottom to Top**:
```
Please       - PHYSICAL
Do           - DATA LINK
Not          - NETWORK
Throw        - TRANSPORT
Sausage      - SESSION
Pizza        - PRESENTATION
Away         - APPLICATION
```

---

## 🌍 TCP/IP Model

The **practical model** used in real-world networking, simplifying the OSI model into **4 layers**.

### The 4 Layers

```
4. APPLICATION LAYER
   ├── Combines OSI's Application Layer
   ├── Presentation Layer
   └── Session Layer
   └── (Browsers handle all three)

3. TRANSPORT LAYER
   └── Same as OSI (TCP/UDP)

2. NETWORK LAYER
   └── Same as OSI (IP routing)

1. PHYSICAL LAYER
   ├── Combines OSI's Data Link Layer
   └── Physical Layer
```

### Why TCP/IP Over OSI?

- **Simpler**: Fewer layers make it more practical
- **Real-world usage**: The internet runs on TCP/IP
- **Browser efficiency**: Modern browsers handle multiple OSI layers together

---

## 🔑 Key Protocols & Concepts

### TCP (Transmission Control Protocol)
- Connection-oriented protocol
- Ensures reliable data delivery
- Used for web browsing, email, file transfers

### HTTP (HyperText Transfer Protocol)
- Protocol for communication between web clients and servers
- Port 80 (HTTP), Port 443 (HTTPS)

### WWW (World Wide Web)
- **Founder**: Tim Berners-Lee
- A system of interlinked web pages accessed via the internet using browsers
- Built on HTTP protocol

---

## 📊 OSI vs TCP/IP Comparison

| Aspect | OSI Model | TCP/IP Model |
|--------|-----------|--------------|
| **Layers** | 7 | 4 |
| **Type** | Reference/Theoretical | Practical/Implementation |
| **Development** | ISO Standard | DARPA/DoD |
| **Usage** | Educational purposes | Real-world internet |
| **Protocol dependency** | Protocol independent | Protocol specific |

---

## 🎯 Quick Reference

### Layer Functions (OSI)

1. **Physical**: Bits, cables, signals
2. **Data Link**: Frames, MAC addresses, switches
3. **Network**: Packets, IP addresses, routers
4. **Transport**: Segments, TCP/UDP, ports
5. **Session**: Connection establishment/termination
6. **Presentation**: Encryption, compression, formatting
7. **Application**: HTTP, FTP, SMTP, DNS

### Data Units by Layer

| Layer | Data Unit |
|-------|-----------|
| Application | Data |
| Transport | Segment |
| Network | Packet |
| Data Link | Frame |
| Physical | Bits |

---

## 📝 Additional Resources

- **Check your IP**: `curl ifconfig.me`
- **OSI Model**: Reference for understanding network communication
- **TCP/IP Model**: Practical implementation used today

---

**Remember**: The internet is simply a vast network of interconnected computers communicating using standardized protocols! 🌐
