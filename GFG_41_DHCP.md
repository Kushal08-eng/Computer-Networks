# Dynamic Host Configuration Protocol (DHCP)

## DHCP Kya Hai?

**DHCP (Dynamic Host Configuration Protocol)** ek network management protocol hai jo devices ko **automatically** IP address aur baaki network configuration (subnet mask, default gateway, DNS server) assign karta hai — manually configure karne ki zaroorat khatam kar deta hai.

| Detail | Value |
|---|---|
| Layer | Application Layer (UDP ke upar) |
| Server Port | 67 |
| Client Port | 68 |
| Type | Client-Server protocol |

## DHCP Kaise Kaam Karta Hai — DORA Process

DHCP mein 4 messages exchange hote hain — **DORA** (Discover, Offer, Request, Acknowledgement):

| Step | Message | Kaun Bhejta Hai | Kaam |
|---|---|---|---|
| 1 | **Discover** | Client → Broadcast | "Mujhe IP address chahiye" |
| 2 | **Offer** | Server → Client | Server ek available IP offer karta hai |
| 3 | **Request** | Client → Broadcast | Client offered IP ko formally request karta hai |
| 4 | **Acknowledgement (ACK)** | Server → Client | Server IP lease confirm karta hai |

> Agar multiple DHCP servers exist karte hain aur client ko multiple Offers milte hain, to client sirf **ek** offer accept karta hai (Request message se), baaki offers automatically decline ho jaate hain.

## Key Terms

| Term | Matlab |
|---|---|
| **IP Address Pool** | DHCP server ke paas available addresses ka range |
| **Lease** | Kitni der tak allocated IP valid rahegi — expire hone pe renew karna padta hai |
| **DNS Servers** | DHCP DNS server info bhi provide kar sakta hai |
| **Default Gateway** | Router jahan external destination ke packets bheje jaate hain |
| **Subnets** | Network ke chhote logical segments |

## DHCP Ka Fayda

| Fayda | Matlab |
|---|---|
| **Automatic Configuration** | Manual IP assignment ki zaroorat khatam |
| **Centralized Management** | Admin ek jagah se poora IP allocation control karta hai |
| **Conflict Prevention** | Duplicate IP addresses assign nahi hoti |
| **Efficient IP Utilization** | Device disconnect ho to uski IP wapas pool mein aa jaati hai, reuse ho sakti hai |

## DHCP Server Local Network Se Bahar Ho Toh?

Agar DHCP server local LAN mein nahi hai, to **IP Helper Address** configure kiya jaata hai routers pe — jisse DORA messages LAN ke bahar wale DHCP server tak forward ho sakein.

## Viva One-Liners

- **Q: DHCP kaunse layer pe kaam karta hai aur kaunsa protocol use karta hai?**
 A: Application Layer, UDP ke upar (Server: port 67, Client: port 68).
- **Q: DORA process ke 4 steps kya hain?**
 A: Discover, Offer, Request, Acknowledgement.
- **Q: DHCP ka main fayda kya hai?**
 A: IP address assignment ko automatic banana, manual configuration ki zaroorat khatam karna.
