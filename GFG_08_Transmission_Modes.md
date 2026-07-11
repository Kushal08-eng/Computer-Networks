# Transmission Modes

## Transmission Modes Kya Hain?

**Transmission Modes (Communication Modes)** batate hain do devices ke beech data kaise exchange hota hai — kya information ek direction mein move karti hai ya dono directions mein, aur kya devices same time pe transmit kar sakte hain.

| Function | Matlab |
|---|---|
| Communication Pattern | Communication ka pattern define karta hai |
| Sender/Receiver Roles | Kaun sender hai, kaun receiver, decide karta hai |
| Speed/Performance | Overall speed aur performance ko influence karta hai |
| Use | Networking aur telecommunication systems mein use hota hai |

---

## 1. Simplex Mode

Communication sirf **ek direction** mein hoti hai — sender se receiver tak, koi reverse data flow nahi.

- Ek device sirf **transmitter**, dusra sirf **receiver**
- Koi feedback ya acknowledgment support nahi hota

> **Example**: Keyboard aur traditional monitor — keyboard sirf input deta hai, monitor sirf output deta hai.

| Advantages | Disadvantages |
|---|---|
| Simple, easy implement karna | Receiver se koi error reporting nahi |
| Installation/maintenance cost kam | Interactive systems ke liye suitable nahi |
| Poora bandwidth sending ke liye use hota hai | Successful delivery confirm nahi ho sakti |
| Broadcast-type applications ke liye suitable | Modern two-way systems mein limited use |

## 2. Half-Duplex Mode

Communication **dono directions** mein ho sakti hai, but **ek time pe sirf ek device** transmit kar sakta hai — devices baari-baari (turns lekar) bhejte/receive karte hain.

- Bidirectional communication support karta hai
- Ek shared communication channel use hota hai
- Transmission devices ke beech alternately hoti hai

> **Example**: Walkie-talkie — message ek time pe ek hi jaata hai, but dono directions mein bheja jaa sakta hai.

| Advantages | Disadvantages |
|---|---|
| One-way se zyada flexible | Simultaneously send/receive nahi kar sakte |
| Full-duplex se cost-effective | Turn-based transmission ki wajah se delay ho sakta hai |
| Ek channel ka efficient use | Heavy traffic mein performance girti hai |
| Controlled communication environments ke liye suitable | Control mechanisms fail hon to collision risk |

## 3. Full-Duplex Mode

Communication **dono directions mein ek saath** hoti hai — dono connected devices simultaneously data transmit aur receive kar sakte hain, ek dusre ka wait kiye bina.

- Simultaneous two-way data exchange enable karta hai
- Separate channels ya divided bandwidth use hota hai
- Real-time communication systems mein common

> **Example**: Telephone Network — dono log ek saath baat kar sakte hain aur sun sakte hain.

| Advantages | Disadvantages |
|---|---|
| Faster data transfer rate | Installation cost high |
| Transmissions ke beech waiting time nahi | Complex hardware chahiye |
| Communication efficiency improve hoti hai | Bandwidth requirement zyada |
| Interactive applications ke liye suitable | System configuration complex hota hai |

---

## Quick Comparison

| Mode | Direction | Example |
|---|---|---|
| **Simplex** | Sirf ek direction | Keyboard → Monitor |
| **Half-Duplex** | Dono directions, ek time pe ek | Walkie-talkie |
| **Full-Duplex** | Dono directions simultaneously | Telephone call |

## Viva One-Liners

- **Q: Simplex mode ka real-life example?**
 A: Keyboard aur monitor — keyboard sirf bhejta hai, monitor sirf receive karta hai.
- **Q: Half-duplex aur full-duplex mein basic difference?**
 A: Half-duplex mein ek time pe ek hi taraf se data jaata hai; full-duplex mein dono taraf se simultaneously data ja sakta hai.
- **Q: Full-duplex ka main disadvantage kya hai?**
 A: Zyada bandwidth aur complex hardware chahiye, installation cost bhi high hoti hai.
