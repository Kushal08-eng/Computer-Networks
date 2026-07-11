# Session Layer

## Session Layer Kya Hai?

**Session Layer** OSI model ki **5th layer** hai — applications ke beech **sessions** establish, manage, synchronize, aur terminate karti hai.

> **Analogy**: Jaise ek phone call mein pehle connect hota hai ("hello"), baat hoti hai, aur phir properly disconnect hota hai ("bye") — Session Layer bhi devices ke beech ek meaningful "dialogue" set up karti hai, organized rakhti hai, aur properly close karti hai.

## Session Layer Ke Kaam

| Kaam | Matlab |
|---|---|
| **Session Setup** | Communicating parties ke beech connection establish karna |
| **Session Maintenance** | Session ko active/organized rakhna, lambi ya complex data transfers ke dauran bhi |
| **Dialogue Control** | Decide karta hai kiska "turn" hai data bhejne/receive karne ka |
| **Session Termination** | Communication complete hone pe session properly close karna |

## Important Note (Modern Networks Mein)

Modern **TCP/IP** networks mein Session Layer ke kuch functions (jaise session release, dialogue control) **Transport Layer (TCP)** ya **Application Layer** handle kar leti hain — isliye Session Layer ka independent role kam ho gaya hai TCP/IP model mein (jismein ye alag layer bhi nahi hai).

## Session Layer Ke Protocols

| Protocol | Kaam |
|---|---|
| **RPC (Remote Procedure Call Protocol)** | Program ko dusre address space mein procedures execute karne deta hai (client-server interaction) |
| **PPTP (Point-to-Point Tunneling Protocol)** | VPNs (Virtual Private Networks) enable karta hai TCP/IP ke upar |
| **PAP (Password Authentication Protocol)** | Password-based authentication PPP connections mein |
| **SDP (Sockets Direct Protocol)** | RDMA-enabled networks pe socket communication support karta hai |

*(RPC aur PPTP ka detail alag note files mein hai.)*

## Session Layer Se Related Devices

| Device | Kaam |
|---|---|
| **Firewalls** | Security ke liye sessions monitor/control karte hain |
| **Proxy Servers** | Client-server ke beech intermediary, sessions manage karte hain |
| **Session Border Controllers (SBCs)** | VoIP sessions secure aur manage karte hain |

## Viva One-Liners

- **Q: Session Layer OSI ki kaunsi layer hai?**
 A: 5th layer.
- **Q: Session Layer ka main kaam kya hai?**
 A: Applications ke beech sessions establish, manage, synchronize, aur terminate karna.
- **Q: Modern TCP/IP networks mein Session Layer ka role kam kyun hai?**
 A: Kyunki iske kuch functions (session release, dialogue control) TCP (Transport Layer) ya Application Layer handle kar leti hain.
