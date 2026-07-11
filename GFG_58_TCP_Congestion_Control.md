# Congestion Control in TCP

## Congestion Control Kya Hai?

**TCP Congestion Control** ek mechanism hai jo network mein data flow manage karta hai — congestion (jab intermediate devices ke buffers fill ho jaate hain) hone se rokta hai.

> Sender ko directly pata nahi hota network ke intermediate devices ke buffers full hain ya nahi — isliye TCP khud **estimate** karta hai, ek variable **congestion window (cwnd)** use karke.

## Congestion Window (cwnd) Kya Hai?

- cwnd batata hai sender **bina acknowledgment ka wait kiye** kitna data bhej sakta hai
- Agar cwnd = 15 packets, to sender 16th packet nahi bhej sakta jab tak ACK na mile

## TCP Congestion Control Ke Phases

| Phase | Kya Hota Hai |
|---|---|
| **1. Slow Start** | cwnd **exponentially** badhta hai (1→2→4→8...) har successful RTT ke saath, jab tak ek threshold (**ssthresh**) tak na pahunch jaaye |
| **2. Congestion Avoidance** | Threshold pahunchne ke baad, cwnd **linearly** (by 1) badhta hai har RTT mein — zyada cautious approach |
| **3. Congestion Detection** | Jab loss detect ho, sender wapas Slow Start ya Congestion Avoidance mein jaata hai |

## Congestion Detect Hone Pe Kya Hota Hai

| Scenario | Response |
|---|---|
| **Timeout se Retransmission** | Congestion ki possibility high hai — ssthresh = cwnd/2, cwnd = 1, wapas Slow Start se shuru |
| **3 Duplicate ACKs se Retransmission** | Congestion ki possibility kam hai — ssthresh = cwnd/2, cwnd = ssthresh, Congestion Avoidance se shuru (Fast Recovery) |

## Slow Start Restart Algorithm

Jab TCP connection **idle** rehta hai (RTO jitni der), sender apna cwnd estimate invalidate kar deta hai (kyunki update nahi ho raha) — jab dobara data bhejna shuru hota hai, **Slow Start dobara se** restart hota hai, cwnd ko fresh estimate karne ke liye.

## Congestion Control Ke Fayde

| Fayda | Matlab |
|---|---|
| Packet Loss Kam | Network overload hone se rokta hai |
| Fair Bandwidth Usage | Sabhi flows ko fairly bandwidth milta hai |
| Network Stability | Congestion collapse (poore network ka slow ho jaana) avoid karta hai |

## Viva One-Liners

- **Q: Congestion window (cwnd) kya hai?**
 A: Ek variable jo batata hai sender bina acknowledgment ka wait kiye kitna data bhej sakta hai.
- **Q: Slow Start phase mein cwnd kaise badhta hai?**
 A: Exponentially — har successful RTT mein double hota hai.
- **Q: Timeout se retransmission aur 3 duplicate ACKs se retransmission mein response kaise differ karta hai?**
 A: Timeout pe cwnd = 1 (wapas Slow Start), Duplicate ACKs pe cwnd = ssthresh (Congestion Avoidance/Fast Recovery) — kyunki timeout zyada severe congestion signal hai.
