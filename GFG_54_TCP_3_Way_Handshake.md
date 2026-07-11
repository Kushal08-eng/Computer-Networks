# TCP 3-Way Handshake Process

## 3-Way Handshake Kya Hai?

**3-Way Handshake** TCP connection establish karne ka process hai — client aur server dono ko synchronize aur ready confirm karta hai, before actual data transfer shuru ho.

## 3 Steps

| Step | Segment | Kaun Bhejta Hai | Detail |
|---|---|---|---|
| **1** | **SYN** | Client → Server | Client apna Initial Sequence Number (ISN) bhejta hai, SYN flag = 1 |
| **2** | **SYN-ACK** | Server → Client | Server apna ISN bhejta hai, SYN=1 aur ACK = client_ISN + 1 |
| **3** | **ACK** | Client → Server | Client confirm karta hai — ACK = server_ISN + 1 |

Iske baad connection **ESTABLISHED** state mein aa jaata hai, aur actual data transfer shuru hota hai.

## TCP Flags Involved

| Flag | Kaam |
|---|---|
| **SYN** | Naya connection start karna |
| **ACK** | Message successfully receive hone ka confirmation |
| **RST** | Connection ko abruptly close karna (errors/security ki wajah se) |
| **FIN** | Connection ko gracefully close karna (termination ke liye) |

## Sequence Numbers Kyun Zaroori Hain

- Har byte ko unique sequence number milta hai — sahi order mein reassembly ke liye
- **Acknowledgement Number** batata hai receiver ka next expected byte
- Isse duplicate/missing data identify karna easy hota hai

## Common Issues Connection Establishment Mein

| Issue | Matlab |
|---|---|
| **SYN Flood Attack** | Attacker bahut saare SYN requests bhejta hai bina connection complete kiye — server overload ho jaata hai |
| **Connection Timeout** | Agar device time pe reply na kare, connection attempt fail ho jaata hai |

## Slow Start Algorithm Ka Connection

3-way handshake ke baad, TCP **Slow Start** congestion control algorithm invoke hota hai — congestion window (cwnd) ko gradually (exponentially) badhata hai, taaki network capacity ka accurate estimate mil sake.

## Viva One-Liners

- **Q: 3-way handshake ke 3 steps kya hain?**
 A: SYN (client→server) → SYN-ACK (server→client) → ACK (client→server).
- **Q: 3-way handshake kyun zaroori hai?**
 A: Dono ends confirm karte hain ki wo ready hain, aur initial sequence numbers exchange hote hain reliable data transfer ke liye.
- **Q: SYN Flood Attack kya hai?**
 A: Attacker bahut saare SYN requests bhejta hai bina connection complete kiye, server ke resources overload karne ke liye.
