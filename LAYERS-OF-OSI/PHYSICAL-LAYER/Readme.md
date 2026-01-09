# PHYSICAL LAYER (Layer 1)

This layer deals with the raw physical bits.
It's the **medium** where the data transmits (like wires, WiFi, etc.)


## Key Concepts
**Bits** → Signals

## Encoding Methods
### Manchester Encoding
At the middle of the clock cycle:
- If the curve is going **up** → means **1**
- If the curve is going **down** → means **0**

## Transmission Media
### Guided Media
- **Twisted Pair Cable** - 
- **Coaxial Cable** - 
- **Fiber Optic Cable** - 

### Unguided Media
- **Radio Waves** - 
- **Microwaves** - 
- **Infrared** - 

## Functions of Physical Layer

### 1. Bit Transmission (Data Encoding & Signaling)
Converts digital data (0s & 1s) into signals (electrical, optical, or radio).

**Examples:**
- **Copper cables** → voltages
- **Fiber optic** → light pulses  
- **Wireless** → radio waves

### 2. Data Rate Control
Defines how many bits per second can be transmitted (bandwidth).

**Examples:**
- 100 Mbps Ethernet
- 1 Gbps Ethernet

### 3. Synchronization
Ensures sender and receiver are aligned so bits are read correctly (clock synchronization).
- Prevents misinterpretation of bit boundaries

### 4. Physical Topology
Defines how devices are physically connected (bus, star, ring, mesh).

---

## 📬 **Analogy: Physical Layer as Mail System**

**Physical Layer** = "hardware layer" that defines how raw bits actually move across wires/waves

**Imagine sending a letter:**

| **Component** | **Network Equivalent** |
|---------------|------------------------|
| Your message (data) | The actual content |
| Envelope (frame) | Structured packaging with sender/receiver info |
| Mail truck/airplane | The network medium |
| **Physical Layer** | The road/rail/air route + fuel + vehicle engine that actually moves the letter physically |

### 👉 **Key Points:**

The Physical Layer doesn’t care what’s inside the letter.

It just makes sure something moves from point A to point B as signals.

Defines how fast the truck goes, which road it uses, and what kind of fuel it runs on.

That’s why it’s called the “hardware transmission layer” — wires, voltages, light pulses, radio signals = its job.

---

## Transmission Modes

### 1. Simplex
**One-way communication only**
```
Device A  ------>  Device B
```
**Examples:** Radio broadcasting, TV transmission

### 2. Half Duplex
**Two-way communication, but not simultaneously**
```
Device A  <----->  Device B
(one direction at a time)
```
**Examples:** Walkie-talkies, old Ethernet hubs

### 3. Full Duplex
**Two-way communication simultaneously**
```
Device A  <=====>  Device B
(both directions at once)
```
**Examples:** Modern Ethernet switches, telephone calls

---
*Add more physical layer details here*
