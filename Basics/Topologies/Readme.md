# Network Topologies

**Topology** is the layout or structure of how devices are connected in a network.

## 1. BUS Topology

### Description
All devices are connected to one single cable. Data travels along the cable, every device can listen, only one person can transfer at a time.

### Characteristics
- No privacy as all devices send data online
- We have to implement external security like password encryption

### Diagram
```
[PC1]---[PC2]---[PC3]---[PC4]---[PC5]
    \                           /
     \-------[Main Cable]------/
```

### Examples
- Early Ethernet networks (10Base2, 10Base5)
- Some industrial control systems
- Legacy office networks

---

## 2. STAR Topology

### Description
All devices connect to a central hub. The hub directly transfers data to the correct device.

### Diagram
```
        [PC1]
         |
[PC4]---[HUB]---[PC2]
         |
        [PC3]
```

### Examples
- Modern Ethernet networks with switches
- Home WiFi networks
- Office LAN networks

---

## 3. RING Topology

### Description
Devices are connected in a circle. Data travels in one direction around the ring until it reaches its destination.

### Diagram
```
    [PC1]----[PC2]
     |         |
     |         |
    [PC4]----[PC3]
```

### Examples
- Token Ring networks (IBM)
- FDDI (Fiber Distributed Data Interface)
- Some metropolitan area networks

---

## 4. MESH Topology

### Description
Every single device is connected to every single other computer. Very reliable, because even if some cables break, the data can take another path and still reach the destination computer.

### Diagram
```
    [PC1]----[PC2]
     |  \    /  |
     |   \  /   |
     |    \/    |
     |    /\    |
     |   /  \   |
     |  /    \  |
    [PC3]----[PC4]
```

### Examples
- Internet backbone networks
- Military communication systems
- Critical infrastructure networks

---

## 5. TREE Topology

### Description
Combination of star + bus topology. Hierarchical structure with multiple levels.

### Diagram
```
           [Root Hub]
          /     |     \
    [Hub1]    [Hub2]   [Hub3]
     / \       / \      / \
  [PC1][PC2][PC3][PC4][PC5][PC6]
```

### Examples
- Large corporate networks
- University campus networks
- Cable TV networks

---

## 6. HYBRID Topology

### Description
Combination of two or more different topologies.

### Diagram
```
  Star Section:        Ring Section:
     [PC1]              [PC5]--[PC6]
      |                  |      |
   [Switch]--[Router]---[PC7]--[PC8]
      |
     [PC2]    
   
  Bus Section:
  [PC3]---[PC4]---[Main Cable]
```

### Examples
- Modern enterprise networks
- Internet infrastructure
- Mixed office environments

---

## Comparison Table

| **Topology** | **Advantages** | **Disadvantages** | **Use Cases** | **Cost** |
|--------------|----------------|-------------------|---------------|----------|
| **Bus** | Simple, cost-effective | Single point of failure, no privacy | Small networks, legacy systems | Low |
| **Star** | Easy to manage, reliable | Central hub failure affects all | Modern LANs, offices | Medium |
| **Ring** | Equal access, no collisions | Break in ring stops network | Token networks, FDDI | Medium |
| **Mesh** | Highly reliable, multiple paths | Expensive, complex | Critical systems, backbone | High |
| **Tree** | Scalable, hierarchical | Root failure affects all | Large organizations | Medium-High |
| **Hybrid** | Flexible, combines benefits | Complex to design/manage | Enterprise networks | Variable |