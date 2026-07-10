# TCP (Transmission Control Protocol)

## TCP Kya Hai?

**TCP** ek transport layer protocol hai jo **reliable, ordered, aur error-checked** data delivery deta hai — internet ka sabse widely used protocol.

> **Analogy**: TCP registered post jaisa hai — pehle confirm karta hai ki dusri taraf koi receive karne ke liye ready hai (connection setup), phir data bhejta hai, aur confirmation leta hai ki sahi se pahuncha.

## TCP Ki Key Features

| Feature | Matlab |
|---|---|
| **Connection-Oriented** | Data bhejne se pehle connection establish hota hai (3-way handshake) |
| **Reliable** | Har packet ka acknowledgment milta hai, loss hone pe retransmit hota hai |
| **Ordered Delivery** | Packets sahi sequence mein deliver hote hain (sequence numbers se) |
| **Flow Control** | Receiver ke capacity ke hisaab se data bheja jaata hai |
| **Congestion Control** | Network congestion hone pe speed adjust karta hai |

## TCP Header Ke Important Fields

| Field | Kaam |
|---|---|
| Source/Destination Port | Application identify karta hai |
| Sequence Number | Data ka order maintain karta hai |
| Acknowledgment Number | Confirm karta hai kitna data receive hua |
| Flags (SYN, ACK, FIN) | Connection setup/close control karte hain |
| Window Size | Flow control ke liye |
| Checksum | Error detection |

## TCP vs UDP (Quick Recap)

| TCP | UDP |
|---|---|
| Reliable | Unreliable |
| Connection-oriented | Connectionless |
| Slower (overhead ki wajah se) | Faster |
| Example: Email, File transfer, Web browsing | Example: Streaming, Gaming |

## Viva One-Liners

- **Q: TCP reliable kaise hai?**
 A: Acknowledgment aur retransmission mechanism se — agar packet loss ho, dobara bheja jaata hai.
- **Q: TCP connection kaise start hoti hai?**
 A: 3-way handshake se.
