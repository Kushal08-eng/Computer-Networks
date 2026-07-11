# Multiprotocol Label Switching (MPLS)

## MPLS Kya Hai?

**MPLS (Multiprotocol Label Switching)** ek advanced packet-forwarding technique hai jo traditional IP routing ke complex Layer 3 lookup ki jagah, **labels** use karke fast forwarding decisions leti hai.

> MPLS OSI model ki **Layer 2 aur Layer 3 ke beech** operate karta hai — isliye ise **"Layer 2.5 protocol"** bhi kehte hain.

## Traditional IP Routing vs MPLS

| Traditional IP Routing | MPLS |
|---|---|
| Har router poori routing table lookup karta hai har packet ke liye | Short, fixed-length **label** ke basis pe forward hota hai |
| Slower (complex lookup) | Fast (simple label lookup) |
| Har hop pe independent decision | Pehle se defined path (Label Switch Path) follow hota hai |

## MPLS Kaise Kaam Karta Hai

- Ek 32-bit **MPLS header** Layer 2 aur Layer 3 headers ke beech insert hoti hai
- Packet ko ek **label** assign hoti hai jo uska predefined path (**Label Switch Path — LSP**) represent karti hai
- Har hop pe, router sirf label dekh ke agla step decide karta hai — poore IP header ki analysis nahi karni padti

## Key Devices/Roles

| Term | Kaam |
|---|---|
| **CE Router (Customer Edge)** | Customer network ke edge pe, PE routers se communicate karta hai |
| **PE Router (Provider Edge)** | MPLS provider network ke edge pe — labels add/remove karta hai |
| **LSR (Label Switch Router)** | MPLS core ke andar, labels process karta hai |
| **Ingress LSR** | Pehla router — CE se packet leke MPLS header **push** (add) karta hai |
| **Intermediate LSR** | Labels ko **swap** (replace) karta hai jaise-jaise packet path pe aage badhta hai |
| **Egress LSR** | Last router — MPLS header **pop** (remove) karke packet CE ko deta hai |

## Push, Pop, Swap

| Operation | Matlab |
|---|---|
| **Push** | Label add karna |
| **Pop** | Label remove karna |
| **Swap** | Existing label ko naye label se replace karna |

## MPLS Ke Fayde

| Fayda | Matlab |
|---|---|
| Faster Packet Forwarding | Label-based forwarding, complex lookup avoid karta hai |
| Multi-Protocol Support | IPv4, IPv6, aur non-IP protocols bhi support karta hai |
| Traffic Engineering | Network resources ka efficient use |
| Quality of Service (QoS) | Different traffic types ko prioritize kar sakta hai |
| Layer 3 VPN Support | Scalable VPN solutions banane mein help karta hai |
| Loop Prevention | TTL mechanism se reliable |

## MPLS Ki Limitations

| Limitation | Matlab |
|---|---|
| No Encryption | MPLS data encrypt nahi karta — isliye IPsec ke saath pair kiya jaata hai |
| Expensive | IP routing ke muqable implement karna costly |
| Complex | Configuration aur management complex hoti hai |
| Small Networks Ke Liye Overkill | Chhote networks ke liye zyada beneficial nahi |

## Viva One-Liners

- **Q: MPLS ko "Layer 2.5 protocol" kyun kehte hain?**
 A: Kyunki ye Layer 2 aur Layer 3 headers ke beech operate karta hai.
- **Q: MPLS traditional IP routing se fast kyun hai?**
 A: Kyunki complex routing table lookup ki jagah, sirf fixed-length label check karta hai forwarding decision ke liye.
- **Q: MPLS security ke liye kya missing hai?**
 A: Encryption — isliye MPLS ko IPsec ke saath pair kiya jaata hai secure tunneling ke liye.
