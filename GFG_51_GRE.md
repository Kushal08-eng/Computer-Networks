# Generic Routing Encapsulation (GRE)

## GRE Kya Hai?

**GRE (Generic Routing Encapsulation)** Cisco ka banaya hua ek **tunneling protocol** hai jo ek network protocol ko dusre ke andar **encapsulate** (wrap) kar deta hai — packets ko securely aur efficiently ek network se dusre tak transport karne ke liye.

> **Analogy**: Jaise ek car ko ferry pe load karke samundar paar kiya jaata hai (jahan car khud nahi jaa sakti) — GRE bhi ek type ke packet (jaise IPv6) ko dusre type ke packet (jaise IPv4) ke andar "load" karke aise network se guzarta hai jo original protocol support nahi karta.

## GRE Kaise Kaam Karta Hai

Jab GRE configure hota hai do routers ke beech, original IP packet ko **2 extra headers** ke saath encapsulate kiya jaata hai:

| Header | Kaam |
|---|---|
| **GRE Header** | Tunnel ke liye information deta hai — ek naye IP header ki tarah kaam karta hai |
| **Delivery Header** | Tunnel endpoints ke naye source/destination IP addresses contain karta hai |

> Sirf GRE-configured routers hi in headers ko encrypt/decrypt/interpret kar sakte hain — beech ke routers sirf **outer (delivery) header** dekhte hain, encapsulated packet ko nahi.

## GRE Tunneling Ka Example

1. PC1 kisi server ko data bhejta hai jo dusre subnet mein hai
2. Router R1 original IP packet receive karta hai aur usse GRE Header + Delivery Header (naye tunnel source/destination) ke saath encapsulate karta hai
3. Encapsulated packet intermediate network se travel karta hai (normal routing se)
4. Router R2 GRE packet receive karta hai, dono headers **remove** karta hai, aur original packet ko server tak forward karta hai

## GRE Ke Fayde

| Fayda | Matlab |
|---|---|
| **Multiprotocol Support** | IPv4, IPv6, multicast, aur non-IP protocols (jaise IPX) bhi carry kar sakta hai |
| **Transparent Communication** | Alag/separated networks ke beech seamless connectivity |
| **Routing Protocol Compatible** | EIGRP, OSPF, BGP jaise protocols ke saath kaam kar sakta hai |
| **Discontinuous Networks Connect** | Alag-alag subnets ko connect kar sakta hai jo directly connected nahi hain |
| **VPN Support** | WAN ke across VPN setup karne mein help karta hai |

## GRE Ki Limitations

| Limitation | Matlab |
|---|---|
| **No Encryption** | GRE sirf encapsulation deta hai, security nahi — isliye **IPsec** ke saath pair kiya jaata hai |
| **Overhead** | Extra headers packet size badhate hain, performance thoda affect ho sakta hai |
| **Stateless** | GRE ko dusre tunnel end ki state/availability ka pata nahi hota |

## GRE vs IPsec

| Feature | GRE | IPsec |
|---|---|---|
| Encapsulation | Haan | Haan |
| Encryption | Nahi | Haan |
| Multicast/Non-IP Support | Haan | Limited |
| Common Use | GRE + IPsec combo (secure tunneling ke liye) | Security-focused tunneling |

## Viva One-Liners

- **Q: GRE ka main kaam kya hai?**
 A: Ek network protocol ke packet ko dusre protocol ke packet ke andar encapsulate (tunnel) karna.
- **Q: GRE security kyun nahi deta khud se?**
 A: Kyunki GRE sirf encapsulation protocol hai — isliye secure tunneling ke liye IPsec ke saath combine kiya jaata hai.
- **Q: GRE packet mein kaunse 2 extra headers add hote hain?**
 A: GRE Header aur Delivery Header.
