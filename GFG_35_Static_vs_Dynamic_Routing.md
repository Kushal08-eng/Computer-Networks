# Static vs Dynamic Routing

## Static Routing Kya Hai?

**Static Routing** (Non-Adaptive Routing) mein routes **network administrator manually** configure karta hai — jab tak khud change na kare, routing table update nahi hoti.

| Feature | Detail |
|---|---|
| Configuration | Manual |
| Algorithm | Simple, complex algorithms nahi use hote |
| Security | Higher — sirf admin allowed routes control karta hai |
| CPU Overhead | Nahi — cheap routers use ho sakte hain |
| Bandwidth Usage | Koi nahi (routers ke beech koi extra communication nahi) |

### Static Routing Ke Disadvantages
- Bade networks mein manually routes add karna **time-consuming** hai
- Poore network topology ki **detailed knowledge** chahiye
- Naye administrators ko sab routes seekhne padte hain configure karne ke liye

## Dynamic Routing Kya Hai?

**Dynamic Routing** (Adaptive Routing) automatically routing table update karti hai jab bhi network topology mein change ho — routers **algorithms** use karke best path calculate karte hain.

| Feature | Detail |
|---|---|
| Configuration | Automatic |
| Algorithm | Complex (Distance Vector, Link State) |
| Security | Static se kam secure |
| CPU Overhead | Zyada (calculations ke liye) |
| Bandwidth Usage | Zyada (routers aapas mein routing info exchange karte hain) |

### Dynamic Routing Ke Advantages
- **Automatic Route Updates**: Topology change hone pe khud update ho jaati hai
- **Efficient Path Selection**: Hop count, cost, delay jaise metrics use karke best path choose karta hai
- **Scalability**: Bade, complex networks ke liye suitable
- **Fault Tolerance**: Link/router fail ho to automatically reroute ho jaata hai

## Comparison Table

| Feature | Static Routing | Dynamic Routing |
|---|---|---|
| Configuration | Manual | Automatic |
| Best For | Chhote networks | Bade networks |
| Security | Zyada | Kam |
| Bandwidth Usage | Kam (zero) | Zyada (routing updates exchange) |
| CPU Usage | Kam (sasta router chal jaata hai) | Zyada |
| Fault Recovery | Manual intervention chahiye | Automatic reroute |
| Scalability | Kam | Zyada |

## Kab Kaunsa Use Karein

| Scenario | Recommendation |
|---|---|
| Chhota, stable network (jaise home network) | Static Routing |
| Bada, complex, frequently-changing network (enterprise/ISP) | Dynamic Routing |

## Viva One-Liners

- **Q: Static routing ka sabse bada disadvantage kya hai?**
 A: Bade networks mein manually manage karna time-consuming aur error-prone hai.
- **Q: Dynamic routing zyada bandwidth kyun use karti hai?**
 A: Kyunki routers periodically ya changes hone pe routing information exchange karte hain.
- **Q: Dynamic routing ka pehla protocol kaunsa tha?**
 A: RIP (Routing Information Protocol), 1980s mein.
