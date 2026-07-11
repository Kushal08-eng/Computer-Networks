# Internet Group Management Protocol (IGMP)

## IGMP Kya Hai?

**IGMP (Internet Group Management Protocol)** ek Layer 3 (Network Layer) protocol hai jo hosts aur routers ke beech **multicast group memberships** manage karta hai — IPv4 networks mein.

## Unicast vs Multicast

| Type | Matlab |
|---|---|
| **Unicast** | One-to-one communication — ek sender, ek receiver |
| **Multicast** | One-to-many communication — ek sender, multiple interested receivers |

> **Multicasting ka fayda**: Sender ek hi baar data bhejta hai, aur network sabhi interested receivers tak deliver karta hai — individual unicast streams bhejne se zyada efficient hai (IPTV, live streaming, gaming, financial data jaisi applications mein use hota hai).

## IGMP Kaise Kaam Karta Hai

- **Multicast Addressing**: Multicast groups **Class D IP addresses** (224.0.0.0 – 239.255.255.255) use karte hain
- Host apne local router ko batata hai ki wo kisi multicast group ka member banna chahta hai
- Router periodically **Membership Queries** bhejta hai — check karne ke liye kaunse groups active hain

## IGMP Message Types

| Message | Kaam |
|---|---|
| **Membership Query** | Router se — check karta hai kaunse multicast groups active hain |
| **Membership Report** | Host se — group join karne ki interest batata hai |
| **Leave Group** | Host se — jab ab traffic nahi chahiye |
| **IGMPv3 Membership Report** | Exact multicast addresses aur sources specify kar sakta hai (Source-Specific Multicast support) |

## IGMP Ke Versions

| Version | Year | Key Feature |
|---|---|---|
| **IGMPv1** | 1989 | Basic join capability, but explicit "leave" nahi tha (timeout ka wait karna padta tha) |
| **IGMPv2** | 1997 | "Leave Group" message add hua — timeout delays kam hue |
| **IGMPv3** | 2002+ | Source-Specific Multicast (SSM) support, membership report aggregation |

> Teeno versions **backward compatible** hain.

## IGMP Snooping

**IGMP Snooping** ek feature hai jisse Layer 2 **switches** IGMP messages ko "sunte" hain aur multicast groups ko sahi ports tak map karte hain — isse unnecessary flooding avoid hoti hai (kyunki normally switches Layer 2 pe hi operate karte hain, IGMP jaisi Layer 3 info unhe pata nahi hoti).

## IGMP Ke Fayde Aur Limitations

| Fayde | Limitations |
|---|---|
| Efficient multicast distribution | Local network tak hi limited (inter-LAN nahi) |
| Traffic reduce hoti hai (sirf interested hosts ko data) | Large networks mein configuration complex ho sakti hai |
| Scalable — streaming/gaming jaisi applications ke liye | DoS attacks ke liye vulnerable ho sakta hai |

## Viva One-Liners

- **Q: IGMP kis layer pe operate karta hai?**
 A: Layer 3 (Network Layer).
- **Q: Multicast addresses kaunsi class use karte hain?**
 A: Class D (224.0.0.0 – 239.255.255.255).
- **Q: IGMP Snooping ka fayda kya hai?**
 A: Switches ko multicast traffic sahi ports tak forward karne mein help karta hai, unnecessary flooding avoid karke.
- **Q: IPv6 mein IGMP ki jagah kya use hota hai?**
 A: MLD (Multicast Listener Discovery).
