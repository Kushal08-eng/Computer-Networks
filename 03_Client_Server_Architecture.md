# Client-Server Architecture

## Kya Hai?

Ek architecture jisme **Client** (request bhejne wala) aur **Server** (response dene wala) do alag roles hote hain.

- **Client**: User ka device jo request bhejta hai (browser, mobile app)
- **Server**: Powerful machine jo data/resources store karke rakhti hai aur request ka response deti hai

> **Analogy**: Tum Zomato app (client) se khana order karte ho, restaurant (server) khaana banake bhejta hai. Tum khud khaana nahi bana rahe — request bhej rahe ho aur response (khaana) mil raha hai.

## Request-Response Cycle

1. Client ek **request** banata hai (jaise "mujhe google.com ka homepage chahiye")
2. Request network se travel karke server tak pahunchti hai
3. Server request process karta hai
4. Server ek **response** wapas bhejta hai (webpage data)
5. Client us response ko display karta hai

## Advantages

| Fayda | Matlab |
|---|---|
| Centralized data | Sab data ek jagah manage hota hai, update karna easy |
| Security | Server pe access control lagana easy hai |
| Scalability | Server ko upgrade karke zyada clients handle kar sakte ho |

## Disadvantages

| Nuksaan | Matlab |
|---|---|
| Single point of failure | Server down ho gaya to sab clients affect honge |
| Cost | Powerful server maintain karna expensive hota hai |
| Traffic bottleneck | Bahut saare clients ek saath request karein to server slow ho sakta hai |

## Real Examples

- **Gmail** — tumhara browser (client) Google ke server se mail data leta hai
- **YouTube** — video content server pe store hota hai, client stream karta hai
- **Banking apps** — transactions server pe process hoti hain

## Viva One-Liners

- **Q: Client-Server architecture kya hai?**
 A: Ek model jisme client requests bhejta hai aur server unhe process karke response deta hai.
- **Q: Iska sabse bada disadvantage?**
 A: Server crash hone pe poora system affect ho sakta hai (single point of failure).
