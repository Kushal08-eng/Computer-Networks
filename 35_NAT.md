# NAT (Network Address Translation)

## NAT Kya Hai?

**NAT** ek technique hai jo **private IP addresses** ko **public IP address** mein translate karta hai, taaki ek hi public IP se multiple devices internet access kar sakein.

> **Analogy**: Ek office building ka ek hi main reception (public IP) hota hai, lekin andar multiple employees (private IPs) kaam karte hain. Bahar se koi bhi letter reception pe aata hai, aur reception decide karta hai kis employee tak jaana hai.

## NAT Kyun Zaroori Hai?

- IPv4 addresses **limited** hain (~4.3 billion), lekin duniya mein usse zyada devices hain
- NAT se ek hi public IP se poora ghar/office ke saare devices internet use kar sakte hain

## NAT Kaise Kaam Karta Hai (Flow)

1. Ghar ke device (private IP, jaise 192.168.1.5) internet pe request bhejta hai
2. Router NAT karta hai — private IP ko apne public IP mein translate karta hai
3. Response wapas aane pe, router phir se translate karke sahi device tak deliver karta hai (ek table maintain karta hai kaunsa connection kis device ka tha)

## Types of NAT

| Type | Matlab |
|---|---|
| **Static NAT** | Ek private IP hamesha same public IP se map hota hai |
| **Dynamic NAT** | Private IPs ko available public IPs se pool mein se assign kiya jaata hai |
| **PAT (Port Address Translation)** | Sabse common — multiple private IPs ek hi public IP share karte hain, port numbers se differentiate hote hain |

## Advantages

| Fayda | Matlab |
|---|---|
| IP Address Saving | Limited public IPs efficiently use hote hain |
| Security | Private IPs directly internet pe expose nahi hote (extra protection layer) |

## Viva One-Liners

- **Q: NAT ka main purpose kya hai?**
 A: Private IP addresses ko public IP mein translate karna, taaki limited public IPs se multiple devices internet use kar sakein.
- **Q: Sabse common NAT type kaunsa hai?**
 A: PAT (Port Address Translation).
