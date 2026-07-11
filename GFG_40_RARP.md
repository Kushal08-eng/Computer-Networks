# Reverse Address Resolution Protocol (RARP)

## RARP Kya Hai?

**RARP (Reverse Address Resolution Protocol)** ARP ka **opposite** kaam karta hai — jab device ko apna **MAC address pata ho but IP address nahi**, to RARP use karke apni IP address dhoondhta hai.

> ARP: IP address se MAC address dhoondhta hai.
> RARP: MAC address se IP address dhoondhta hai.

## RARP Kyun Zaroori Tha

RARP mainly **diskless workstations** ke liye develop hua tha — aise devices jinke paas apna IP address store karne ki memory/storage nahi hoti thi. System startup ke waqt, aisa device apna IP address kisi server se maangta tha.

## RARP Kaise Kaam Karta Hai

1. Device apna **MAC address** jaanta hai, IP address nahi
2. Wo ek **RARP Request** broadcast karta hai apne MAC address ke saath
3. Local network mein ek dedicated **RARP Server** hota hai jo apne IP-to-MAC mapping table mein check karta hai
4. Agar match milta hai, RARP server ek **RARP Reply** bhejta hai us device ke liye assigned IP address ke saath
5. Device wo IP address apna kar leta hai

## RARP Packet Format

RARP packet ka format ARP jaisa hi hota hai, sirf **Operation field** alag hoti hai:

| Operation Value | Matlab |
|---|---|
| 3 | RARP Request |
| 4 | RARP Reply |

## RARP Ki Limitation

- Ek **dedicated RARP server** same local network segment mein hona zaroori tha
- Sirf **IP address** deta tha — subnet mask, default gateway, DNS jaisi baaki configuration nahi

## RARP Aaj Kal Kyun Use Nahi Hota

RARP ab **obsolete** hai — ise zyada efficient aur scalable protocols ne replace kar diya:

| Replaced By | Extra Fayda |
|---|---|
| **BOOTP** | Poori network configuration de sakta tha, na ki sirf IP |
| **DHCP** | Automatic, dynamic, aur scalable — aaj bhi widely use hota hai |

## ARP vs RARP — Quick Comparison

| Feature | ARP | RARP |
|---|---|---|
| Direction | IP → MAC | MAC → IP |
| Mapping | 32-bit IP se 48-bit MAC | 48-bit MAC se 32-bit IP |
| Status | Aaj bhi widely used | Obsolete (BOOTP/DHCP ne replace kiya) |
| Server Zaroori? | Nahi | Haan (dedicated RARP server) |

## Viva One-Liners

- **Q: RARP ka main kaam kya hai?**
 A: Device ko sirf uski MAC address se, apni IP address dhoondhne mein help karna.
- **Q: RARP kisne replace kiya?**
 A: BOOTP, aur baad mein DHCP ne.
- **Q: RARP kis type ke devices ke liye use hota tha?**
 A: Diskless workstations, jinke paas IP address store karne ki storage nahi hoti thi.
