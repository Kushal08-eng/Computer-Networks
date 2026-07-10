# TCP/IP Model — Transport Layer

## Transport Layer Ka Kaam

Transport Layer responsible hai **end-to-end data delivery** ke liye — ek device ke specific application se dusre device ke specific application tak.

## Key Responsibilities

| Responsibility | Matlab |
|---|---|
| **Segmentation** | Data ko chhote segments mein todna |
| **Multiplexing/Demultiplexing** | Multiple applications ka data port numbers se manage karna |
| **Reliability** (TCP mein) | Data sahi order mein aur bina loss ke pahunche ensure karna |
| **Flow Control** | Sender itni speed se bheje ki receiver handle kar sake |
| **Error Detection** | Checksum se check karna data corrupt to nahi hua |

## Do Main Protocols

| Protocol | Type | Use Case |
|---|---|---|
| **TCP** | Reliable, connection-oriented | Email, file transfer, web browsing |
| **UDP** | Fast, connectionless | Video streaming, gaming, voice calls |

## Multiplexing/Demultiplexing Ka Concept

Transport layer **port numbers** use karke decide karta hai data kaunsi application tak jaana hai — isse ek device pe multiple applications simultaneously network use kar paate hain.

> **Analogy**: Ek office building (device) mein multiple companies (applications) kaam karti hain. Transport layer receptionist jaisa hai jo decide karta hai konsi courier (data) konsi company (application) tak jaani hai — floor/room number (port) dekhke.

## Viva One-Liners

- **Q: Transport layer ka main kaam kya hai?**
 A: End-to-end data delivery, applications ke beech (port numbers use karke).
- **Q: Transport layer ke 2 main protocols?**
 A: TCP aur UDP.
