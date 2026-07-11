# Datagram Congestion Control Protocol (DCCP)

## DCCP Kya Hai?

**DCCP (Datagram Congestion Control Protocol)** ek **message-based transport layer protocol** hai jo un applications ke liye congestion control provide karta hai jo reliable delivery nahi chahti (UDP jaisi applications ke liye).

## DCCP Kyun Banaya Gaya

Network congestion (routers/buffers overload hone) se packets delay ya loss ho sakte hain. UDP khud congestion control nahi karta — DCCP is gap ko fill karta hai, **bina TCP jaisi full reliability ke overhead ke**.

## DCCP Ki Key Features

| Feature | Matlab |
|---|---|
| **Message-Based** | UDP jaisa — byte-stream nahi (TCP ki tarah) |
| **Congestion Control** | Built-in — network overload prevent karta hai |
| **ECN Support** | Explicit Congestion Notification — congestion signal detect karta hai |
| **Secure Handshake** | Connection setup/closure ke liye |
| **Multiple Congestion Control Mechanisms** | Flexible, TCP-friendly options available |
| **No Reliable/In-Order Delivery** | TCP jaisa guarantee nahi deta |

## DCCP vs SCTP

DCCP mein **SCTP jaisi sequential delivery of multiple streams** nahi hoti — DCCP simpler hai, sirf congestion control pe focus karta hai.

## DCCP Kab Use Hota Hai

| Application | Kyun DCCP |
|---|---|
| **Online Multiplayer Gaming** | Fast delivery zaroori, purane messages jaldi expire ho jaate hain |
| **Internet Telephony** | Real-time data, delay se zyada important hai fresh data |
| **Streaming Media (Audio/Video)** | Low-latency delivery, congestion-aware |

> Purane messages ki koi zaroorat nahi hoti in applications mein — isliye retransmission (jo purana data dobara bhejta hai) waste of time/resources hai. DCCP naye messages ko priority deta hai.

## Viva One-Liners

- **Q: DCCP ka main purpose kya hai?**
 A: Un applications ko congestion control dena jo UDP jaisi hain (reliable delivery nahi chahtin).
- **Q: DCCP aur SCTP mein main difference?**
 A: DCCP mein sequential multi-stream delivery nahi hoti (SCTP mein hoti hai).
- **Q: DCCP kis type ki applications ke liye best hai?**
 A: Time-sensitive applications — gaming, VoIP, streaming, jahan purane messages jaldi useless ho jaate hain.
