# Transport Layer

## Transport Layer Kya Hai?

**Transport Layer** OSI model ki 4th layer (aur TCP/IP model ki 2nd layer) hai — **end-to-end communication** ke liye responsible, applications ke beech (process-to-process), na ki sirf devices ke beech.

> **Analogy**: Network Layer ek building tak courier pahunchata hai (host-to-host), Transport Layer building ke andar sahi flat/room tak deliver karta hai (process-to-process) — port numbers use karke.

## Key Characteristics

| Characteristic | Matlab |
|---|---|
| **End-to-End Layer** | Point-to-point connection deta hai (hop-to-hop nahi), source se destination tak |
| **Process-to-Process** | Port numbers use karke specific application tak data deliver karta hai |
| **Implemented Only in End Systems** | Intermediate routers mein nahi, sirf sender/receiver devices mein |
| **Data Unit** | Segment (TCP) ya Datagram (UDP) |

## Transport Layer Ke Main Functions

| Function | Matlab |
|---|---|
| **Segmentation** | Upar wali layers ka data segments/datagrams mein todta hai, headers add karta hai |
| **Multiplexing/Demultiplexing** | Port numbers se multiple applications ka data manage karta hai |
| **Error Detection** | Checksums se corrupted data detect karta hai |
| **Retransmission & Sequencing** | Lost data dobara bhejta hai, sahi order maintain karta hai (TCP mein) |
| **Flow Control** | Receiver overload na ho, iske liye rate control karta hai |
| **Reliable/Fast Delivery** | TCP (reliable) ya UDP (fast) — application ki zaroorat ke hisaab se |

## Main Protocols

| Protocol | Type | Use |
|---|---|---|
| **TCP** | Connection-oriented, reliable | Web browsing, email, file transfer |
| **UDP** | Connectionless, fast | Streaming, gaming, VoIP |
| **SCTP** | Message-oriented, multi-homing | Telephony signaling |

*(In sab protocols ka detail alag note files mein hai.)*

## TCP vs UDP (Quick Preview)

| TCP | UDP |
|---|---|
| Connection-oriented | Connectionless |
| Reliable | Fast, unreliable |
| Data phele connection establish hoti hai | Direct data bhej deta hai |

## Viva One-Liners

- **Q: Transport Layer ko "end-to-end layer" kyun kehte hain?**
 A: Kyunki ye point-to-point connection deta hai — source host se destination host tak, hop-to-hop nahi.
- **Q: Transport Layer kis unit mein data encapsulate karti hai?**
 A: Segment (TCP mein).
- **Q: Transport Layer sirf kahan implement hoti hai?**
 A: End systems mein — intermediate routers mein nahi.
