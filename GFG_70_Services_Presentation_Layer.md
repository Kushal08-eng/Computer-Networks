# Services Provided by Presentation Layer

## Presentation Layer Ki Services

Presentation Layer, Application Layer (Layer 7) aur lower layers ke beech **translator** ka kaam karti hai — ensure karti hai ki sender ka data receiver ke system ko samajh aa jaaye, chahe encoding/encryption/compression mein differences hi kyun na hon.

## Detailed Services

### 1. Character Encoding Translation
Alag systems alag encoding formats use kar sakte hain data represent karne ke liye (jaise ASCII, Unicode, EBCDIC) — Presentation Layer inke beech translate karti hai taaki data har system pe correctly display ho.

### 2. Data Compression
Transmission se pehle data ki size kam karti hai:

| Fayda | Matlab |
|---|---|
| Faster Transmission | Kam data bhejna padta hai |
| Bandwidth Saving | Network resources efficiently use hote hain |

### 3. Encryption & Decryption
Security ke liye data ko encode karti hai:

| Step | Kaam |
|---|---|
| **Encryption** | Sender side pe plain text ko ciphertext mein convert karti hai |
| **Decryption** | Receiver side pe ciphertext ko wapas readable form mein convert karti hai |

### 4. Format Conversion
Different file formats/media types (images, videos, documents) ko compatible format mein convert karti hai, taaki receiver correctly interpret kar sake.

## Presentation Layer Kaam Kaise Aata Hai (Flow)

```
Application Layer (data generate) 
   → Presentation Layer (format, compress, encrypt) 
      → Session Layer 
         → ...baaki layers
```

Receiving end pe ye process **reverse** hoti hai.

## Viva One-Liners

- **Q: Presentation Layer Application aur lower layers ke beech kya kaam karti hai?**
 A: Translator ka kaam — data ko aise format mein convert karti hai jo dono communicating systems samajh sakein.
- **Q: Presentation Layer kaunse 2 security-related services deti hai?**
 A: Encryption aur Decryption.
- **Q: Compression ka fayda kya hai?**
 A: Data size kam hoti hai, isse transmission fast hoti hai aur bandwidth save hoti hai.
