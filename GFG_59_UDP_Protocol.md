# User Datagram Protocol (UDP)

## UDP Kya Hai?

**UDP (User Datagram Protocol)** ek Transport Layer protocol hai jo **fast, connectionless, aur lightweight** communication deta hai — delivery, order, ya error checking ki guarantee nahi deta.

## UDP Header Structure (8 Bytes Fixed)

| Field | Size | Kaam |
|---|---|---|
| **Source Port** | 16 bits | Sender application identify karta hai |
| **Destination Port** | 16 bits | Receiver application identify karta hai |
| **Length** | 16 bits | Poore UDP datagram (header + data) ki length |
| **Checksum** | 16 bits | Error checking ke liye (IPv4 mein optional, IPv6 mein mostly mandatory) |

> UDP header **fixed 8 bytes** hai — TCP ke variable 20-60 bytes se bahut chhota, isiliye fast hai.

## UDP Ki Key Properties

| Property | Matlab |
|---|---|
| **Connectionless** | Koi handshake/setup nahi, seedha data bhej diya jaata hai |
| **Unreliable** | Delivery guarantee nahi — packet loss ho sakta hai |
| **No Ordering** | Packets kisi bhi order mein pahunch sakte hain |
| **No Flow/Congestion Control** | IP/ICMP pe reliability ke liye depend karta hai |

## UDP Kab Use Hota Hai

| Application | Kyun UDP |
|---|---|
| **DNS** | Chhoti queries, fast response chahiye |
| **VoIP** | Real-time — thoda packet loss acceptable, delay nahi |
| **Video Streaming** | Speed important, chhoti frame loss se koi bada farak nahi padta |
| **Online Gaming** | Low latency critical hai |

## UDP Flood Attack (Security Note)

**UDP Flood** ek DDoS attack hai jisme attacker target ke random ports pe massive UDP packets bhejta hai (spoofed IP se) — target har packet ke liye "Destination Unreachable" ICMP reply bhejta hai, jisse uske resources overload ho jaate hain.

## Viva One-Liners

- **Q: UDP header ki size kitni hai?**
 A: Fixed 8 bytes.
- **Q: UDP mein checksum mandatory hai ya optional?**
 A: IPv4 mein optional, IPv6 mein mostly mandatory.
- **Q: UDP kis type ki applications ke liye best hai?**
 A: Real-time applications jahan speed zaroori hai aur thoda packet loss acceptable hai (streaming, gaming, VoIP).
