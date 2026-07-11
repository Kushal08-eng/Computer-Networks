# Link Aggregation (LACP)

## Link Aggregation Kya Hai?

**Link Aggregation Control Protocol (LACP)** ek IEEE standard protocol hai (802.3ad) jo **multiple physical Ethernet links** ko combine karke ek **single logical link** banata hai.

> **Analogy**: Jaise airport tak jaane ke liye do highways bana di jaayein — traffic dono mein baant sakte ho, aur ek highway band ho to dusri se kaam chal jaata hai. LACP bhi multiple network links ko combine karke bandwidth badhata hai aur backup deta hai.

## Ye Kya Provide Karta Hai

| Fayda | Matlab |
|---|---|
| **Bandwidth Increase** | Multiple links combine hoke total bandwidth badha dete hain |
| **Reliability** | Ek link fail ho to traffic baaki active links pe automatically shift ho jaata hai |
| **Load Balancing** | Traffic sab active links mein distribute hota hai |

## LACP Ke Modes

| Mode | Matlab |
|---|---|
| **Active Mode** | Port actively LACPDUs (LACP Data Units) bhejta hai link aggregation initiate/maintain karne ke liye |
| **Passive Mode** | Port khud communication initiate nahi karta, but received LACPDUs ka response deta hai |

## LACP Multiple Layers Pe Kaam Karta Hai

| Layer | Kaam |
|---|---|
| **Layer 1 (Physical)** | Multiple physical links ko ek logical channel mein combine karta hai |
| **Layer 2 (Data Link)** | Switch ports ko aggregation set mein group karta hai, MAC addressing manage karta hai |
| **Layer 3 (Network)** | IP addresses, MAC addresses, ya TCP/UDP port numbers ke basis pe hashing algorithms se load balance karta hai |

## Key Specs

| Spec | Detail |
|---|---|
| Max interfaces per group | 16 tak support, but max 8 **active** links (baaki standby) |
| Multicast Address | 01:80:C2:00:00:02 (LACPDUs exchange karne ke liye) |

## Static LAG vs Dynamic LAG (LACP)

| Static LAG | Dynamic LAG (LACP) |
|---|---|
| Manual configuration | Automatic negotiation |
| Link failures detect nahi kar sakta (sirf complete link down hi pata chalta hai) | Link status dynamically detect/manage karta hai |
| Simple but less flexible | Zyada resilient aur maintain karna easy |

## Use Cases

| Use Case | Matlab |
|---|---|
| Enterprise LANs | Switch uplinks aggregate karke bandwidth badhana |
| Data Centers | Servers/storage ke liye throughput aur redundancy improve karna |
| Service Providers | Multiple WAN links bundle karke high-speed connectivity |
| High-Availability Systems | Zero downtime ke saath automatic failover |

## Viva One-Liners

- **Q: LACP ka IEEE standard kya hai?**
 A: IEEE 802.3ad.
- **Q: LACP ka main fayda kya hai?**
 A: Multiple physical links ko ek logical link mein combine karke bandwidth badhana aur redundancy dena.
- **Q: Active aur Passive LACP mode mein difference?**
 A: Active mode khud LACPDUs bhejta hai; passive mode sirf response karta hai jab dusra device initiate kare.
