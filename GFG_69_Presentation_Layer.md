# Presentation Layer

## Presentation Layer Kya Hai?

**Presentation Layer** OSI model ki **6th layer** hai — data ko **translate, encrypt, compress, aur format** karti hai, taaki communicating systems ek dusre ko correctly samajh sakein.

> Isi wajah se ye **"Translation Layer"** ya **"Syntax Layer"** bhi kehlaati hai.

## Presentation Layer Kaise Kaam Karti Hai

- Jab **Application Layer** data generate karti hai, Presentation Layer use ek **standard form** mein convert karti hai (transmission ke liye)
- Jab data **receive** hota hai, ye use receiving system ke process karne layak format mein translate karti hai

## Presentation Layer Ke Core Functions

| Function | Matlab |
|---|---|
| **Data Translation** | Application ke format ko standard network format mein convert karti hai (jaise ASCII ↔ Unicode, ASCII ↔ EBCDIC) |
| **Data Compression** | Data size kam karti hai transmission se pehle — bandwidth save hoti hai, speed badhti hai |
| **Encryption/Decryption** | Plain text ko ciphertext mein convert karti hai (encryption), aur wapas (decryption) — key values use karke |
| **Syntax & Semantics** | Data ka proper structure aur meaning maintain karti hai |
| **Compatibility** | Alag-alag systems/devices ke beech compatibility ensure karti hai |

## Presentation Layer Ke Protocols

| Protocol | Kaam |
|---|---|
| **AFP** | macOS ke liye file services protocol |
| **NCP** | Novell NetWare mein file/print services |
| **LPP** | ISO presentation services TCP/IP stacks pe |
| **NDR / XDR** | Network communication ke liye data types/representation define karte hain |
| **SSL / TLS** | Encryption aur secure communication |

*(In sabka detail alag note files mein hai.)*

## Security Concern

Presentation Layer data formatting, compression, aur encryption handle karti hai — isliye ye attackers ka common target hoti hai:

| Attack | Matlab |
|---|---|
| **Man-in-the-Middle (MITM)** | Communication intercept karke sensitive data churana |
| **SSL/TLS Downgrade Attacks** | Jaan-boojh kar weaker encryption protocol use karwaana |

## Viva One-Liners

- **Q: Presentation Layer ko "Translation Layer" kyun kehte hain?**
 A: Kyunki ye data ko ek format se dusre mein translate karti hai, taaki dono systems ek dusre ko samajh sakein.
- **Q: Presentation Layer OSI ki kaunsi layer hai?**
 A: 6th layer.
- **Q: Presentation Layer ke 3 main functions kya hain?**
 A: Translation, Compression, aur Encryption/Decryption.
