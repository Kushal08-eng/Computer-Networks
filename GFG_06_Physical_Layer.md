# Physical Layer

## Physical Layer Kya Hai?

**Physical Layer** OSI model ki sabse neeche wali layer hai, jo network hardware ke through raw data bits transmit karne ke liye responsible hai.

| Kaam | Matlab |
|---|---|
| Physical/Electrical Transmission | Data ka physical/electrical level pe transmission handle karta hai |
| Hardware | Cables, connectors, plugs, receivers include hote hain |
| Raw Bits Transfer | Devices ke beech raw bits transfer karta hai |
| Standards | Hardware standards aur signal types define karta hai |

## Functions of Physical Layer

- Raw data ko **bits** ki form mein physical medium ke through bhejne ke liye responsible hai
- Data ko signals mein convert karta hai jo wires, fiber optics, ya wireless channels se travel kar sakein (**Encoding**), aur receiver pe signals ko wapas data mein convert karta hai (**Decoding**)
- Signals sahi se transmit hon, iske liye **Modulation** (transmission ke liye data prepare karna) aur **Demodulation** (dusre end pe data retrieve karna) techniques use karta hai
- Data flow ka direction (one-way, two-way alternately, ya simultaneously) **Transmission Modes** se decide karta hai, aur transmission ki speed/timing control karta hai

## Physical Topologies — Line Configuration

| Configuration | Matlab |
|---|---|
| **Point-to-Point** | Do devices ke beech ek dedicated line (link), sirf unhi do ke beech data carry karta hai |
| **Multi-Point** | Ek line ke through multiple devices connected hote hain |

*(Detailed topology types — Bus, Star, Ring, Mesh, Tree, Hybrid — alag note file mein cover ki gayi hain.)*

## Protocols in Physical Layer

Physical layer hardware aur software programming ka combination hota hai, jisme kuch Layer 1 protocols shaamil hote hain:

| Protocol | Use |
|---|---|
| **Ethernet (IEEE 802.3)** | Wired networks ke liye widely used |
| **Wi-Fi (IEEE 802.11)** | Wireless communication ke liye |
| **Bluetooth (IEEE 802.15.1)** | Short-range wireless communication |
| **USB** | Short distances mein devices connect karne ke liye |

## Physical Layer Aur Security

Physical Layer security ke liye essential hai, kyunki bahut saare attacks kisi bhi software involve hone se pehle ho sakte hain — threats directly hardware ya transmission medium ko target karte hain.

| Threat | Matlab |
|---|---|
| **Cable Tapping** | Hackers network cables se directly connect karke data intercept kar sakte hain |
| **Physical Access** | Bina permission server rooms/hardware areas mein access milne se equipment steal/damage ho sakta hai |
| **Wireless Signal Interception** | Attackers WiFi signals ko bahar se special tools se capture kar sakte hain |
| **Hardware Manipulation** | Routers/USB ports jaise physical devices ke saath tamper karke secretly harmful software install kiya ja sakta hai |

## Applications

- Devices raw data physical mediums ke through transmit/receive kar sakein, ye ensure karta hai
- Cables, connectors, signaling ke liye universal standards deta hai, compatibility ensure karta hai
- Wired (Ethernet) aur wireless (WiFi) dono technologies ke saath kaam karta hai

## Viva One-Liners

- **Q: Physical layer ka main kaam kya hai?**
 A: Raw bits ko physical medium ke through transmit karna — encoding/decoding aur signal synchronization ke saath.
- **Q: Point-to-Point aur Multi-Point configuration mein difference?**
 A: Point-to-Point mein ek dedicated line sirf do devices ke beech hoti hai; Multi-Point mein ek line se multiple devices connected hote hain.
- **Q: Physical layer pe security threats kaunse hain?**
 A: Cable tapping, unauthorized physical access, wireless signal interception, hardware manipulation.
