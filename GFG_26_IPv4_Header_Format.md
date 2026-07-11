# IPv4 Header Format

## IPv4 Header Kya Hai?

Har **IPv4 datagram** mein ek header hota hai jo actual data (payload) se pehle aata hai — isme routing/delivery ke liye zaroori meta-information hoti hai. Standard header size **20 bytes** (minimum) hoti hai, **60 bytes tak** (options ke saath) ja sakti hai.

## IPv4 Header Ke Fields

| Field | Size | Kaam |
|---|---|---|
| **Version** | 4 bits | IP protocol ka version batata hai (IPv4 ke liye value = 4) |
| **HLEN (Header Length)** | 4 bits | Header mein kitne 32-bit words hain (min 5, max 15) |
| **Type of Service** | 8 bits | Delay, Throughput, Reliability ke priorities batata hai (QoS ke liye) |
| **Total Length** | 16 bits | Header + Data ki poori length (min 20 bytes, max 65,535 bytes) |
| **Identification** | 16 bits | Ek datagram ke sab fragments ko unique ID deta hai (reassembly ke liye) |
| **Flags** | 3 bits | Reserved bit, Do Not Fragment (DF), More Fragments (MF) |
| **Fragment Offset** | 13 bits | Batata hai fragment original datagram mein kahan fit hota hai (8-byte units mein) |
| **Time to Live (TTL)** | 8 bits | Datagram ki "lifetime" — har hop pe 1 kam hoti hai, 0 pe packet discard |
| **Protocol** | 8 bits | Batata hai upar wali layer ka protocol kaunsa hai (TCP=6, UDP=17, ICMP=1) |
| **Header Checksum** | 16 bits | Header mein errors check karta hai |
| **Source IP Address** | 32 bits | Sender ka IP address |
| **Destination IP Address** | 32 bits | Receiver ka IP address |
| **Options** | Variable | Optional info (source route, record route) — network admin use karta hai |

## TTL Ka Special Role

**Time to Live (TTL)** ensure karta hai ki packet infinite loop mein na ghoome:

- Sender ek initial TTL value set karta hai (jaise 64 ya 128)
- Har router se guzarte waqt TTL **1 se kam** hoti hai
- Jab TTL **0** ho jaaye, packet discard kar diya jaata hai aur sender ko ICMP error message bhej diya jaata hai

## Fragmentation Ke Fields (Identification, Flags, Fragment Offset)

Agar datagram destination network ke **MTU (Maximum Transmission Unit)** se bada ho, to use fragment karna padta hai:

| Field | Kaam |
|---|---|
| **Identification** | Sab fragments ko same number milta hai, taaki reassembly ke time pehchane ja sakein |
| **DF (Do Not Fragment) Flag** | Agar 1 set hai, packet fragment nahi ho sakta — bhejna possible na ho to discard hoke ICMP error jaata hai |
| **MF (More Fragments) Flag** | 1 = aur fragments aa rahe hain; 0 = ye last (ya sirf) fragment hai |
| **Fragment Offset** | Batata hai ye fragment original data mein kahan (kitne 8-byte blocks ke baad) fit hota hai |

## Header Checksum Kaise Kaam Karta Hai

- Sirf **header** ka checksum hota hai (payload ka nahi — wo TCP/UDP apna khud verify karta hai)
- Har router jab TTL (ya options) modify karta hai, checksum **recalculate** karta hai
- Agar checksum match nahi hota, packet **discard** kar diya jaata hai

## Viva One-Liners

- **Q: IPv4 header ki minimum aur maximum size kya hai?**
 A: Minimum 20 bytes, maximum 60 bytes (options ke saath).
- **Q: TTL field ka kaam kya hai?**
 A: Packet ko infinite loop mein ghoomne se rokna — har hop pe value kam hoti hai, 0 hone pe discard.
- **Q: Protocol field TCP aur UDP ke liye kya value rakhta hai?**
 A: TCP = 6, UDP = 17.
- **Q: Fragmentation kab hoti hai?**
 A: Jab datagram size destination network ke MTU se zyada ho.
