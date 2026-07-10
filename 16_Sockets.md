# Sockets

## Socket Kya Hai?

**Socket** ek endpoint hai jo network communication ke liye use hota hai — ye **IP address + Port number** ka combination hota hai.

> **Analogy**: IP address = building ka address, Port = flat number, Socket = poora address jisse exactly pata chale kaunse building ke kaunse flat mein delivery karni hai.

## Socket Ka Format

```
IP Address : Port Number
Example: 192.168.1.5:443
```

## Socket Kyun Zaroori Hai

- Ek hi device pe multiple applications ek saath network use kar sakte hain (browser, email client, game — sab alag ports pe)
- Socket exactly identify karta hai **kaunsa process** kis machine pe data bhej/receive kar raha hai

## Types of Sockets

| Type | Based On | Use |
|---|---|---|
| **TCP Socket (Stream Socket)** | TCP protocol | Reliable, connection-oriented communication |
| **UDP Socket (Datagram Socket)** | UDP protocol | Fast, connectionless communication |

## Socket Kaise Kaam Karta Hai (Simple Flow)

1. Server ek socket create karta hai aur ek port pe "listen" karta hai
2. Client bhi ek socket create karta hai aur server ke socket se connect karta hai
3. Dono ke beech data socket ke through exchange hota hai

## Viva One-Liners

- **Q: Socket kise kehte hain?**
 A: IP address aur Port number ka combination jo ek network endpoint identify karta hai.
- **Q: TCP socket aur UDP socket mein difference?**
 A: TCP socket reliable/connection-oriented hota hai, UDP socket fast but connectionless.
