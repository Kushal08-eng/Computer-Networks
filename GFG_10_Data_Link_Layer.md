# Data Link Layer

## Data Link Layer Kya Hai?

**Data Link Layer (DLL)** OSI model ki **2nd layer** hai (Physical Layer ke upar) — same local network ke andar **node-to-node data delivery** ke liye responsible.

| Kaam | Matlab |
|---|---|
| Error-Free Transmission | Information ka error-free transmission ensure karna main role hai |
| Encoding/Decoding | Outgoing/incoming data ko encode, decode, aur organize karta hai |
| Complexity Hide Karna | Hardware ki underlying complexity ko upar wali layers se hide karta hai — isiliye OSI ki sabse complex layer maani jaati hai |

## 2 Sublayers

| Sublayer | Kaam |
|---|---|
| **LLC (Logical Link Control)** | Multiplexing, applications/services ke beech data flow, error messages aur acknowledgments provide karna |
| **MAC (Media Access Control)** | Device ke interaction manage karta hai, frames ko address karta hai, physical media access control karta hai |

## Addressing at Data Link Layer

- Local network/link ke andar devices identify karne ke liye **MAC address** use hoti hai
- MAC address NIC (Network Interface Card) se associated hardware address hoti hai
- Same local network ke devices ke beech, ya connected networks ke point-to-point link mein frames route karne ke liye MAC address use hoti hai
- **Limitation**: Encryption/authentication mechanism nahi hoti — MAC spoofing, ARP poisoning, aur eavesdropping jaise attacks ke liye vulnerable hai
- Sirf LAN ya direct point-to-point connection ke andar operate karti hai — Network Layer (Layer 3) jaisi multiple networks ke across routing nahi kar sakti

## Key Devices at Data Link Layer

| Device | Kaam |
|---|---|
| **Switch** | MAC addresses ke basis pe frames ko sahi port tak forward karta hai — data link layer ka main device |
| **Bridge** | Do network segments ko connect karta hai, traffic reduce karta hai |
| **NIC (Network Interface Card)** | Frames mein MAC address add karti hai, network ke saath proper communication ensure karti hai |
| **Wireless Access Point (WAP)** | Wireless MAC addresses manage karta hai, WiFi (IEEE 802.11) protocol use karta hai |
| **Layer 2 Switches** | Sirf Layer 2 pe operate karte hain (multi-layer switches ke ulta), MAC address tables se frame forwarding karte hain |

## Security Concern

Data Link Layer par **MAC spoofing** ya **ARP poisoning** jaise attacks ho sakte hain. Devices aur frames is layer pe kaise operate karte hain, ye samajhna aise threats detect/mitigate karne mein help karta hai.

## Viva One-Liners

- **Q: Data Link Layer ka main role kya hai?**
 A: Same local network ke andar reliable, error-free node-to-node data delivery.
- **Q: DLL ke 2 sublayers kaunse hain?**
 A: LLC (Logical Link Control) aur MAC (Media Access Control).
- **Q: Data Link Layer pe main device kaunsa hai?**
 A: Switch — MAC address ke basis pe frames forward karta hai.
- **Q: DLL kis type ke attacks ke liye vulnerable hai?**
 A: MAC spoofing aur ARP poisoning, kyunki isme encryption/authentication nahi hoti.
