# Routing Information Protocol (RIP)

## RIP Kya Hai?

**RIP (Routing Information Protocol)** ek **distance-vector** routing protocol hai jo **hop count** ko metric ki tarah use karta hai — sabse kam hops wale route ko best path maanta hai.

| Detail | Value |
|---|---|
| Type | Distance-vector, Interior Gateway Protocol (IGP) |
| Metric | Hop count |
| Max Hop Count | 15 (16 = unreachable) |
| Update Interval | Har 30 seconds |
| Algorithm | Bellman-Ford |
| Transport | UDP |

## RIP Kaise Kaam Karta Hai

- Har router apni **poori routing table** neighbors ke saath periodically share karta hai (har 30 sec)
- RIP **"routing by rumor"** principle pe based hai — neighbors ki di hui info pe trust karta hai
- Loops prevent karne ke liye **split horizon** aur **route poisoning** jaise mechanisms use hote hain

## RIP Ke Versions

| Version | Key Feature |
|---|---|
| **RIPv1** | Classful, broadcast updates (255.255.255.255) |
| **RIPv2** | Classless (CIDR/VLSM support), multicast updates (224.0.0.9), authentication support |
| **RIPng** | IPv6 ke liye |

## RIP Ke Advantages Aur Disadvantages

| Advantages | Disadvantages |
|---|---|
| Simple — configure/implement karna easy | Scalability issues — sirf 15 hops tak (chhote networks tak limited) |
| Low resource usage — kam processing power chahiye | Slow convergence — bade network mein temporary loops ban sakte hain |
| Compatibility — almost sab networking devices support karte hain | Limited features — hierarchical routing, load sharing jaisi advanced facilities nahi |

## Use Cases

- Chhote se medium-sized networks, simple routing needs ke saath
- Legacy networks jo OSPF/EIGRP se pehle bane the
- Educational labs, basics seekhne ke liye
- Backup routing protocol jab primary fail ho jaaye

## Viva One-Liners

- **Q: RIP mein maximum hop count kitna hota hai?**
 A: 15 — 16 ko unreachable treat kiya jaata hai.
- **Q: RIPv1 aur RIPv2 mein main difference?**
 A: RIPv1 classful hai (broadcast updates), RIPv2 classless hai (CIDR/VLSM support, multicast updates, authentication).
- **Q: RIP kaunsa algorithm use karta hai?**
 A: Bellman-Ford Algorithm.
