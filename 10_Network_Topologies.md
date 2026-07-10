# Network Topologies (BUS, RING, STAR, TREE, MESH)

## Topology Kya Hai?

Topology batata hai network ke devices (nodes) physically/logically **kaise arranged/connected** hain.

## Types of Topologies

### 1. Bus Topology
Sab devices ek hi central cable (bus) se connected hote hain.

| Fayda | Nuksaan |
|---|---|
| Sasta, kam cable chahiye | Cable break hui to poora network down |
| Setup easy hai | Zyada devices se performance slow ho jaata hai |

### 2. Ring Topology
Devices ek circle mein connected hote hain, data ek fixed direction mein travel karta hai.

| Fayda | Nuksaan |
|---|---|
| Data collision kam hota hai | Ek node fail ho to poora ring affect ho sakta hai |

### 3. Star Topology
Sab devices ek central **hub/switch** se connected hote hain.

| Fayda | Nuksaan |
|---|---|
| Ek device fail ho to baaki chalte rehte hain | Hub/switch fail hua to sab down |
| Sabse zyada use hoti hai practically | Extra cabling cost (har device ka apna wire hub tak) |

### 4. Tree Topology
Star topologies ka hierarchical combination — jaise ek "tree" structure (root, branches).

| Fayda | Nuksaan |
|---|---|
| Scalable — naye branches easily add ho sakte hain | Root node fail ho to us branch ka poora network down |

### 5. Mesh Topology
Har device har dusre device se **directly** connected hota hai.

| Fayda | Nuksaan |
|---|---|
| Bahut reliable, single point of failure nahi | Bahut mehenga (cables ki N×(N-1)/2 zaroorat) |

## Analogy Table

| Topology | Analogy |
|---|---|
| Bus | Ek single road jispe sab ghar connected hain |
| Ring | Students circle mein baithe hain, note ek direction mein pass kar rahe hain |
| Star | Classroom mein teacher (hub) ke around students |
| Tree | Company ka organizational hierarchy chart |
| Mesh | Har dost seedha har dost se WhatsApp pe connected (group nahi, sabke sath individual chat) |

## Viva One-Liner

> "Star topology sabse common hai practically kyunki ek device fail hone se poora network affect nahi hota — sirf central hub critical hota hai."
