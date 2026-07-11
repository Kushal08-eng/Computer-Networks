# Internet Control Message Protocol (ICMP)

## ICMP Kya Hai?

**ICMP (Internet Control Message Protocol)** ek network layer protocol hai jo routers, gateways, aur hosts **error messages** aur **operational information** bhejne ke liye use karte hain.

> **Zaroorat**: IP protocol khud mein koi built-in error-reporting mechanism nahi rakhta — ICMP IP suite ka ek supporting protocol hai jo errors report karta hai aur diagnostic messages bhejta hai.

## ICMP Ke Main Uses

| Use | Matlab |
|---|---|
| **Error Reporting** | Jab data packets destination tak nahi pahunch paate (unreachable host, timeout, fragmentation error) |
| **Operational Queries** | Jaise `ping` tool mein use hone wale echo request/reply |

## ICMP Packet Format

| Field | Size | Kaam |
|---|---|---|
| **Type** | 8 bits | Message ka type batata hai |
| **Code** | 8 bits | Error/type ke baare mein additional info |
| **Checksum** | 16 bits | Error checking ke liye |

## Common ICMP Message Types

| Type Number | Message |
|---|---|
| 0 | Echo Reply |
| 3 | Destination Unreachable |
| 5 | Redirect Message |
| 8 | Echo Request |
| 11 | Time Exceeded |
| 12 | Parameter Problem |

## Kaise Kaam Karta Hai (Examples)

- **Destination Unreachable**: Agar packet destination tak nahi pahunch paata (kisi bhi reason se), host ya intermediate router source ko ICMP error message bhejta hai
- **Time Exceeded**: Jab packet ka TTL 0 ho jaata hai, ICMP message source ko inform karta hai
- **Redirect**: Router source ko bata sakta hai ki koi aur (shorter) path available hai, taaki future packets us route se jaayein
- **Echo Request/Reply**: `ping` command isi pe based hai — check karta hai ki destination reachable hai ya nahi

## Security Concern: Smurf Attack

**Smurf Attack** ek attack hai jisme attacker spoofed source IP address ke saath ICMP packets bhejta hai — jaise purane "Ping of Death" attacks bhi is category mein aate hain.

## Viva One-Liners

- **Q: ICMP ka main kaam kya hai?**
 A: Network devices ke beech error messages aur diagnostic information (jaise ping) bhejna.
- **Q: `ping` command kis ICMP message type ko use karta hai?**
 A: Echo Request (Type 8) aur Echo Reply (Type 0).
- **Q: IP protocol mein error reporting kyun nahi hoti khud?**
 A: Isliye ICMP ek supporting protocol ki tarah kaam karta hai, IP ke saath milke error handling karta hai.
