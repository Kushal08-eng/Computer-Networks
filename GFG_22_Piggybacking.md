# Piggybacking in Computer Networks

## Piggybacking Kya Hai?

**Piggybacking** ek technique hai jisme receiver apna **acknowledgment (ACK)** turant nahi bhejta — balki thoda delay karke, use apne **next outgoing data packet** ke saath attach kar deta hai.

> **Analogy**: Jaise koi courier delivery boy ek building mein parcel deliver karne jaa raha ho, aur raaste mein tumhara bhi ek letter post box mein daal de — ek hi trip mein 2 kaam ho gaye, alag trip ki zaroorat nahi padi.

## Ye Kyun Use Hota Hai

| Fayda | Matlab |
|---|---|
| **Efficiency** | Alag ACK frame bhejne ki zaroorat nahi — control frames ki count kam ho jaati hai |
| **Bandwidth Saving** | Data aur ACK ek hi frame mein jaane se bandwidth save hoti hai |
| **Overhead Reduction** | Network pe overall overhead kam hota hai |

## Kaise Kaam Karta Hai

Ye 2 alag channels (ek sending ke liye, ek receiving ke liye) use karne ki jagah, **ek hi channel** use karta hai data aur ACK dono ke liye:

1. Agar host ke paas **data aur acknowledgment dono** ready hain → single frame mein dono bhej deta hai (Data + ACK)
2. Agar sirf **acknowledgment** ready hai → thoda wait karta hai dekhne ke liye data bhi ready hoti hai ya nahi; agar nahi to ACK akela bhej deta hai
3. Agar sirf **data** ready hai → last acknowledgment usme include kar deta hai

Sender frame header se identify karta hai ki frame mein data hai, ACK hai, ya dono.

## Piggybacking Ke Liye Requirement

- **Full-duplex transmission** zaroori hoti hai — jisse dono ends simultaneously data bhej aur receive kar sakein
- Simplex ya Half-Duplex modes mein piggybacking practical nahi hoti

## Sliding Window Protocols Ke Saath Connection

Sliding Window protocols (jaise Selective Repeat) mein sender multiple packets bina acknowledgment ka wait kiye bhej sakta hai — piggybacking is throughput ko aur bhi improve karti hai, kyunki alag ACK frames ki zaroorat kam ho jaati hai.

- Sender aur receiver dono **finite buffers** maintain karte hain outgoing/incoming packets ke liye
- Unacknowledged packets **timeout** ke baad retransmit hote hain

## Viva One-Liners

- **Q: Piggybacking kya hai?**
 A: Acknowledgment ko delay karke agle outgoing data packet ke saath attach karne ki technique.
- **Q: Piggybacking ke liye kaunsa transmission mode zaroori hai?**
 A: Full-duplex.
- **Q: Piggybacking ka main fayda kya hai?**
 A: Alag control frames (ACKs) ki zaroorat kam hoti hai, isse network efficiency badhti hai.
