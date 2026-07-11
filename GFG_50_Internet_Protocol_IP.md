# Internet Protocol (IP)

## IP Kya Hai?

**Internet Protocol (IP)** rules ka wo set hai jo computers aur devices ko internet pe communicate karne deta hai — ye ensure karta hai ki data sahi destination tak pahunche, unique **IP addresses** use karke.

## IP Ke Core Components

| Component | Kaam |
|---|---|
| **IP Address** | Har device ko diya gaya unique "number sticker" — device identify karne aur locate karne ke liye |
| **Packet** | Data ka wo unit jo source se destination tak travel karta hai — header + payload |
| **Router** | Network device jo packets ko forward karta hai networks ke beech |
| **Payload** | Packet ke andar ka actual data |

## IP Kaise Kaam Karta Hai

1. Data ko **packets** mein todha jaata hai
2. Har packet mein **header** hota hai — source IP, destination IP, aur baaki metadata
3. **Routers** IP header dekhkar, destination IP address ke basis pe best route decide karte hain
4. Packet multiple routers se hoke travel kar sakta hai, jab tak destination na pahunch jaaye
5. Destination pe pahunchke, packet **decapsulate** hota hai aur payload sahi application ko de diya jaata hai

## IP Ki Key Properties

| Property | Matlab |
|---|---|
| **Connectionless** | Data transfer se pehle koi connection establish nahi hoti — har packet independent travel karta hai |
| **Best-Effort Delivery** | IP delivery guarantee nahi karta — reliability ke liye upar wale protocols (jaise TCP) chahiye |
| **Unreliable** | Packet loss/corruption ho sakta hai, IP khud se recover nahi karta |

## IP Routing Kya Hai?

**IP Routing** wo process hai jisse data source se destination tak best route se pahunchti hai. Data multiple pieces mein todha jaata hai, aur har piece kai routers se hoke destination tak pahunchta hai — jo path liya jaata hai wo **routing algorithm** decide karta hai.

## IPv4 vs IPv6 (Quick Recap)

| Feature | IPv4 | IPv6 |
|---|---|---|
| Address Size | 32-bit | 128-bit |
| Total Addresses | ~4.3 billion | Practically unlimited |
| Format | Dotted decimal (192.168.1.1) | Hexadecimal (2001:0db8::1) |

*(Detailed comparison alag note file mein hai.)*

## Viva One-Liners

- **Q: IP connectionless kyun hai?**
 A: Kyunki data transfer se pehle koi formal connection establish nahi hoti — har packet apna independent path le sakta hai.
- **Q: IP delivery guarantee karta hai kya?**
 A: Nahi — ye "best-effort" delivery deta hai; reliability ke liye TCP jaisa upper-layer protocol chahiye.
- **Q: IP packet ka structure kya hai?**
 A: Header (routing/addressing info) + Payload (actual data).
