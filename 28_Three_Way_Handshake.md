# 3-Way Handshake

## Kya Hai?

**3-Way Handshake** TCP connection establish karne ka process hai — ye ensure karta hai ki dono devices data bhejne/receive karne ke liye ready hain, pehle actual data transfer shuru ho.

> **Analogy**: Ek phone call karne se pehle:
> 1. Tum call karte ho: "Hello, sun rahe ho?" (**SYN**)
> 2. Dusra bandha reply karta hai: "Haan, sun raha hoon, tum sunn rahe ho?" (**SYN-ACK**)
> 3. Tum confirm karte ho: "Haan sun raha hoon" (**ACK**)
>
> Ab dono confirm hain ki connection ready hai, baat (data) shuru ho sakti hai.

## 3 Steps

| Step | Kaun Bhejta Hai | Flag | Matlab |
|---|---|---|---|
| 1 | Client → Server | **SYN** | "Mai connection start karna chahta hoon" |
| 2 | Server → Client | **SYN-ACK** | "Theek hai, mai bhi ready hoon" |
| 3 | Client → Server | **ACK** | "Great, ab connection establish ho gaya" |

Iske baad **actual data transfer** shuru hota hai.

## Kyun Zaroori Hai

- Dono devices confirm kar lete hain ki dusri taraf koi hai aur ready hai
- Initial **sequence numbers** exchange hote hain jo data ordering ke liye use honge

## Connection Termination (Bonus)

TCP connection close karne ke liye **4-way handshake** use hota hai (FIN, ACK, FIN, ACK) — dono taraf se independently connection close karne ka confirmation hota hai.

## Viva One-Liners

- **Q: 3-way handshake ke 3 steps kaunse hain?**
 A: SYN → SYN-ACK → ACK.
- **Q: 3-way handshake kyun zaroori hai?**
 A: Connection establish karne ke liye, taaki dono devices data exchange ke liye ready hon.
