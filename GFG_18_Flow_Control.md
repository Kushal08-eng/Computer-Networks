# Flow Control in Data Link Layer

## Flow Control Kya Hai?

**Flow Control** Data Link Layer ka mechanism hai jo sender-receiver ke beech **data transmission ki speed** control karta hai — ensure karta hai ki sender data usi rate se bheje jo receiver handle kar sake.

> **Analogy**: Agar tum fast bolte ho but dusra bandha slow samajhta hai, to tumhe apni speed thodi kam karni padegi taaki wo sun/samajh sake. Flow control network mein wahi kaam karta hai — fast sender ko slow receiver ke hisaab se adjust karta hai.

## Flow Control Kyun Zaroori Hai

- Sender fast rate se data bhej sakta hai, but receiver ka processing power ya traffic load kam ho sakta hai
- Bina flow control ke, receiver ka **buffer overflow** ho sakta hai aur data **loss** ho sakta hai
- Flow control 2 alag-alag speed pe kaam karne wale stations ko properly communicate karne deta hai

## Techniques of Flow Control

### 1. Stop-and-Wait Flow Control
Sabse simple technique.

- Data ko multiple frames mein todha jaata hai
- Sender ek frame bhejta hai, receiver **ready hone ka signal** deta hai
- Acknowledgment milne ke baad hi sender next frame bhejta hai
- Ye continue hota hai jab tak **EOT (End of Transmission)** frame na bhej diya jaaye

| Limitation | Matlab |
|---|---|
| Low Efficiency | Ek time pe sirf ek frame transit mein ho sakta hai |
| Propagation Delay Issue | Agar propagation delay transmission delay se bahut zyada ho, to productivity kam ho jaati hai |

### 2. Sliding Window Flow Control
Zyada efficient — sender multiple frames (window size tak) bina har ek ka wait kiye bhej sakta hai.

*(Detailed breakdown Go-Back-N aur Selective Repeat wali alag note files mein hai.)*

## Flow Control: Data Link Layer vs Network Layer

Flow control dono layers pe zaroori hota hai:

| Layer | Kyun Zaroori |
|---|---|
| **Data Link Layer** | Data loss prevent karta hai jab receiver overwhelmed ho jaaye (buffer full ho jaaye) |
| **Network Layer** | Poore network path ke across congestion aur synchronization manage karta hai |

## Viva One-Liners

- **Q: Flow control ka main purpose kya hai?**
 A: Sender ki transmission speed ko receiver ki processing capacity ke hisaab se control karna, taaki data loss na ho.
- **Q: Stop-and-Wait flow control ka main disadvantage kya hai?**
 A: Ek time pe sirf ek frame transit mein hota hai, jisse channel underutilized rehta hai.
- **Q: Flow control aur Error control mein basic difference?**
 A: Flow control speed/rate manage karta hai (overwhelm na ho), Error control data ki correctness ensure karta hai (errors detect/fix karta hai).
