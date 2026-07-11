# Stop and Wait ARQ

## Stop-and-Wait ARQ Kya Hai?

**Stop-and-Wait ARQ (Automatic Repeat Request)** ek reliable data transmission protocol hai jisme sender **ek time pe ek frame** bhejta hai aur next frame bhejne se pehle receiver se **acknowledgment (ACK)** ka wait karta hai.

> Isse Sliding Window Protocol ka hi ek special case maana jaata hai — jisme **window size = 1** hoti hai.

## Kaise Kaam Karta Hai

1. Sender ek data frame bhejta hai
2. Sender **timer** start karta hai aur ACK ka wait karta hai
3. Agar ACK time limit ke andar mil jaaye → sender next frame bhejta hai
4. Agar ACK nahi milta (timeout ho jaaye) → sender wahi frame **retransmit** karta hai

## Ye Kin Problems Ko Solve Karta Hai

Stop-and-Wait ARQ acknowledgments, sequence numbers, aur timeouts use karke ye problems handle karta hai:

| Problem | Solution |
|---|---|
| **Lost Data** | Timeout ke baad retransmission |
| **Lost Acknowledgment** | Timeout se automatically retransmission trigger hoti hai |
| **Delayed Frames** | Sequence numbers se duplicate frames identify karke discard kiya jaata hai |

## Key Characteristics

| Feature | Detail |
|---|---|
| **Connection Type** | Connection-oriented (logical connection pehle establish hoti hai) |
| **Error Control** | Acknowledgments aur retransmissions se |
| **Flow Control** | Ek time pe sirf 1 frame allow karke |
| **Sequence Numbers** | Sirf 2 (0 aur 1) — duplication avoid karne ke liye kaafi hai |
| **Throughput** | 1 data frame per Round Trip Time (RTT) |

## Limitations

- **Low channel utilization** — sender zyada time idle wait karte hue bitaata hai
- Jab **bandwidth-delay product** high ho (jaise high-speed ya long-distance links), performance bahut poor ho jaata hai
- Best suited hai **low propagation delay** wale networks ke liye, jaise LAN

> Isi wajah se advanced protocols jaise **Go-Back-N ARQ** aur **Selective Repeat ARQ** prefer kiye jaate hain — jo multiple frames ek saath bhej sakte hain (window size > 1).

## Viva One-Liners

- **Q: Stop-and-Wait ARQ mein window size kitni hoti hai?**
 A: 1 — sirf ek frame ek time pe bina acknowledgment ke bheja jaa sakta hai.
- **Q: Stop-and-Wait ARQ mein kitne sequence numbers use hote hain?**
 A: 2 (0 aur 1).
- **Q: Stop-and-Wait ARQ kis type ke network ke liye best suited hai?**
 A: Low propagation delay wale networks (jaise LAN).
- **Q: Ye kaunsi 2 cheezein simultaneously provide karta hai?**
 A: Error control (retransmission se) aur Flow control (ek time pe ek frame allow karke).
