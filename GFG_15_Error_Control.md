# Error Control in Data Link Layer

## Error Control Kya Hai?

**Error Control** Data Link Layer ka mechanism hai jo transmission ke dauran **damaged ya lost frames** detect karta hai aur unhe retransmit karke data integrity maintain karta hai.

> Error correction techniques generally complex, costly, aur resource-intensive hoti hain — isliye selectively use hoti hain (mostly error detection + retransmission approach zyada common hai).

## Error Control Ke Techniques (ARQ Protocols)

### 1. Stop-and-Wait ARQ
- Sender ek time pe **ek** data frame bhejta hai aur receiver se **ACK** (Acknowledgment) ka wait karta hai
- Agar time limit ke andar ACK nahi milta, sender frame **retransmit** karta hai
- ACK milne ke baad hi sender next frame bhejta hai

### 2. Sliding Window ARQ
Continuous data transmission ke liye use hota hai — sender multiple frames bina har ek ke liye wait kiye bhej sakta hai, isse channel utilization aur efficiency improve hoti hai. Ye 2 types mein divide hota hai:

| Type | Retransmission Strategy |
|---|---|
| **Go-Back-N ARQ** | Frame lost/corrupt ho to, uss frame **aur us ke baad ke sab frames** retransmit hote hain |
| **Selective Repeat ARQ** | Sirf wo specific frame retransmit hota hai jo lost/damaged hua — zyada efficient |

*(In dono protocols ka detailed breakdown alag note files mein hai.)*

## Comparison

| Feature | Stop-and-Wait | Go-Back-N | Selective Repeat |
|---|---|---|---|
| Frames sent at once | 1 | N (window size) | N (window size) |
| Retransmission on loss | Sirf wahi frame | Poora window (from lost frame onwards) | Sirf lost/damaged frame |
| Efficiency | Sabse kam | Medium | Sabse zyada |
| Complexity | Simple | Medium | Complex (buffer chahiye) |

## Viva One-Liners

- **Q: Error control ka main goal kya hai?**
 A: Damaged/lost frames detect karke retransmit karna, taaki data integrity maintain rahe.
- **Q: Go-Back-N aur Selective Repeat mein main difference?**
 A: Go-Back-N poora window retransmit karta hai frame loss pe; Selective Repeat sirf specific lost frame retransmit karta hai.
- **Q: Stop-and-Wait ARQ ka main limitation kya hai?**
 A: Ek time pe sirf ek hi frame bhej sakte hain, jisse channel underutilized rehta hai.
