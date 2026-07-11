# Basics of Computer Networking

## Computer Network Kya Hai?

**Computer Network** interconnected devices ka ek collection hai jo aapas mein data aur resources exchange karne ke liye communicate karte hain — email, file sharing, aur internet access jaisi services isi ki wajah se possible hoti hain.

> **Analogy**: Jaise city ki roads ghar-office ko connect karti hain taaki log aana-jaana kar sakein — waise hi network cables/signals devices ko connect karte hain taaki data travel kar sake.

**Basic Building Blocks:**

| Component | Kaam |
|---|---|
| **Nodes** | Physical devices — computer, mobile, printer |
| **Routers/Switches** | Information ka flow control karte hain |
| **Transmission Media** | Data ko ek device se dusre tak carry karta hai |
| **Wired Media** | Ethernet cables, optical fiber |

## Network Kaam Kaise Karta Hai (Working)

Network devices ek shared communication system use karke data exchange karte hain — har device kuch predefined rules follow karta hai taaki data accurately, efficiently, aur securely transmit ho.

**Step-by-Step Flow:**

1. Network mein **nodes** (computers, servers, routers, switches) hote hain jo data bhejte/receive karte hain
2. Ye nodes **links** se connected hote hain — wired (cables, fiber) ya wireless (WiFi, radio signals)
3. Data bhejte waqt, use chhote **packets** mein toda jaata hai
4. **Protocols** decide karte hain data kaise format, transmit, receive, aur acknowledge hoga
5. Har device ka ek unique **IP address** hota hai, jisse data sahi destination tak pahunche
6. **Switches aur Routers** data packets ko best available path se forward karte hain
7. **Firewalls** jaise security mechanisms traffic monitor karte hain aur security rules ke hisaab se allow/block karte hain

> **Analogy**: Jaise dak (post) system mein letter ko address ke hisaab se sahi ghar tak pahunchaya jaata hai, sorting offices (routers) route decide karte hain, aur security check (firewall) hoti hai — network mein data packets ke saath bhi wahi hota hai.

## Types of Network Architecture

| Architecture | Matlab |
|---|---|
| **Client-Server** | Kuch nodes **server** ka role play karte hain (resources manage karte hain), baaki **client** hote hain jo request karte hain |
| **Peer-to-Peer (P2P)** | Koi central server nahi hota — har device client aur server dono ka kaam kar sakta hai |

## Network Devices (Quick Overview)

| Device | Kaam |
|---|---|
| **Router** | Multiple networks ko connect karta hai, IP address se best path decide karta hai |
| **Switch** | Ek hi network ke andar devices ko connect karta hai, sirf destination device ko data bhejta hai |
| **Hub** | Sabko data broadcast karta hai (koi filtering nahi, less secure) |
| **Bridge** | Do network segments ko connect karta hai, MAC address se traffic filter karta hai |
| **Gateway** | Do alag protocols wale networks ko connect/translate karta hai |
| **Access Point (AP)** | Wired network ko wireless (WiFi) mein extend karta hai |
| **Modem** | Digital data ko analog signal mein convert karta hai (aur vice-versa) ISP connection ke liye |
| **Firewall** | Security device jo traffic monitor/control karta hai |

*(Har device ka detailed breakdown "Network Devices" wali note file mein hai.)*

## Network Ke Goals Aur Uses

| Goal | Matlab |
|---|---|
| **Resource Sharing** | Hardware, software, data ko multiple users efficiently share kar sakein |
| **Internet/Cloud Access** | Internet aur cloud-based services tak access milta hai |
| **Cost Efficiency** | Shared resources aur centralized systems se cost kam hoti hai |
| **Reliability & Availability** | Backup paths aur fault-tolerant mechanisms se system reliable banta hai |
| **Scalability** | Naye devices/services easily add kiye jaa sakte hain |
| **Security & Control** | Authentication, access control, monitoring se data protect hota hai |

## Viva One-Liners

- **Q: Computer network ka basic definition kya hai?**
 A: Interconnected devices ka collection jo data/resources exchange karne ke liye communicate karte hain.
- **Q: Client-Server aur P2P architecture mein basic difference?**
 A: Client-Server mein dedicated server hota hai jo clients ko manage karta hai; P2P mein koi central server nahi, har device dono role play karta hai.
- **Q: Network mein data kaise travel karta hai?**
 A: Data ko packets mein todke, protocols ke rules follow karte hue, IP addressing aur routing devices (switch/router) ke through destination tak bheja jaata hai.
