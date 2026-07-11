# Reliable User Datagram Protocol (RUDP)

## RUDP Kya Hai?

**RUDP (Reliable User Datagram Protocol)** ek protocol hai jo **UDP ke upar** build hota hai — acknowledgments, retransmissions, aur ordered delivery jaisi reliability features add karta hai, UDP ki low-latency benefits maintain karte hue.

> **Analogy**: "UDP + Reliability Layer" — TCP ke heavy connection setup ke bina, but UDP se zyada dependable.

## Trade-off Jo RUDP Solve Karta Hai

| Protocol | Speed | Reliability |
|---|---|---|
| **UDP** | Fast | Unreliable |
| **TCP** | Slower (connection overhead) | Reliable |
| **RUDP** | Fast (UDP jaisa) | Reliable (extra layer se) |

## RUDP Kaise Kaam Karta Hai

1. Packets **RUDP protocol ke through UDP pe** bheje jaate hain
2. Receiver errors aur order check karta hai
3. Receiver **ACKs (acknowledgments)** bhejta hai aur packets ko buffer mein rakhta hai jab tak sab correctly receive na ho jaayein
4. Agar ACK **timeout** ke andar nahi aata, sender wo packet **retransmit** karta hai

## Key Design Elements

| Element | Kaam |
|---|---|
| **Synchronized Shared Buffers** | Sender-receiver dono use karte hain, semaphores se protect kiye jaate hain — multiple threads ke access se corruption/deadlock avoid karne ke liye |
| **In-Flight Packet Tracking** | Efficiently track karta hai kaunse packets abhi transit mein hain |

## RUDP Kahan Use Hota Hai

| Use Case | Kyun RUDP |
|---|---|
| High-speed real-time applications | Gaming, streaming, VoIP — jahan TCP ka connection overhead affordable nahi, but reliability bhi chahiye |
| Signaling backhaul (Cisco) | SS7 MTP3, ISDN PRI backhaul mein use hota hai |

## Viva One-Liners

- **Q: RUDP kis protocol ke upar build hota hai?**
 A: UDP ke upar.
- **Q: RUDP TCP se kaise different hai reliability approach mein?**
 A: RUDP UDP ki speed maintain karte hue reliability add karta hai, TCP ke heavy connection setup ke bina.
- **Q: RUDP ka main use case kya hai?**
 A: High-speed real-time applications jaise gaming, streaming, VoIP — jahan speed aur reliability dono chahiye.
