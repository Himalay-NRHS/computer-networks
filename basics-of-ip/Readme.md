# Computer Networks – Clean 3‑Day Notes

This document compiles **all computer networks concepts discussed over the last 3 days**, arranged **from first principles → real-world usage**.

No repetition. Logical order. Meant to be read end-to-end.

---

## 1. What an IP Address Really Is

An **IP address** is a logical identifier for a device in a network.

Two scopes:

* **Private IP** → valid only inside a local network
* **Public IP** → globally unique on the internet

Key rule:

* Multiple devices **can share the same private IP** across different networks
* **Public IPs must be unique**

Why?
Because routers on the internet only understand public IPs.

---

## 2. Private vs Public IP (First Principles)

### Private IP

* Assigned inside LAN (college, home, office)
* Examples:

  * 10.0.0.0 – 10.255.255.255
  * 172.16.0.0 – 172.31.255.255
  * 192.168.0.0 – 192.168.255.255

Used for:

* Device-to-device communication **inside the same network**

### Public IP

* Assigned by ISP
* Used for communication **over the internet**

---

## 3. Why NAT Exists

**Problem**: IPv4 addresses are limited.

**Solution**: NAT (Network Address Translation)

How it works:

* Internal devices use **private IPs**
* Router has **one public IP**
* Router rewrites packets:

  * Outgoing: private → public
  * Incoming: public → correct private device

This is why:

* Internet can reach your router
* Router decides which internal device gets the packet

---

## 4. DHCP – How Devices Get IPs Automatically

**DHCP = Dynamic Host Configuration Protocol**

Purpose:

* Automatically assigns:

  * IP address
  * Subnet mask
  * Default gateway
  * DNS server

Process (DORA):

1. Discover
2. Offer
3. Request
4. Acknowledge

This happens:

* When you connect to WiFi
* When you enable mobile data

Yes, **mobile networks also use DHCP-like mechanisms**.

---

## 5. Subnet Mask – How a Device Knows Local vs Internet

Subnet mask splits IP into:

* **Network part**
* **Host part**

Example:

```
IP:        192.168.1.10
Subnet:    255.255.255.0  (/24)
Network:   192.168.1.0
```

Rule:

* Same network → send directly
* Different network → send to gateway

This decision is made **by the client itself**, not the router.

---

## 6. Local Packet Flow (Very Important)

If two devices:

* Are on the same subnet
* Share same network address

Then packet flow is:

```
Device A → Switch → Device B
```

No router involved.
No internet involved.

This is why:

* You can ping private IPs in the same WiFi
* LAN games work without internet

---

## 7. When Packets Go to the Gateway

If destination IP is **outside subnet**:

Flow:

```
Device → Default Gateway → ISP → Internet
```

Example:

* Google.com
* Any public IP

Gateway is **mandatory** for internet access.

---

## 8. Network Address and Broadcast Address

For every subnet:

### Network Address

* Host bits = all 0
* Identifies the network itself

Example:

```
192.168.1.0
```

Used by:

* Routers
* Routing tables

Cannot be assigned to a device.

---

### Broadcast Address

* Host bits = all 1

Example:

```
192.168.1.255
```

Used for:

* DHCP discovery
* ARP requests
* Sending message to **all devices in subnet**

Cannot be assigned to a device.

---

## 9. ARP – How Local Delivery Actually Happens

ARP = Address Resolution Protocol

Problem:

* IP is logical
* Ethernet works on MAC addresses

Solution:

* ARP maps IP → MAC

Process:

1. Broadcast: "Who has 192.168.1.5?"
2. Reply: "I do"
3. Packet sent using MAC

---

## 10. DNS – What It Really Does

DNS maps:

```
Domain name → IP address
```

DNS does **NOT**:

* Host websites
* Serve content

It only answers: "What is the IP?"

---

## 11. DNS Resolution Flow (Complete)

Steps:

1. Browser asks local DNS
2. Local DNS asks Root server
3. Root → TLD (.com)
4. TLD → Authoritative nameserver
5. Authoritative → IP address

Result returned to client.

---

## 12. Registrar vs DNS Provider vs Hosting

### Registrar

* Where domain is purchased
* Controls **nameservers**

### DNS Provider (e.g. Cloudflare)

* Stores DNS records
* Handles domain → IP mapping

### Hosting Server

* Actually serves website content

Changing nameservers means:

* Registrar points domain authority to DNS provider

---

## 13. DNS Records Explained

Common records:

* **A** → domain → IPv4
* **AAAA** → domain → IPv6
* **CNAME** → alias to another domain
* **MX** → mail server
* **TXT** → verification / metadata

These live inside **DNS provider**, not ISP.

---

## 14. Multiple DNS Servers Don’t Break Internet

If:

* DHCP gives DNS = 8.8.8.8
* Domain uses Cloudflare

Still works because:

* DNS servers cooperate via hierarchy
* They query authoritative servers when needed

DNS is **distributed, not centralized**.

---

## 15. College / Captive Portal Networks

Observed behavior:

* Many access points
* One central internet connection
* Login page before internet works

What actually happens:

* You get private IP
* Gateway intercepts traffic
* Until authentication succeeds

After login:

* Router allows packets to pass to internet

---

## 16. Can You Ping Friend’s Private IP?

YES if:

* Same subnet
* Same LAN

NO if:

* Different networks
* Over internet

Private IPs are **not routable on the internet**.

---

## 17. How to Send Message to Friend by IP

Options:

* Ping → ICMP (only reachability)
* TCP/UDP → needs server listening

Example:

* Chat app
* Socket program
* HTTP server

IP alone is not enough.
A **service + port** is required.

---

## 18. Key Mental Model (Final)

* Subnet mask decides **local vs remote**
* ARP handles **local delivery**
* Gateway handles **external delivery**
* NAT enables internet sharing
* DNS only resolves names



---

**End of Notes**
