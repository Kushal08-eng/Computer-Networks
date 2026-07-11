# Link State Routing

## Link State Routing Kya Hai?

**Link State Routing** ek dynamic routing algorithm hai jisme **har router poori network topology** ki knowledge maintain karta hai — sirf neighbors se info share karne ki jagah, routers apni **link-state information poore network mein "flood"** kar dete hain.

## Kaise Kaam Karta Hai

1. Har router apne direct links ke baare mein info (neighbors, cost, status) collect karta hai
2. Ye info **flood** ki jaati hai poore network mein — har router tak
3. Har router ke paas ab **poori network ki map** hoti hai (jaisi baaki sab routers ke paas hai)
4. **Dijkstra's Algorithm** (Shortest Path First) use karke, har router khud se sabhi destinations tak ka shortest path calculate karta hai

## Link-State Routing Ke 3 Tables

| Table | Kya Store Karta Hai |
|---|---|
| **Neighbor Table** | Sirf directly connected neighbors ki info (jinke saath adjacency bani hai) |
| **Topology Table** | Poori network topology — best aur backup routes dono |
| **Routing Table** | Final best routes jo advertise kiye gaye networks tak jaate hain |

## Key Characteristics

| Feature | Matlab |
|---|---|
| **Triggered Updates** | Updates sirf tab bhejte hain jab topology mein actual change ho (periodic nahi) |
| **Hello Messages** | Neighbor discovery aur "keep-alive" ke liye use hote hain |
| **Complete Network View** | Har router ko poori network ka pata hota hai, na ki sirf neighbors ka |

## Example Protocol: OSPF

**OSPF (Open Shortest Path First)** sabse common link-state protocol hai:

- **Classless** protocol — VLSM support karta hai
- Updates specific multicast addresses (`224.0.0.5` aur `224.0.0.6`) pe bheje jaate hain
- IP datagram mein protocol field ki value **89** hoti hai

## Link State vs Distance Vector

| Feature | Link State | Distance Vector |
|---|---|---|
| Network View | Poori network ki knowledge | Sirf immediate neighbors ki |
| Update Method | Flooding (triggered, jab change ho) | Periodic (poori routing table neighbors ko bhejna) |
| Algorithm | Dijkstra's Algorithm | Bellman-Ford Algorithm |
| Convergence | Fast | Slow |
| Routing Loops | Rare (poori topology pata hai) | Common (jaise "Count to Infinity" problem) |
| Resource Usage | Zyada (processing, memory) | Kam |
| Example | OSPF, IS-IS | RIP |

## Viva One-Liners

- **Q: Link State routing mein har router kya maintain karta hai?**
 A: Poori network topology ki complete knowledge.
- **Q: Link State routing kaunsa algorithm use karti hai?**
 A: Dijkstra's Algorithm (Shortest Path First).
- **Q: OSPF kis type ka protocol hai?**
 A: Link-state, classless, Interior Gateway Protocol (IGP).
