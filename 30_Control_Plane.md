# Control Plane

## Control Plane Kya Hai?

Networking mein do "planes" hote hain — **Control Plane** aur **Data Plane**. Control Plane decide karta hai **kaise** data route hoga, Data Plane actually data ko **forward** karta hai us decision ke basis pe.

> **Analogy**: Control Plane ek city planner jaisa hai jo decide karta hai kaunsi roads kahan honi chahiye aur traffic signals kaise set hone chahiye. Data Plane wo actual traffic hai jo un roads pe chal raha hai.

## Control Plane vs Data Plane

| Control Plane | Data Plane |
|---|---|
| Routing decisions leta hai (routing tables banata hai) | Actual packets ko forward karta hai un decisions ke basis pe |
| "Kaunsa raasta best hai" decide karta hai | "Data ko wahi raaste se bhejo" karta hai |
| Slower, less frequent updates | Fast, har packet ke liye kaam karta hai |

## Control Plane Kaise Kaam Karta Hai

- Routers aapas mein **routing protocols** (jaise OSPF, BGP) use karke information share karte hain
- Is information se har router apni **routing table** banata/update karta hai
- Ye table batati hai ki kisi bhi destination ke liye next hop kya hoga

## Common Routing Protocols

| Protocol | Use |
|---|---|
| **OSPF** | Ek organization ke andar routing (interior) |
| **BGP** | Internet ka backbone protocol — different networks/ISPs ke beech routing (exterior) |

## Viva One-Liner

> "Control Plane routing decisions leta hai (routing tables banake), Data Plane un decisions ke basis pe actual packets forward karta hai."
