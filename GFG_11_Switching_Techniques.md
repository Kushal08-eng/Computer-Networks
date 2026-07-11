# Switching Techniques

## Switching Kya Hai?

**Switching** wo technique hai jisse data packets ek device se dusre tak, ya ek network se dusre network tak transfer kiye jaate hain — dedicated devices (switches) ke through.

Switching ke 3 main types hain: **Circuit Switching**, **Packet Switching**, aur **Message Switching**.

---

## 1. Circuit Switching

**Connection-oriented** method — traditional telephone networks mein widely use hoti thi.

- Data transmission shuru hone se **pehle** sender-receiver ke beech ek **dedicated path** establish hota hai
- Ye connection poori communication session ke duration tak reserved rehta hai
- Dono ends ko **fixed bandwidth** aur **low latency** milti hai

| Advantages | Disadvantages |
|---|---|
| Guaranteed, constant data rate | Resources reserved hone se costly aur inefficient (especially high-traffic mein) |
| Bit delay constant rehta hai, bina delay ke data flow | Bandwidth waste ho sakti hai agar continuous connection na ho |

> **Real Example**: Traditional telephone system, dial-up internet connections.

## 2. Packet Switching

Data ko chhote **packets** mein todke bheja jaata hai — sabse zyada modern internet isi pe based hai.

### a) Connectionless (Datagram) Packet Switching
- Har packet **independently** treat hota hai, saara addressing/control info packet mein hi included hota hai
- Koi connection setup zaroori nahi — packets alag-alag paths le sakte hain, out of order bhi aa sakte hain
- Reliability higher-layer protocols (jaise TCP) handle karte hain

### b) Connection-Oriented (Virtual Circuit) Packet Switching
- Data transfer se pehle sender-receiver ke beech ek **logical path** establish hota hai
- Sab packets isi predefined route ko follow karte hain, sequence numbers milte hain (order maintain karne ke liye)
- Ek **Virtual Circuit ID** har connection ko identify karta hai
- **Protocols**: X.25, Frame-Relay, ATM, MPLS

> **Analogy**: Message ko chhote text messages ki series ki tarah bhejna — flexible aur efficient, especially chhote/burst data ke liye.

## 3. Message Switching

Sabse purani switching techniques mein se ek.

- Poora **message** ek intermediate node ko bheja jaata hai
- Message wahan temporarily **store** hota hai, phir next node ko forward hota hai (**store-and-forward**)
- Sender-receiver ke beech koi dedicated path establish nahi hota

| Characteristics | Detail |
|---|---|
| Real-time use | Suitable nahi (storing se delay hoti hai) |
| Storage | Har intermediate device ko large storage chahiye |
| Reliability | Direct connection na hone ki wajah se kam reliable |

> **Analogy**: Physical letter bhejna jo pehle post office (intermediate node) mein store hota hai, phir next branch tak jaata hai.

## Comparison Summary

| Feature | Circuit Switching | Packet Switching | Message Switching |
|---|---|---|---|
| Path | Dedicated, pre-established | No fixed path (packets independent ya virtual circuit) | No dedicated path |
| Best For | Continuous, real-time communication | Modern internet (bursty data) | Store-and-forward systems (legacy, email backend) |
| Efficiency | Kam (resources reserved) | High (shared resources) | Medium (storage overhead) |

## Viva One-Liners

- **Q: Switching ke 3 main types kaunse hain?**
 A: Circuit Switching, Packet Switching, aur Message Switching.
- **Q: Modern internet kaunsi switching technique use karta hai?**
 A: Packet Switching.
- **Q: Circuit switching mein connection kab establish hota hai?**
 A: Data transmission shuru hone se pehle hi, aur poori session tak reserved rehta hai.
- **Q: Virtual Circuit Packet Switching aur Datagram Packet Switching mein difference?**
 A: Virtual Circuit mein pehle se ek logical path set hota hai (sab packets same route follow karte hain), Datagram mein har packet independently apna path le sakta hai.
