# Sliding Window Protocol — Selective Repeat (SR)

## Selective Repeat Kyun Zaroori Hai?

**Go-Back-N** protocol tab theek kaam karta hai jab errors kam hon — but agar link **noisy/unreliable** ho, to GBN bahut zyada bandwidth waste kar deta hai kyunki wo poora window retransmit karta hai, chahe sirf ek hi frame lost hua ho.

**Selective Repeat (SR)** is problem ko solve karta hai — ye sirf wahi frame retransmit karta hai jo **actually lost ya damaged** hua hai.

## Selective Repeat vs Go-Back-N

| Feature | Go-Back-N | Selective Repeat |
|---|---|---|
| Retransmission | Poora window (lost frame ke baad ke sab) | Sirf specific lost/damaged frame |
| Acknowledgment | Cumulative | **Independent** (har frame ka apna ACK) |
| Out-of-order packets | Discard kar deta hai | Accept karta hai (buffer mein rakhta hai, sort karta hai) |
| Efficiency | Kam (jab errors zyada hon) | Zyada (especially unreliable links pe) |
| Complexity | Simple | Complex (buffers dono taraf chahiye) |
| Requires | — | Full-duplex link |

## Kaise Kaam Karta Hai

- Sender aur Receiver dono ek **window** maintain karte hain (GBN ki tarah, but dono taraf)
- Receiver **out-of-order** packets bhi accept karta hai aur unhe buffer mein store karta hai
- Jab missing packet aa jaata hai, receiver window ko sort karke sequence complete karta hai
- Har frame ka **independent acknowledgment** hota hai — isliye receiver exactly bata sakta hai kaunsa frame miss hua

## Kab Use Hota Hai

Selective Repeat especially **unreliable/noisy links** pe better perform karta hai — kyunki jitni zyada retransmissions honi hain, utna hi zyada fayda hai sirf specific frames retransmit karne ka (poora window nahi).

## Piggybacking Connection

Selective Repeat mein **piggybacking** ka use hota hai — receiver acknowledgment ko delay karke apne agle outgoing data packet ke saath attach kar deta hai, isse control overhead kam hota hai.

*(Piggybacking ka detail alag note file mein hai.)*

## Viva One-Liners

- **Q: Selective Repeat, Go-Back-N se better kab hota hai?**
 A: Jab link noisy/unreliable ho — kyunki SR sirf lost frame retransmit karta hai, poora window nahi.
- **Q: Selective Repeat mein acknowledgment kaise kaam karta hai?**
 A: Independent acknowledgment — har frame ka apna alag ACK hota hai.
- **Q: Selective Repeat ko kya extra chahiye jo GBN ko nahi chahiye?**
 A: Buffers (dono sender aur receiver taraf) out-of-order packets store karne ke liye, aur full-duplex link.
