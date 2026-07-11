# TCP Protocol (Transmission Control Protocol)

## TCP Kya Hai?

**TCP (Transmission Control Protocol)** internet ka sabse widely used transport-layer protocol hai — **reliable, ordered, aur error-checked** data delivery deta hai devices ke beech.

## TCP Ke 6 Key Characteristics

| Characteristic | Matlab |
|---|---|
| **1. Process-to-Process Communication** | 16-bit port numbers use karke sending/receiving processes identify karta hai |
| **2. Stream-Oriented** | Data ko continuous **byte stream** ki tarah bhejta hai, segments mein group karke |
| **3. Full-Duplex Service** | Dono directions mein ek saath communication ho sakta hai |
| **4. Connection-Oriented** | Data bhejne se pehle connection establish hoti hai (3 phases: setup, transfer, termination) |
| **5. Reliability** | Checksums, retransmissions, acknowledgements, sequencing, congestion control se ensure hoti hai |
| **6. Multiplexing** | Sender-receiver dono ends pe multiplexing/demultiplexing karta hai — multiple logical connections ek physical connection pe |

## TCP Kaise Kaam Karta Hai (High-Level Flow)

1. Application data bhejta hai (jaise email, file)
2. TCP data ko chhote chunks — **segments** mein todta hai
3. Har segment mein header hota hai — sequence numbers, ports, flags
4. Segments ko **IP** ko de diya jaata hai delivery ke liye — TCP path ki chinta nahi karta, sirf IP karta hai
5. Segments alag-alag paths se ja sakte hain, out-of-order aa sakte hain
6. Receiver pe TCP **sequence numbers** use karke segments ko sahi order mein reassemble karta hai

## TCP Ki Reliability Mechanisms

| Mechanism | Kaam |
|---|---|
| **Acknowledgements & Sequence Numbers** | Data accurate order mein deliver hota hai, ye ensure karta hai |
| **Checksums** | Errors detect karta hai; corrupted/lost packets retransmit hote hain |
| **Flow Control** | Sliding window mechanism se receiver overwhelm nahi hota |
| **Congestion Control** | Network traffic ke hisaab se sending rate adjust karta hai |

## TCP Ke Real-World Use Cases

| Use Case | Kyun TCP |
|---|---|
| **Web Browsing (HTTPS)** | Packets sahi order mein aane chahiye, page sahi se load ho |
| **Email** | Poora message accurately pahunchna chahiye |
| **File Transfer** | Har byte accurate hona chahiye |

## Viva One-Liners

- **Q: TCP process-to-process communication kaise karta hai?**
 A: 16-bit port numbers use karke.
- **Q: TCP ka data unit kya hai?**
 A: Segment (byte stream se banaya jaata hai).
- **Q: TCP reliability kin mechanisms se aati hai?**
 A: Checksums, retransmissions, acknowledgements, sequencing, aur congestion control se.
