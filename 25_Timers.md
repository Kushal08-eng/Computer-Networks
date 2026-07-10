# Timers (TCP)

## Timers Kyun Zaroori Hain?

TCP reliable delivery ensure karta hai — iske liye wo **timers** use karta hai jo track karte hain kab retransmit karna hai, connection band karna hai, ya connection alive hai ya nahi.

> **Analogy**: Jaise tum kisi ko important message bhejte ho aur agar kuch time tak reply nahi aata, tum dobara bhej dete ho — TCP bhi wahi karta hai timers ki madad se.

## Main TCP Timers

| Timer | Kaam |
|---|---|
| **Retransmission Timer (RTO)** | Agar acknowledgment time pe nahi aaya, to data dobara bhej deta hai |
| **Persist Timer** | Jab receiver ka buffer full ho (window size 0), ye periodically check karta rehta hai ki receiver ready hua ya nahi |
| **Keep-Alive Timer** | Idle connection ko check karta hai ki dusra device abhi bhi active hai ya nahi |
| **Time-Wait Timer** | Connection close hone ke baad thodi der wait karta hai taaki delayed packets properly handle ho sakein |

## RTO (Retransmission Timeout) Kaise Decide Hota Hai

- TCP dynamically calculate karta hai based on **RTT (Round Trip Time)** — jitni der mein packet jaake acknowledgment wapas aata hai
- Network slow hai to RTO bada hoga, fast hai to chhota

## Viva One-Liners

- **Q: Retransmission timer ka kaam kya hai?**
 A: Agar acknowledgment time pe na aaye to data dobara bhejna.
- **Q: Keep-alive timer kyun use hota hai?**
 A: Idle connection mein check karne ke liye ki dusra device active hai ya nahi.
