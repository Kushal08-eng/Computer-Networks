# Open Shortest Path First (OSPF)

## OSPF Kya Hai?

**OSPF (Open Shortest Path First)** ek **link-state Interior Gateway Protocol (IGP)** hai jo ek Autonomous System (AS) ke andar best routing path find karta hai — IETF ne develop kiya tha.

| Detail | Value |
|---|---|
| Type | Link-state, IGP |
| Algorithm | Dijkstra's (SPF - Shortest Path First) |
| Protocol Number | 89 |
| Administrative Distance | 110 |
| Classless? | Haan — VLSM aur CIDR support karta hai |
| Update Style | Triggered (sirf jab change ho, periodic nahi) |

## OSPF Kaise Kaam Karta Hai

- Har router apne direct links ki info (**Link-State Advertisements — LSAs**) poore network mein flood karta hai
- Har router isse **LSDB (Link State Database)** banata hai — poori topology ka map
- **Dijkstra's Algorithm** use karke, har router khud se sab destinations tak ka **shortest path tree** calculate karta hai
- Distance-vector protocols (jaise RIP) ke ulta, OSPF **periodic updates nahi** bhejta — sirf **triggered updates** (jab actual change ho)

## OSPF Areas — Hierarchical Design

Bade networks ko manage karne ke liye OSPF **Areas** mein divide hota hai:

| Term | Matlab |
|---|---|
| **Backbone Area (Area 0)** | OSPF domain ka core — baaki sab areas isi se connect hone chahiye |
| **Normal Areas** | Standard areas jo Area 0 se connect hote hain |
| **Internal Router** | Sirf ek hi area ke andar operate karta hai |
| **Area Border Router (ABR)** | Multiple areas ko Area 0 se connect karta hai |
| **Autonomous System Boundary Router (ASBR)** | OSPF ko dusre routing protocols se connect karta hai |

## Neighbor Formation — Key Roles

| Role | Kaam |
|---|---|
| **Designated Router (DR)** | Broadcast network mein adjacencies kam karne ke liye elect hota hai, LSAs distribute karta hai |
| **Backup Designated Router (BDR)** | DR ka backup |
| **Router ID** | Highest active IP address (ya loopback address) se determine hota hai |

## OSPF States (Neighbor Formation Process)

| State | Matlab |
|---|---|
| **Down** | Abhi tak koi Hello packet receive nahi hua |
| **Init** | Hello packet receive hua, but bidirectional communication establish nahi hui |
| **2-Way** | Dono routers ek dusre ko neighbor list mein dekh chuke hain |
| **ExStart / Exchange** | Database Description (DBD) packets exchange ho rahe hain |
| **Loading** | Missing LSAs request kiye jaa rahe hain |
| **Full** | Poori adjacency ban chuki hai — routers fully synchronized hain |

## OSPF Message Types

| Message | Kaam |
|---|---|
| **Hello** | Neighbor discovery/maintenance (default: har 10 sec) |
| **Database Description (DBD)** | LSDB ka summary compare karne ke liye |
| **Link-State Request (LSR)** | Missing LSAs request karta hai |
| **Link-State Update (LSU)** | Actual LSAs carry karta hai |
| **Link-State Acknowledgment (LSAck)** | LSU receipt confirm karta hai |

## OSPF vs RIP

| Feature | OSPF | RIP |
|---|---|---|
| Type | Link-state | Distance-vector |
| Metric | Cost (bandwidth-based) | Hop count |
| Max Network Size | Unlimited (no hop restriction) | 15 hops |
| Convergence | Fast | Slow |
| Complexity | High | Low |
| Resource Usage | Zyada (CPU/memory) | Kam |

## Viva One-Liners

- **Q: OSPF kaunsa algorithm use karta hai?**
 A: Dijkstra's Algorithm (Shortest Path First).
- **Q: OSPF ka Area 0 kya hai?**
 A: Backbone Area — poore OSPF domain ka core, baaki sab areas isse connect hote hain.
- **Q: OSPF mein Hello packets kitni der mein bhejte hain?**
 A: Default 10 seconds, aur 40 seconds tak reply na aaye to neighbor "down" maan liya jaata hai.
- **Q: OSPF RIP se better kyun hai bade networks ke liye?**
 A: OSPF ke paas hop count ki limitation nahi hai, fast convergence hai, aur Dijkstra's algorithm se accurate shortest paths calculate karta hai.
