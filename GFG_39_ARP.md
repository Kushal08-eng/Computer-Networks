# Address Resolution Protocol (ARP)

## ARP Kya Hai?

**ARP (Address Resolution Protocol)** ek IPv4 address ko corresponding **MAC address** mein map karta hai — taaki local network ke andar frames sahi device tak deliver ho sakein.

> **Zaroorat**: Data destination tak pahunchane ke liye IP address kaafi hai, but usi network ke andar physically frame deliver karne ke liye **MAC address** chahiye hoti hai (Data Link Layer). ARP is gap ko bridge karta hai.

## ARP Kaise Kaam Karta Hai

1. Device A, Device B se baat karna chahta hai, but sirf uska IP address pata hai, MAC nahi
2. Device A ek **ARP Request** (broadcast message) poore local network mein bhejta hai — "Ye IP kiski hai? Apna MAC address batao"
3. Jis device ka wo IP hai, wo ek **ARP Reply** (unicast message) bhejta hai apne MAC address ke saath
4. Device A apna **ARP Cache** update kar leta hai is mapping ke saath, aur ab directly data bhej sakta hai

## Key Terms

| Term | Matlab |
|---|---|
| **ARP Cache** | Temporary table jisme recently resolved IP-to-MAC mappings store hoti hain — repeated requests avoid karta hai |
| **ARP Cache Timeout** | Time duration jab tak entry valid rehti hai; expire hone pe remove ho jaati hai |
| **ARP Request** | Broadcast message — jab kisi IP ka MAC cache mein nahi hota |
| **ARP Reply** | Unicast message — jo device wo IP "owns" karta hai, wahi reply deta hai |

## ARP Packet Fields

| Field | Kaam |
|---|---|
| Hardware Type | Kaunsi hardware technology use ho rahi hai (Ethernet = 1) |
| Protocol Type | Kaunsa protocol use ho raha hai (IPv4 = 2048) |
| Hardware Address Length | MAC address ki length (6 bytes) |
| Protocol Address Length | IP address ki length (4 bytes) |
| Operation | Request (1) ya Reply (2) |

## ARP Ke Types

| Type | Kaam |
|---|---|
| **Proxy ARP** | Router dusre network ke device ki taraf se ARP request ka reply deta hai — sender ko lagta hai destination usi network mein hai |
| **Gratuitous ARP** | Device khud apni IP-to-MAC mapping announce/update karta hai — duplicate IP addresses detect karne ke liye bhi use hota hai |
| **Inverse ARP (InARP)** | MAC address se IP address dhoondhta hai (ARP ka ulta) — mainly ATM networks mein |

## ARP Ki Limitations

| Limitation | Matlab |
|---|---|
| **Security** | ARP Spoofing attacks ka risk — attacker galat MAC-IP mapping bhej sakta hai |
| **Broadcast Traffic** | Bade networks mein congestion badha sakta hai |
| **No Authentication** | ARP devices ki identity verify nahi karta |

## Viva One-Liners

- **Q: ARP ka main kaam kya hai?**
 A: IPv4 address ko corresponding MAC address mein resolve/map karna.
- **Q: ARP Request kis type ka message hota hai?**
 A: Broadcast.
- **Q: ARP Cache kya karta hai?**
 A: Recently resolved IP-to-MAC mappings store karta hai, taaki baar-baar ARP request na karni pade.
- **Q: IPv6 mein ARP ki jagah kya use hota hai?**
 A: NDP (Neighbor Discovery Protocol).
