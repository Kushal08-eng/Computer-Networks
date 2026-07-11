# Intermediate System to Intermediate System (IS-IS)

## IS-IS Kya Hai?

**IS-IS (Intermediate System to Intermediate System)** ek **standardized link-state routing protocol** hai — originally OSI model ke liye definitive routing protocol banaya gaya tha.

| Detail | Value |
|---|---|
| Type | Link-state, IGP |
| Best Path Calculation | Link-state advertisements se poori network map banata hai, phir shortest path calculate karta hai |
| Usage | Mainly **ISP environments** mein predominantly use hota hai |

## IS-IS Kaise Kaam Karta Hai

Link-state protocols (jaise IS-IS) ki khasiyat hai — poori network connectivity map banane ke liye required information circulate karna, har participating router pe. Ye map phir destinations tak shortest path calculate karne ke liye use hoti hai.

## IS-IS vs OSPF

| Feature | IS-IS | OSPF |
|---|---|---|
| Origin | OSI model ke liye develop hua | TCP/IP suite ke liye develop hua |
| New Concepts | — | Authentication, VLSM, route summarization introduce kiye |
| Common Use | ISP (Internet Service Provider) networks | Enterprise networks |
| Algorithm | Link-state (Dijkstra) | Link-state (Dijkstra) |

> Dono protocols **link-state** hain aur similar core concept follow karte hain — har router poori network topology ki map banata hai, phir shortest path calculate karta hai.

## Viva One-Liners

- **Q: IS-IS kis type ka protocol hai?**
 A: Link-state Interior Gateway Protocol (IGP).
- **Q: IS-IS kahan predominantly use hota hai?**
 A: ISP (Internet Service Provider) environments mein.
- **Q: IS-IS aur OSPF mein similarity kya hai?**
 A: Dono link-state protocols hain, poori network topology map banate hain aur shortest path calculate karte hain.
