# TCP Connection Establishment

## TCP Connection Establishment Kya Hai?

Ye process hai jisse client aur server, data transfer se pehle, ek reliable connection **3-way handshake** ke through establish karte hain — parameters (window size, MSS) bhi is process mein negotiate hote hain.

## Key Parameters Exchange Hote Hain

| Parameter | Kaam |
|---|---|
| **SYN Flag** | Sender ko sequence number synchronize karne ka request |
| **MSS (Maximum Segment Size)** | Receiver apna max segment size bataata hai — fragmentation avoid karne ke liye |
| **Window Size** | Receiver apni buffer capacity bataata hai — sender ko batata hai kitna data bhej sakta hai bina wait kiye |
| **Acknowledgement Number** | Next expected sequence number |

> Agar sender aur receiver ke MSS values alag hon, to dono **minimum MSS** pe agree karte hain — fragmentation avoid karne ke liye.

## Example Calculation

Agar Window Size = 10000 bytes aur MSS = 500 bytes, to:

```
Sender ki sending window size = 10000 / 500 = 20 packets
```

## 3 Steps (Recap)

| Step | Flags | Matlab |
|---|---|---|
| 1 | SYN=1 | Client connection request karta hai, apna sequence number bhejta hai |
| 2 | SYN=1, ACK=1 | Server acknowledge karta hai, apna sequence number bhejta hai |
| 3 | ACK=1 | Client confirm karta hai — connection establish |

## Common Problems

| Problem | Matlab |
|---|---|
| **SYN Flood Attacks** | Hackers bahut saare SYN requests bhejte hain bina complete kiye, server overload ho jaata hai |
| **Connection Timeout** | Device time pe respond nahi karta, attempt fail ho jaata hai |

## Viva One-Liners

- **Q: Connection establishment ke dauran kaunse 2 important parameters exchange hote hain?**
 A: MSS (Maximum Segment Size) aur Window Size.
- **Q: Sender aur receiver ka MSS alag ho to kya hota hai?**
 A: Dono minimum MSS value pe agree karte hain, fragmentation avoid karne ke liye.
- **Q: 3-way handshake ko is naam se kyun jaana jaata hai?**
 A: Kyunki connection establish karne ke liye 3 packets (SYN, SYN+ACK, ACK) exchange hoti hain.
