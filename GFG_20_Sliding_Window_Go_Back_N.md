# Sliding Window Protocol — Go-Back-N (GBN)

## Go-Back-N Kya Hai?

**Go-Back-N (GBN)** ek sliding window-based **ARQ (Automatic Repeat reQuest)** protocol hai, jisme sender **multiple frames** (window size tak) bina har frame ka acknowledgment wait kiye transmit kar sakta hai.

## Key Characteristics

| Feature | Detail |
|---|---|
| **Window Size (N)** | Sender window size Ws = N; jaise GBN-4 mein window size 4 hai |
| **N > 1** | Pipelining enable karne ke liye N hamesha 1 se zyada hona chahiye |
| **N = 1** | Is case mein GBN, Stop-and-Wait ARQ jaisa ban jaata hai |
| **Receiver Window Size** | Hamesha **1** hoti hai (GBN mein) |

## Kaise Kaam Karta Hai

1. Sender ek sliding window (size N) maintain karta hai
2. Bina individual ACKs ka wait kiye, N frames tak transmit kar sakta hai
3. Har transmitted frame ke saath ek timer associate hota hai
4. ACK receive hone pe, sender window forward slide karta hai — naye frames transmit karne ke liye

## Frame Loss Pe Kya Hota Hai

Agar koi frame **lost** ho jaaye, to sender us frame **aur uske baad ke saare frames** retransmit karta hai — chahe wo successfully receive hue hon.

> **Example**: Agar frames 1 se 5 bheje gaye aur frame 3 lost ho gaya, to sender frames **3, 4, aur 5** retransmit karega (chahe 4 aur 5 receiver ko already mil chuke hon).

## Efficiency Formula

Agar processing delay, queuing delay, aur ACK transmission delay ignore kiya jaaye:

```
Efficiency = N / (1 + 2a)
```

Jahan **a** = propagation delay / transmission delay ka ratio.

## Window Size Aur Sequence Numbers Ka Relation

- Window size batata hai sender bina acknowledgment ke kitne packets bhej sakta hai
- Sequence numbers packets ko label karte hain taaki receiver order maintain kar sake aur missing packets identify kar sake
- Window size **available sequence number range se chhota ya barabar** hona chahiye — warna receiver confuse ho sakta hai (duplicate vs naya packet)

## Viva One-Liners

- **Q: GBN mein receiver window size kitni hoti hai?**
 A: Hamesha 1.
- **Q: Frame lost hone par GBN kya karta hai?**
 A: Lost frame aur uske baad ke sab frames retransmit karta hai, chahe wo successfully receive hue hon.
- **Q: GBN kab Stop-and-Wait jaisa ban jaata hai?**
 A: Jab window size N = 1 ho.
- **Q: GBN ki efficiency formula kya hai?**
 A: N / (1 + 2a), jahan a = propagation delay / transmission delay.
