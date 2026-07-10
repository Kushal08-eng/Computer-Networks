# UDP (User Datagram Protocol)

## UDP Kya Hai?

**UDP** ek transport layer protocol hai jo **fast but unreliable** data delivery deta hai — koi connection setup nahi hota, koi acknowledgment nahi, bas data bhej diya jaata hai.

> **Analogy**: UDP normal post jaisa hai — letter daal diya post box mein, pahuncha ya nahi confirmation nahi milta, but fast hota hai.

## UDP Ki Characteristics

| Feature | Detail |
|---|---|
| **Connectionless** | Koi handshake/setup nahi hota, seedha data bhej do |
| **Unreliable** | Delivery guarantee nahi, packet loss ho sakta hai |
| **Fast** | Koi extra overhead (acknowledgment, error checking) nahi hai |
| **No Ordering** | Packets kisi bhi order mein pahunch sakte hain |

## UDP Header (Simple)

| Field | Kaam |
|---|---|
| Source Port | Sender application ka port |
| Destination Port | Receiver application ka port |
| Length | Data ki length |
| Checksum | Basic error checking |

UDP ka header bahut **chhota aur simple** hota hai (sirf 8 bytes) — isiliye fast hai.

## Use Cases

| Use Case | Kyun UDP |
|---|---|
| **Video Streaming** | Ek do frame miss ho jaaye to bhi chalega, speed important hai |
| **Online Gaming** | Real-time response chahiye, thoda data loss acceptable hai |
| **Voice Calls (VoIP)** | Delay se badhtar hai chhota data loss |
| **DNS Queries** | Chhoti requests, fast response chahiye |

## Viva One-Liners

- **Q: UDP connection-oriented hai ya connectionless?**
 A: Connectionless.
- **Q: UDP kab use karte hain TCP ki jagah?**
 A: Jab speed important ho aur thoda data loss acceptable ho (video/gaming/voice).
