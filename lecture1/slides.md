---
author: ""
date: ""
paging: "%d / %d"
---

# Assumptions

We don't deal with electronics.

00010101001011001011000...

---

# How to connect

```
💻╺━━━━━━━╸💻
```
* collision (CSMA/CD)
* start/end of packet

---

# How to connect

```
💻╺━━━┳━━━╸💻
      ┃
      ┃
      ╹
      💻
```
* addresses
* throughput
* collision (CSMA/CD)

---

# How to connect

```
💻╺━━━┳━━━╸💻
      ┃
      ┃
      ╹
      💻
```
* addresses
* throughput
* collision (CSMA/CD)

---

# How to connect

```
💻╺━━━┳━━━╸BRIDGE╺━━━┳━━━╸💻
      ┃              ┃      
💻╺━━━╋━━━╸BRIDGE╺━━━╋━━━╸💻
      ┃              ┃      
💻╺━━━┛              ┗━━━╸💻
```
* addresses
* throughput
* multiple routes
* fault tolerance

---

# How to connect

```
💻╺━━━┳━━━╸BRIDGE╺━━━━━━━╸💻
      ┃                     
💻╺━━━╋━━━╸BRIDGE╺━━━┳━━━╸💻
      ┃              ┃      
💻╺━━━┛              ┗━━━╸💻
```
* addresses
* throughput
* multiple routes
* fault tolerance

---

# Stack

* Ethernet
* IPv4
* TCP

---

# Ethernet frame

```
┏━━━━━━━━━━━━┓
┃  PREAMBLE  ┃
┣━━━━━━━━━━━━┫
┃ .......... ┃
┣━━━━━━━━━━━━┫
┃  TO (MAC)  ┃
┣━━━━━━━━━━━━┫
┃ FROM (MAC) ┃
┣━━━━━━━━━━━━┫
┃ .......... ┃
┣━━━━━━━━━━━━┫
┃  PAYLOAD   ┃
┣━━━━━━━━━━━━┫
┃ .......... ┃
┗━━━━━━━━━━━━┛
```

---

# Ethernet

MAC
```
❯ ip link show enp0s31f6 | grep link/ether
    link/ether e8:6a:64:41:d6:9a brd ff:ff:ff:ff:ff:ff
```

---

# IPv4 packet
```
┏━━━━━━━━━━━┓
┃ ......... ┃
┣━━━━━━━━━━━┫
┃   TTL     ┃
┣━━━━━━━━━━━┫
┃ PROTOCOL  ┃
┣━━━━━━━━━━━┫
┃  TO (IP)  ┃
┣━━━━━━━━━━━┫
┃ FROM (IP) ┃
┣━━━━━━━━━━━┫
┃ ......... ┃
┣━━━━━━━━━━━┫
┃  PAYLOAD  ┃
┣━━━━━━━━━━━┫
┃ ......... ┃
┗━━━━━━━━━━━┛
```

---

# IPv4 address

192.168.0.34

---

# hub vs. switch

---

# IP packet overview

---

# ARP

---

# IP subnet & router/gateway
