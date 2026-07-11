# Enhanced Interior Gateway Routing Protocol (EIGRP)

## EIGRP Kya Hai?

**EIGRP (Enhanced Interior Gateway Routing Protocol)** ek **hybrid routing protocol** hai — Cisco ne banaya, jisme distance-vector aur link-state, dono protocols ki features combine hoti hain.

| Detail | Value |
|---|---|
| Type | Hybrid (advanced distance-vector) |
| Algorithm | DUAL (Diffusing Update Algorithm) |
| Vendor | Cisco (proprietary — sirf Cisco devices pe kaam karta hai) |
| Administrative Distance | 90 (Cisco default) |

## EIGRP Distance-Vector Aur Link-State Dono Features Kyun Rakhta Hai

| Distance-Vector Jaisa | Link-State Jaisa |
|---|---|
| Neighbors se routes seekhta hai (directly connected) | Hello Protocol use karta hai neighbor discovery/adjacency ke liye |
| — | Topology change hone pe partial (triggered) updates bhejta hai |

## Key Features

| Feature | Matlab |
|---|---|
| **DUAL Algorithm** | Loop-free backup paths identify karta hai, fast reconvergence deta hai |
| **Unequal-Cost Load Balancing** | Multiple paths pe traffic distribute kar sakta hai, chahe unki cost same na ho (OSPF sirf equal-cost load balancing karta hai) |
| **Partial/Triggered Updates** | Sirf change hui information bhejta hai, na ki poori routing table (jaise RIP karta hai) |
| **Neighbor Table** | Poori network map ki jagah, sirf neighbors ki info maintain karta hai |
| **Classless Protocol** | VLSM aur route summarization support karta hai |

## EIGRP vs OSPF

| Feature | EIGRP | OSPF |
|---|---|---|
| Type | Hybrid (advanced distance-vector) | Link-state |
| Vendor | Cisco proprietary | Open standard (IETF) |
| Algorithm | DUAL | Dijkstra |
| Load Balancing | Unequal-cost bhi possible | Sirf equal-cost |
| CPU/Memory Usage | Kam | Zyada |
| Convergence | Fast | Comparatively slow |
| Multi-vendor Support | Nahi (sirf Cisco) | Haan |

## Advantages Aur Disadvantages

| Advantages | Disadvantages |
|---|---|
| Fast convergence (DUAL algorithm) | Limited vendor support — sirf Cisco devices |
| Easy configuration | Multi-vendor networks mein use nahi ho sakta |
| Unequal-cost load balancing | — |
| Scalable — chhote aur bade networks dono mein kaam karta hai | — |

## Viva One-Liners

- **Q: EIGRP kis type ka protocol hai?**
 A: Hybrid — distance-vector aur link-state, dono ki features combine karta hai.
- **Q: EIGRP kaunsa algorithm use karta hai?**
 A: DUAL (Diffusing Update Algorithm).
- **Q: EIGRP ki sabse badi limitation kya hai?**
 A: Ye Cisco-proprietary hai — sirf Cisco devices pe kaam karta hai, multi-vendor networks mein nahi.
