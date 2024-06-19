---
author: ""
date: ""
paging: "%d / %d"
---

# Networks
```
   _______________                        |*\_/*|________
  |  ___________  |     .-.     .-.      ||_/-\_|______  |
  | |           | |    .****. .****.     | |           | |
  | |   0   0   | |    .*****.*****.     | |   0   0   | |
  | |     -     | |     .*********.      | |     -     | |
  | |   \___/   | |      .*******.       | |   \___/   | |
  | |___     ___| |       .*****.        | |___________| |
  |_____|\_/|_____|        .***.         |_______________|
    _|__|/ \|_|_.............*.............._|________|_
   / ********** \                          / ********** \
 /  ************  \                      /  ************  \
--------------------                    --------------------
```

---

# Assumptions

We don't deal with electronics.

00010101001011001011000...

---

# How to connect

```
💻╺━━━━━━━╸💻
```

---

# How to connect

```
💻╺━━━━━━━╸💻
```
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
💻╺━━━*━━━╸💻
      ┃
      ┃
      ╹
      💻
```
* addresses
* throughput
* collision (CSMA/CD)

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

# MAC (Medium Access Control)

```
❯ ip link show enp0s31f6 | grep link/ether
    link/ether e8:6a:64:41:d6:9a brd ff:ff:ff:ff:ff:ff
```

---

# MAC (Medium Access Control)

```
❯ ip link show enp0s31f6 | grep link/ether
    link/ether e8:6a:64:41:d6:9a brd ff:ff:ff:ff:ff:ff
```

`e8:6a:64`
LCFC(HeFei) Electronics Technology co., ltd

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

# Internet 🌐
```
💻╺━━━┳━━━╸BRIDGE╺━╸BRIDGE╺━━━━━━╸💻
      ┃ 
💻╺━━━╋━━━╸BRIDGE╺┳╸BRIDGE╺━━━━━━╸💻
      ┃           ┃
💻╺━━━╋━━━╸BRIDGE╺┻╸BRIDGE╺━━┳━━━╸💻
      ┃                      ┃
💻╺━━━╋━━━╸BRIDGE╺┳╸BRIDGE╺━━╋━━━╸BRIDGE╺━━━┳━━━╸💻
      ┃           ┃          ┃              ┃
💻╺━━━┛           ╹          ┣━━━╸💻  💻╺━━━┛
                  💻         ┃
                             ┣━━━╸💻
         💻╺━━┳━━━╸BRIDGE╺━━━┛
              ╹
              💻
---

# IPv4 packet
```
┏━━━━━━━━━━━┓
┃ ......... ┃
┣━━━━━━━━━━━┫
┃    TTL    ┃
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
```
     192.     168.       0.      34
11000000.10101000.00000000.00100010
```

---

# IPv4 address
```
     192.     168.       0.      34
11000000.10101000.00000000.00100010
11111111.11111111.11111111.00000000
     255.     255.     255.       0
```

---

# IPv4 address
```
     192.     168.       0.      34
11000000.10101000.00000000.00100010
11111111.11111111.11111000.00000000
     255.     255.     248.       0
```

---

# IPv4 address ❌
```
     192.     168.       0.      34
11000000.10101000.00000000.00100010
11111111.11111111.00111000.00000000
     255.     255.      56.       0
```

---

# IPv4 address
```
     192.     168.       0.      34
11000000.10101000.00000000.00100010
11111111.11111111.11111000.00000000
     255.     255.     248.       0
```

192.168.0.34/21

---

# ARP (Address Resolution Protocol)
```
192.168.0.1 -> e8:6a:64:41:d6:9a
```

---

# Routing

```
  💻
  ╻ 192.168.0.34/24
  ┃
  ┃
  ╹ 192.168.0.1/24
BRIDGE
  ╻ 10.0.0.52/16
  ┃
  ┃
  ╹ 10.0.0.74/16
  💻
```

---

# DHCP (Dynamic Host Configuration Protocol)

```
CLIENT                                 SERVER

 ----------------- DISCOVER --------------->
  FROM: e8:6a:64:41:d6:9a /   0.  0.  0.  0
  TO:   ff:ff:ff:ff:ff:ff / 255.255.255.255
```

---

# DHCP (Dynamic Host Configuration Protocol)

```
CLIENT                                 SERVER

 <----------------- OFFER ------------------
  FROM: 52:54:00:2d:6f:e1 / 192.168.  0.  1
  TO:   e8:6a:64:41:d6:9a / 192.168.  0. 21
    subnet mask: 255.255.255.255
    DHCP server: 192.168.  0.  1
    router:      192.168.  0.  2
    DNS:           8.  8.  8.  8
                   8.  8.  4.  4
    lease time:  86400 seconds
```

---

# DHCP (Dynamic Host Configuration Protocol)

```
CLIENT                                 SERVER

 ----------------- REQUEST ---------------->
  FROM: e8:6a:64:41:d6:9a /   0.  0.  0.  0
  TO:   ff:ff:ff:ff:ff:ff / 255.255.255.255
    address:     192.168.  0. 21 
    DHCP server: 192.168.  0.  1
```

---

# DHCP (Dynamic Host Configuration Protocol)

```
CLIENT                                 SERVER

 <------------------ ACK -------------------
  FROM: 52:54:00:2d:6f:e1 / 192.168.  0.  1
  TO:   e8:6a:64:41:d6:9a / 192.168.  0. 21
    subnet mask: 255.255.255.255
    DHCP server: 192.168.  0.  1
    router:      192.168.  0.  2
    DNS:           8.  8.  8.  8
                   8.  8.  4.  4
    lease time:  86400 seconds
```
