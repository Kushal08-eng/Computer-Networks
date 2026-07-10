# Middle Boxes

## Middlebox Kya Hai?

**Middlebox** wo network device hai jo sender aur receiver ke **beech mein** baithke traffic ko modify, filter, ya monitor karta hai — ye sirf simple forwarding nahi karta, balki actively data pe kaam karta hai.

> **Analogy**: Jaise ek security guard building ke entrance pe har visitor ko check karta hai, kabhi kisi ko andar nahi jaane deta, kabhi kisi ka bag search karta hai — middlebox bhi network traffic ke saath aisa hi kuch karta hai.

## Common Types of Middleboxes

| Middlebox | Kaam |
|---|---|
| **Firewall** | Traffic ko allow/block karta hai security rules ke basis pe |
| **NAT Device** | Private IP ko public IP mein translate karta hai |
| **Load Balancer** | Traffic ko multiple servers mein distribute karta hai |
| **Proxy Server** | Client ki taraf se requests forward karta hai (anonymity/caching ke liye) |
| **Intrusion Detection System (IDS)** | Suspicious traffic detect karta hai |

## Middleboxes Kyun Use Hote Hain

| Purpose | Matlab |
|---|---|
| Security | Malicious traffic ko block karna |
| Performance | Load balancing, caching se speed improve karna |
| Address Management | NAT se limited public IPs ko efficiently use karna |
| Monitoring | Traffic analysis, logging |

## Challenge

Middleboxes kabhi-kabhi end-to-end principle (jo original internet design mein tha — sirf endpoints hi smart hone chahiye) ko violate karte hain, isse debugging aur naye protocols design karna mushkil ho jaata hai.

## Viva One-Liner

> "Middlebox ek network device hai jo sender-receiver ke beech traffic ko modify/filter/monitor karta hai — jaise Firewall, NAT, Load Balancer."
