# TCP/IP Model — Network Layer

## Network Layer Ka Kaam

Network Layer responsible hai **routing** aur **logical addressing (IP address)** ke liye — data ko source se destination tak, chahe different networks ke through hi kyun na jaana pade.

## Key Responsibilities

| Responsibility | Matlab |
|---|---|
| **Logical Addressing** | Har device ko IP address se identify karna |
| **Routing** | Best path decide karna data ko destination tak pahunchane ke liye |
| **Packet Forwarding** | Router se router data forward karna |
| **Fragmentation** | Bade data ko chhote packets mein todna agar zaroorat ho |

## Main Protocol: IP (Internet Protocol)

Network layer ka sabse important protocol **IP** hai, jo addressing aur routing dono handle karta hai.

## Routing Kaise Kaam Karta Hai (Simple)

- Har router ke paas ek **routing table** hoti hai jo batati hai kis destination ke liye kaunsa raasta best hai
- Data packet har router pe apna next-hop decide karta hai jab tak destination na pahunch jaaye

> **Analogy**: Jaise Google Maps decide karta hai kaunsa route fastest hai — routers bhi similar tareeke se decide karte hain data ka best path.

## Viva One-Liner

> "Network layer ka kaam hai logical addressing (IP) aur routing — data ko sahi raaste se destination network tak pahunchana."
