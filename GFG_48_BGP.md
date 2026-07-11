# Border Gateway Protocol (BGP)

## BGP Kya Hai?

**BGP (Border Gateway Protocol)** ek **Exterior Gateway Protocol (EGP)** hai jo **Autonomous Systems (AS)** ko aapas mein connect karta hai — internet ka backbone routing protocol hai.

| Detail | Value |
|---|---|
| Type | Path-vector protocol (distance-vector ya link-state se alag) |
| Category | Exterior Gateway Protocol (EGP) |
| Transport | TCP |
| Main Kaam | Network reachability information exchange karna, alag Autonomous Systems ke beech |

## Autonomous System (AS) Kya Hai?

Ek **Autonomous System** IP networks aur routers ka collection hai jo ek single administrative authority ke under hota hai (jaise ek ISP ya bada organization). Har AS ka apna unique **AS Number** hota hai.

## eBGP vs iBGP

| Type | Full Form | Kab Use Hota Hai |
|---|---|---|
| **eBGP** | External BGP | Alag-alag Autonomous Systems ke beech routing info exchange karne ke liye |
| **iBGP** | Internal BGP | Same Autonomous System ke andar routers ke beech, consistency ensure karne ke liye |

## BGP Kyun "Path Vector" Protocol Hai

Distance-vector protocols (jaise RIP) sirf "distance" (hop count) share karte hain. BGP isse aage jaake **poora AS Path** (kaunse-kaunse Autonomous Systems se hoke jaana hai) advertise karta hai — isse:

- Best path decide karne mein help milti hai (shorter AS path)
- **Loop prevention** hota hai — agar AS apna khud ka AS number path mein dekh le, to samajh jaata hai loop hai

## BGP Ke Key Concepts

| Concept | Matlab |
|---|---|
| **Weight** | Cisco-specific attribute jo batata hai kaunsa path preferred hai |
| **Next-Hop Paradigm** | BGP advertisements mein reachable destination ke saath next-hop info bhi hoti hai |
| **Route Advertisement** | BGP routers apni routing table se best route advertise karte hain, sab options nahi |

## BGP Kaise Kaam Karta Hai (Basic Flow)

1. Dono BGP routers (peers) TCP se connection establish karte hain (3-way handshake)
2. **Open messages** exchange karte hain — apna AS number bataate hain (decide hota hai eBGP hai ya iBGP)
3. **Keepalive messages** bhejte rehte hain, taaki connection alive rahe
4. Jab route info share karni ho, **Update messages** bheji jaati hain

## BGP vs OSPF (Quick Comparison)

| Feature | BGP | OSPF |
|---|---|---|
| Category | Exterior Gateway Protocol | Interior Gateway Protocol |
| Scope | Autonomous Systems ke beech | Ek Autonomous System ke andar |
| Best For | Internet, WAN environments | LAN, data centers |
| Structure | Mesh-like | Hierarchical (areas) |
| Convergence | Slower | Fast |

## Viva One-Liners

- **Q: BGP kis category ka protocol hai?**
 A: Exterior Gateway Protocol (EGP) — path-vector routing.
- **Q: eBGP aur iBGP mein difference?**
 A: eBGP alag Autonomous Systems ke beech use hota hai, iBGP same AS ke andar.
- **Q: BGP ko "Path Vector" kyun kehte hain?**
 A: Kyunki ye sirf distance nahi, balki poora AS Path advertise karta hai — jo best path selection aur loop prevention dono mein help karta hai.
