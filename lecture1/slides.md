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

# Stack

* Ethernet
* IP
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
┃ .......... ┃
┣━━━━━━━━━━━━┫
┃  PAYLOAD   ┃
┣━━━━━━━━━━━━┫
┃ .......... ┃
┗━━━━━━━━━━━━┛
```

---

# Ethernet

* shared medium
* collision detection (CSMA/CD)

---

# packet overview



---

# MAC

---

# hub vs. switch

---

# IP packet overview

---

# ARP

---

# IP subnet & router/gateway
