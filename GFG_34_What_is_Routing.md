# What is Routing?

## Routing Kya Hai?

**Routing** wo process hai jisse network layer decide karti hai ki data packets source se destination tak **best path** se kaise pahunchein — chahe wo path multiple intermediate networks/routers se hoke guzarta ho.

## Routing Kaise Kaam Karti Hai (Step-by-Step)

| Step | Kya Hota Hai |
|---|---|
| 1. Communication Start | Device (client/server) HTTP jaisa protocol use karke communication shuru karta hai |
| 2. Data Packets | Data chhote packets mein todha jaata hai, har packet pe destination IP tag hoti hai |
| 3. Best Path Selection | Router **load** (kitna busy path hai) aur **reliability** (kitna stable/available path hai) dekhkar best path decide karta hai |
| 4. Forwarding | Packets hop-by-hop, router se router, destination tak travel karte hain |

## Key Factors Jo Routing Decision Ko Influence Karte Hain

| Factor | Matlab |
|---|---|
| **Load** | Path kitna busy hai — kam busy path se fast delivery hoti hai |
| **Reliability** | Kaunsa path zyada stable/available hai, taaki data safely pahunche |

## Types of Routing

### 1. Static Routing
Non-adaptive routing — routes network administrator **manually** configure karta hai. Complete control deta hai, but sirf **chhote networks** ke liye suitable hai.

### 2. Dynamic Routing
Automatic aur adaptive — routers algorithms use karke khud paths choose karte hain. Modern networks mein widely use hoti hai flexibility ke liye.

### 3. Default Routing
Jab koi specific route available na ho, packets ek predefined **gateway** ko bhej diye jaate hain. Single exit point wale networks mein common hai.

## Static vs Dynamic vs Default — Quick Comparison

| Type | Control | Best For |
|---|---|---|
| **Static** | Zyada manual control, but time-consuming large networks mein | Chhote, simple networks |
| **Dynamic** | Kam manual control, automated | Bade, scalable networks — load balancing bhi support karta hai |
| **Default** | Fixed "last resort" gateway | Single exit point wale networks (stub routers) |

## Core Concepts

| Term | Matlab |
|---|---|
| **Router** | Network device jo routing decisions leta hai |
| **Routing Table** | Ek logical data structure jisme routes store hote hain |
| **Routing Algorithm** | Metrics (hop count, delay, bandwidth) ke basis pe shortest path select karta hai |

## Viva One-Liners

- **Q: Routing ka main goal kya hai?**
 A: Data packets ko source se destination tak best (efficient, reliable) path se pahunchana.
- **Q: Routing decisions kis 2 factors pe depend karte hain?**
 A: Load (path kitna busy hai) aur Reliability (path kitna stable hai).
- **Q: Default routing kab use hoti hai?**
 A: Jab koi specific route routing table mein match na ho, packet predefined gateway ko bhej diya jaata hai.
