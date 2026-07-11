# Distance Vector Routing (DVR)

## Distance Vector Routing Kya Hai?

**Distance Vector Routing** ek dynamic routing algorithm hai jisme har router sirf apne **immediate neighbors** ke basis pe destinations tak ki distance calculate karta hai — poori network ki knowledge nahi hoti, sirf jo neighbors bataate hain.

Isse informally **"routing by rumor"** bhi kaha jaata hai — kyunki router ko sirf utna hi pata hota hai jitna uska neighbor use bataata hai.

## Kaise Kaam Karta Hai

1. Har router apni **routing table** directly connected neighbors ke saath share karta hai
2. Ye sharing **regular intervals** pe hoti hai (periodic updates)
3. Received information se router apni khud ki table **update** karta hai
4. Route computation ke liye **Bellman-Ford Algorithm** use hota hai

## Distance aur Vector Ka Matlab

| Term | Matlab |
|---|---|
| **Distance** | Destination network kitni "dur" hai — metric jaise hop count |
| **Vector** | Direction — kaunse next-hop router/interface se destination tak pahuncha jaa sakta hai |

## Problems With Distance Vector Routing

| Problem | Matlab |
|---|---|
| **Count to Infinity** | Agar link fail ho jaaye, routers galat information ek dusre ko baar-baar bhejte reh sakte hain, jisse metric slowly infinity tak badhta rehta hai |
| **Routing Loops** | Persistent loops ban sakte hain, kyunki router ko poori topology ka pata nahi hota |
| **Slow Convergence** | Poori routing table bhejni padti hai, updates periodic hote hain — isse network changes reflect hone mein time lagta hai |

## Example Protocol: RIP

**RIP (Routing Information Protocol)**:

- Distance vector protocol hai — **hop count** ko metric ki tarah use karta hai
- Maximum hop count = **15** (routing loops rokne ke liye — 16 ko "unreachable" maana jaata hai)
- Mechanisms jaise **split horizon**, **route poisoning**, aur **hold-down timers** loops rokne ke liye use hote hain

## Distance Vector vs Link State

| Feature | Distance Vector | Link State |
|---|---|---|
| Knowledge | Sirf neighbors ki | Poori network ki |
| Update | Periodic, poori table | Triggered, sirf changes |
| Algorithm | Bellman-Ford | Dijkstra |
| Complexity | Simple | Complex |
| Best For | Chhoti networks | Bade, complex networks |
| Example | RIP | OSPF |

## Viva One-Liners

- **Q: Distance Vector Routing ko "routing by rumor" kyun kaha jaata hai?**
 A: Kyunki router ko sirf utni info hoti hai jitni uske immediate neighbors ne share ki ho — poori network ka pata nahi hota.
- **Q: Distance Vector Routing kaunsa algorithm use karta hai?**
 A: Bellman-Ford Algorithm.
- **Q: RIP mein maximum hop count kitna hota hai?**
 A: 15 — 16 ko unreachable treat kiya jaata hai, isse infinite loops prevent hote hain.
- **Q: "Count to Infinity" problem kya hai?**
 A: Ek scenario jisme link failure ke baad routers galat metric information circulate karte rehte hain, jisse metric slowly badhta jaata hai.
