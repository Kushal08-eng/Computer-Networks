# IP (Internet Protocol)

## IP Kya Hai?

**IP (Internet Protocol)** network layer ka core protocol hai jo har device ko ek unique **IP address** deta hai aur data packets ko source se destination tak **route** karta hai.

## IP Ke 2 Main Kaam

| Kaam | Matlab |
|---|---|
| **Addressing** | Har device ko unique IP address dena |
| **Routing** | Packet ko sahi path se destination tak pahunchana |

## IP Header Ke Important Fields

| Field | Kaam |
|---|---|
| Source IP | Kisne bheja |
| Destination IP | Kisko jaana hai |
| TTL (Time to Live) | Packet kitni der/hops tak zinda rahega (infinite loop rokta hai) |
| Protocol | Batata hai upar TCP hai ya UDP |
| Checksum | Header ki integrity check karta hai |

## TTL Ka Concept (Interesting)

Har router se guzarte waqt TTL value **1 se kam** hoti hai. Agar TTL 0 ho jaaye, packet **discard** kar diya jaata hai — isse packets hamesha ke liye network mein ghoomte nahi rehte (infinite loop se bachaata hai).

> **Analogy**: TTL ek "expiry countdown" jaisa hai — agar packet bahut zyada raaste bhatak jaaye bina destination pahunche, TTL khatam hone pe use "expire" kar diya jaata hai.

## IP Connectionless Hai

IP khud **unreliable aur connectionless** hai — reliability (agar chahiye) TCP jaise upar wale protocol se aati hai.

## Viva One-Liners

- **Q: IP ke 2 main functions kya hain?**
 A: Addressing aur Routing.
- **Q: TTL field ka kaam kya hai?**
 A: Packet ko infinite loop mein ghoomne se rokna — har hop pe value kam hoti hai, 0 hone pe packet discard.
