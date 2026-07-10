# TCP/IP Model — Data Link Layer

## Data Link Layer Ka Kaam

Data Link Layer responsible hai **same local network** ke andar devices ke beech data transfer ke liye — physical addressing aur error detection karta hai.

## Key Responsibilities

| Responsibility | Matlab |
|---|---|
| **Physical Addressing (MAC)** | Har device ka unique MAC address use karke local delivery |
| **Framing** | Data ko "frames" mein organize karna |
| **Error Detection** | Transmission errors detect karna (CRC jaise techniques se) |
| **Flow Control** | Sender-receiver ke beech speed match karna local level pe |

## MAC Address Kya Hai?

**MAC (Media Access Control) Address** har network device ka **unique, hardware-level** address hota hai (jaise `00:1A:2B:3C:4D:5E`) — ye device ke network card mein fixed hota hai (physically burned in).

> **Analogy**: MAC address jaise tumhara Aadhaar number hai — permanent aur unique, chahe tum kahin bhi raho. IP address tumhare current address jaisa hai — jo change ho sakta hai jagah ke hisaab se.

## MAC Address vs IP Address

| MAC Address | IP Address |
|---|---|
| Physical/hardware address | Logical address |
| Permanent (device ke saath fixed) | Change ho sakta hai (network ke hisaab se) |
| Local network ke andar use hota hai | Global routing ke liye use hota hai |
| Data Link Layer | Network Layer |

## Switch Ka Role Yahan

**Switch** data link layer pe kaam karta hai — ye MAC addresses ka use karke decide karta hai frame kis specific device tak bhejni hai (na ki sabko broadcast karna, jaise Hub karta hai).

## Viva One-Liners

- **Q: Data Link layer kaunsa addressing use karta hai?**
 A: MAC (physical) address.
- **Q: MAC address aur IP address mein basic difference?**
 A: MAC address hardware-level, permanent hota hai; IP address logical, changeable hota hai.
