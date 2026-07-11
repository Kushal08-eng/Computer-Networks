# QUIC Protocol (Quick UDP Internet Connections)

## QUIC Kya Hai?

**QUIC** ek transport layer protocol hai jo web communication ko **faster aur more reliable** banata hai — **UDP ke upar** kaam karta hai, but TCP jaisi reliability aur built-in security (TLS) dono deta hai.

> HTTP/2 = TCP + TLS (multiple handshakes, zyada latency)
> HTTP/3 = QUIC (single handshake, low latency)

## TCP + TLS Ki Problem

Traditional web communication (TCP + TLS) mein connection setup ke liye **multiple round trips** lagte hain:

1. **TCP 3-Way Handshake**: SYN → SYN-ACK → ACK (1 round trip)
2. **TLS/SSL Handshake**: Certificate verification ke liye (1 aur round trip, agar HTTPS ho)

Total: **kam se kam 2 round trips** — jitna zyada latency, utna slow connection setup.

## QUIC Isse Kaise Solve Karta Hai

QUIC **transport aur encryption dono ko ek hi handshake mein merge** kar deta hai:

| Fayda | Matlab |
|---|---|
| **Fewer Round Trips** | Setup ke liye kam time lagta hai |
| **Encrypted by Default** | Security built-in hai, alag se TLS handshake nahi chahiye |
| **Faster Page Load Times** | Overall latency kam ho jaati hai |

## QUIC Reliability Kaise Deta Hai (UDP Pe Hote Hue Bhi)

Traditionally UDP unreliable hota hai — QUIC ismein extra mechanisms add karta hai:

- **Packet Sequencing**
- **Acknowledgments**
- **Retransmissions**

> Isse UDP effectively "reliable" ban jaata hai — TCP jaise guarantees ke saath, but UDP ki speed ke saath.

## QUIC Ke Key Fayde

| Fayda | Matlab |
|---|---|
| **Single Handshake** | Transport + encryption dono ek saath establish hote hain |
| **Multiplexing** | Multiple streams ek connection mein — ek stream ka issue doosre ko block nahi karta (TCP mein "head-of-line blocking" hoti thi) |
| **Better Mobile Performance** | Connection migration support karta hai (jaise WiFi se mobile data switch karna, bina connection tod ke) |

## Viva One-Liners

- **Q: QUIC kis protocol ke upar based hai?**
 A: UDP.
- **Q: QUIC, TCP+TLS se fast kyun hai?**
 A: Kyunki QUIC transport aur encryption handshake ko ek hi step mein combine kar deta hai, jabki TCP+TLS mein alag-alag multiple round trips lagte hain.
- **Q: HTTP/3 kis protocol pe based hai?**
 A: QUIC.
