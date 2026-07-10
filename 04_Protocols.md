# Protocols

## Protocol Kya Hai?

**Protocol** rules ka wo set hai jo decide karta hai devices aapas mein data kaise bhejenge, receive karenge, aur samjhenge.

> **Analogy**: Do log tabhi baat kar sakte hain jab dono same language bolte hon. Protocol wahi "common language" hai jo devices ke beech follow hoti hai.

## Protocol Ke 3 Core Elements

| Element | Matlab |
|---|---|
| **Syntax** | Data ka format/structure kaisa hoga |
| **Semantics** | Har field ka matlab kya hai |
| **Timing** | Data kab aur kis speed se bheja jaayega |

## Protocol Zaroori Kyun Hai

- Different companies/devices bina common rule ke communicate nahi kar sakte
- Error handling, addressing, aur data sequencing sab protocol define karta hai
- Standardization se poori duniya ke devices aapas mein connect ho paate hain

## Common Protocols Overview

| Protocol | Kaam |
|---|---|
| **TCP** | Reliable data delivery |
| **UDP** | Fast, unreliable delivery |
| **IP** | Addressing aur routing |
| **HTTP/HTTPS** | Web browsing |
| **FTP** | File transfer |
| **SMTP** | Email bhejna |
| **DNS** | Domain name → IP conversion |
| **DHCP** | Automatic IP assignment |

## Protocol Stack/Layers Ka Idea

Networking mein protocols **layers** mein organize hote hain (jaise OSI ya TCP/IP model) — har layer ka apna specific protocol aur responsibility hoti hai. Ek layer ka protocol sirf apna kaam karta hai, aur data ko next layer ko pass kar deta hai.

> **Analogy**: Factory mein assembly line — har station (layer) apna specific kaam karta hai (screw lagana, paint karna) aur product ko next station ko pass kar deta hai.

## Viva One-Liners

- **Q: Protocol define karo.**
 A: Rules ka set jo network devices ke beech communication govern karta hai.
- **Q: Protocol ke 3 elements kaunse hain?**
 A: Syntax, Semantics, Timing.
