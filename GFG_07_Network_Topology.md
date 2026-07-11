# Types of Network Topology

## Network Topology Kya Hai?

**Network Topology** network mein devices (nodes) aur unke connections (links) ka arrangement hai — ye batata hai devices kaise connected hain aur data kaise flow karta hai.

| Type | Matlab |
|---|---|
| **Physical Topology** | Cables aur devices ka actual physical layout |
| **Logical Topology** | Data network mein kaise move karta hai, physical layout se independent |

*(Bus, Star, Mesh, Ring, Tree, Hybrid — ye sab **physical** topologies hain.)*

---

## 1. Point-to-Point Topology

Sender aur receiver ke functionality pe based simplest topology — ek sender, ek receiver.

| Advantages | Disadvantages |
|---|---|
| Simple, easy setup | Bade networks ke liye suitable nahi |
| High data transfer speed (dedicated link) | Multiple devices connect karna expensive |
| Secure communication (direct connection) | Limited scalability |
| Low data collision chances | Link fail ho to communication cut ho jaata hai |

## 2. Mesh Topology

Har device har dusre device se ek dedicated channel (link) se connected hota hai.

- N devices connected hon to har device ko **N-1 ports** chahiye
- Total dedicated links chahiye: **N × (N-1) / 2**
- Example: 6 devices ho to har device ko 5 ports chahiye, total links = 6×5/2 = 15

| Advantages | Disadvantages |
|---|---|
| Nodes ke beech communication bahut fast | Installation/configuration difficult |
| Robust | Cable cost high (bulk wiring chahiye) |
| Fault easily diagnose hota hai, reliable data | Maintenance cost high |
| Security aur privacy better | — |

> **Real Example**: Internet backbone, jahan alag-alag ISPs dedicated channels se connected hote hain. Military communication aur aircraft navigation systems mein bhi use hota hai.

## 3. Star Topology

Sab devices ek single central **hub** se cable ke through connected hote hain.

| Advantages | Disadvantages |
|---|---|
| N devices ke liye sirf N cables chahiye — easy setup | Hub fail ho to poora system crash |
| Har device ko sirf 1 port chahiye | Installation cost high |
| Robust — ek link fail ho to sirf wahi affect hota hai | Performance hub pe depend karta hai |
| Fault identify/isolate karna easy | — |
| Cost-effective (inexpensive coaxial cable) | — |

> **Real Example**: Office LAN jahan sab computers ek central hub se connected hain; wireless networks jahan devices ek access point se connected hote hain.

## 4. Bus Topology

Har computer/device ek single cable se connected hota hai — bi-directional, multi-point connection.

| Advantages | Disadvantages |
|---|---|
| N devices ke liye 1 backbone cable + N drop lines chahiye | Bulk cabling chahiye hoti hai |
| Cable cost kam (small networks ke liye) | Backbone cable fail ho to poora system crash |
| Well-known installation/troubleshooting | Heavy traffic mein collisions badhte hain |
| — | Naye devices add karne se network slow ho sakta hai |
| — | Security bahut low hai |

> **Real Example**: Ethernet LAN jahan sab devices ek coaxial cable se connected hain; cable television networks.

## 5. Ring Topology

Devices ek ring form karte hain, har device apne exactly 2 neighbors se connected hota hai. Bade number of nodes ke liye **repeaters** use hote hain.

### Operations
- Ek **monitor station** poori operation ki responsibility leta hai
- Data transmit karne ke liye station ko **token** hold karna padta hai — transmission ke baad token release karta hai
- Jab koi transmit nahi kar raha, token ring mein circulate karta rehta hai

| Advantages | Disadvantages |
|---|---|
| High-speed data transmission | Ek node fail ho to poora network fail ho sakta hai |
| Collision possibility minimum | Troubleshooting mushkil |
| Install/expand karna sasta | Security kam |

> **Note**: Data ek direction mein flow karta hai, but 2 connections use karke bidirectional (**Dual Ring Topology**) bhi banaya ja sakta hai.

## 6. Tree Topology

Star topology ka variation — hierarchical data flow.

- Multiple **secondary hubs** ek central hub (jisme repeater hota hai) se connected hote hain
- Data top-to-bottom (central hub → secondary → devices) ya bottom-to-top flow kar sakta hai
- Multi-point connection, non-robust (backbone fail ho to poora topology crash)

| Advantages | Disadvantages |
|---|---|
| Zyada devices ek central hub se attach ho sakte hain | Central hub fail ho to poora system fail |
| Network ko isolate/prioritize kar sakte hain | Cost high (cabling ki wajah se) |
| Naye devices existing network mein add kar sakte hain | Naye devices add karne pe reconfigure karna mushkil |

> **Real Example**: Bade organization ki hierarchy — CEO root hai, departments child nodes, managers grandchild nodes, team members leaf nodes.

## 7. Hybrid Topology

Upar wali sab topologies ka **combination**.

| Advantages | Disadvantages |
|---|---|
| Bahut flexible | Architecture design karna challenging |
| Naye devices add karke size easily expand kar sakte hain | Hubs expensive hote hain |
| — | Infrastructure cost bahut high (zyada cabling aur devices) |

> **Real Example**: University campus network — backbone star topology ka, har building switch/router se backbone se connected, aur building ke andar bus/ring topology.

---

## Network Topology Kyun Important Hai

| Point | Matlab |
|---|---|
| **Network Performance** | Sahi topology se network smoothly chalta hai, performance badhti hai |
| **Network Reliability** | Star/Mesh jaisi topologies reliable hain — ek connection fail ho to backup available hota hai |
| **Network Expansion** | Sahi topology se naye devices add karna easy hota hai, bina disruption ke |
| **Network Security** | Topology samajhna better security implement karne mein help karta hai |

## Viva One-Liners

- **Q: Mesh topology mein N devices ke liye total links kitni chahiye?**
 A: N × (N-1) / 2.
- **Q: Star topology ka sabse bada disadvantage kya hai?**
 A: Central hub fail hone pe poora system crash ho jaata hai.
- **Q: Ring topology mein data transmit karne ke liye kya chahiye?**
 A: Token — jo station transmit karna chahti hai use pehle token hold karna padta hai.
- **Q: Hybrid topology kya hai?**
 A: Do ya zyada topologies (jaise Star + Bus) ka combination, flexible but design/cost mein complex.
