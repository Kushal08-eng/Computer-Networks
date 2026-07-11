# Virtual LAN (VLAN)

## VLAN Kya Hai?

**VLAN (Virtual LAN)** ek logical grouping hai devices ki, jo unhe same local network jaisa behave karne deta hai — chahe wo physically alag-alag switches se connected hon. Ye Layer 2 switch pe create hoti hai, **broadcast domain** ka size reduce karne ke liye.

> **Analogy**: Ek hi room mein alag-alag groups of friends baithe hain, but har group sirf apne group ke logo se hi baat kar sakta hai — physical room same hai, but logical separation hai.

**VLAN Ke Fayde:**

| Fayda | Matlab |
|---|---|
| Broadcast Traffic Kam | Unnecessary broadcast traffic reduce karta hai |
| Security | Traffic isolation se security better hoti hai |
| Performance | Network performance aur manageability improve hoti hai |
| Flexibility | Ek hi physical infrastructure pe multiple logical networks coexist kar sakte hain |

## VLAN Communication

| Type | Kaise Hota Hai |
|---|---|
| **Same VLAN** | Devices directly same broadcast domain ke andar communicate karte hain |
| **Different VLANs** | Communication ke liye **Inter-VLAN Routing** chahiye (router ya Layer 3 switch se) |

## VLAN Tagging (IEEE 802.1Q)

- Ethernet frames mein ek **4-byte VLAN tag** insert kiya jaata hai — batata hai frame kaunsi VLAN se belong karta hai
- **VLAN Membership**: Devices ko switch port, MAC address, ya protocol type ke basis pe VLAN assign ki ja sakti hai
- **VLAN Trunking**: Ek hi physical link pe multiple VLANs share ho sakti hain (VLAN-aware devices ke beech)
- **VLAN 1**: Default VLAN — delete nahi ho sakti, control/management protocols (STP, CDP, VTP) ke liye common use hoti hai

## Types of VLAN

| Type | Kaam |
|---|---|
| **Default VLAN** | Switch start hote hi sab ports isi VLAN (usually VLAN 1) ke member ban jaate hain |
| **Data VLAN** | Sirf user-generated data traffic ke liye (voice/management traffic nahi) |
| **Voice VLAN** | Voice traffic (VoIP) ke liye — high priority di jaati hai low latency ke liye |
| **Management VLAN** | Switch ki management capabilities (logging, monitoring) access karne ke liye |
| **Native VLAN** | Trunk link ke har end se aane wale **untagged** traffic ko identify karti hai |

### Configuration-Based Types

| Type | Matlab |
|---|---|
| **Port-Based VLAN** | Har switch port ek specific VLAN ko assign hota hai — us port ka saara traffic automatically usi VLAN mein jaata hai |
| **Tagged VLAN** | Ek hi physical port pe multiple VLANs support karta hai — har packet VLAN ID se tag hoti hai |
| **Protocol-Based VLAN** | Layer 3 protocol information use karke packets VLAN assign hoti hain |

## VLAN Use Cases

| Use Case | Kyun |
|---|---|
| Cloud/Data Centers | Tenant workloads ko logically isolate karna |
| IoT Networks | IoT devices segment karke security risk kam karna |
| VoIP/Video Conferencing | QoS ensure karne ke liye traffic prioritize karna |

## Challenges/Risks

| Risk | Matlab |
|---|---|
| **VLAN Hopping** | Misconfiguration se attacker ek VLAN se dusri VLAN tak unauthorized access le sakta hai |
| **Interoperability** | Legacy/non-standard devices ke saath compatibility issues |
| **Troubleshooting** | Isolated traffic flows ki wajah se fault diagnose karna complex ho sakta hai |

## Viva One-Liners

- **Q: VLAN kis layer pe create hoti hai?**
 A: Layer 2 (Data Link Layer) switch pe.
- **Q: VLAN tagging kaunsa standard use karta hai?**
 A: IEEE 802.1Q.
- **Q: Different VLANs ke devices aapas mein kaise communicate karte hain?**
 A: Inter-VLAN Routing ke through — router ya Layer 3 switch chahiye.
- **Q: VLAN hopping kya hai?**
 A: Ek security risk jisme misconfiguration ki wajah se attacker unauthorized VLAN tak pahunch sakta hai.
