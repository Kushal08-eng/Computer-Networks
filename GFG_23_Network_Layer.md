# Network Layer

## Network Layer Kya Hai?

**Network Layer** OSI model ki **3rd layer** hai — logical addressing, routing, aur interconnected networks ke across **end-to-end packet delivery** ke liye responsible.

> **Note**: Data Link Layer sirf **same network segment** ke andar node-to-node delivery dekhta hai; Network Layer ensure karta hai ki data source host se destination host tak pahunche, **chahe wo alag-alag networks pe hi kyun na ho**.

## Key Responsibilities

| Responsibility | Matlab |
|---|---|
| **Logical Addressing** | Har device ko unique IP address assign karta hai — accurate identification aur communication ke liye |
| **Packetization** | Transport layer se aaye segments ko packets mein encapsulate karta hai |
| **Host-to-Host Delivery** | Sender se intended receiver tak, alag-alag networks ke across reliable delivery ensure karta hai |
| **Forwarding** | Router ke input interface se sahi output interface tak packets move karta hai, destination IP ke basis pe |

## Network Layer Kaise Kaam Karta Hai (Flow)

1. Har device ko ek unique **logical address (IP address)** assign hota hai
2. Transport layer se aaya data **packets** mein encapsulate hota hai, source-destination IPs ke saath
3. **Routers** destination address analyze karke best available path decide karte hain
4. Packets **hop-by-hop** travel karte hain, routers se guzarte hue, jab tak destination na pahunch jaayein
5. Agar packet size **MTU** (Maximum Transmission Unit) se zyada ho, to **fragment** ho jaata hai chhote units mein
6. Destination pe fragments wapas **reassemble** hote hain original data banane ke liye
7. Agar error aaye (jaise destination unreachable), to **ICMP** jaise protocols error messages source ko wapas bhejte hain

## Key Protocols

| Protocol | Kaam |
|---|---|
| **IP (IPv4/IPv6)** | Logical addressing deta hai, packets ko networks ke across deliver karta hai |
| **ICMP** | Error reports aur diagnostic messages bhejta hai (jaise destination unreachable, ping) |

## Network Layer Ki Limitations

| Limitation | Matlab |
|---|---|
| No Flow Control | Congestion ho sakti hai agar bahut zyada datagrams transit mein hon |
| Limited Error Control | Reliability ke liye mainly upper layers pe depend karta hai |
| Packet Drop Risk | Heavy load mein routers packets drop kar sakte hain |
| Fragmentation Overhead | Fragmentation processing overhead add karta hai, performance affect kar sakta hai |

## Viva One-Liners

- **Q: Network Layer aur Data Link Layer mein basic difference kya hai?**
 A: Data Link Layer sirf same network segment ke andar delivery karta hai, Network Layer alag-alag networks ke across end-to-end delivery ensure karta hai.
- **Q: Network Layer ke 4 main responsibilities kya hain?**
 A: Logical Addressing, Packetization, Host-to-Host Delivery, aur Forwarding.
- **Q: Fragmentation kab hoti hai?**
 A: Jab packet size destination network ke MTU se zyada ho.
