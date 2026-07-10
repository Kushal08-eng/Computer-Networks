# Packets

## Packet Kya Hai?

**Packet** data ka wo chhota tukda hai jisme actual data ke saath extra information (header) bhi hoti hai jo batati hai ye packet kahan se aaya aur kahan jaana hai.

> **Analogy**: Jaise ek bada parcel ko chhote boxes mein todke bheja jaata hai, har box pe address label (header) lagi hoti hai — waise hi bada data packets mein todke bheja jaata hai.

## Packet Ka Structure

| Part | Matlab |
|---|---|
| **Header** | Metadata — source IP, destination IP, sequence number, protocol type |
| **Payload (Data)** | Actual content jo bheja jaa raha hai |
| **Trailer** (kabhi-kabhi) | Error-checking info (jaise CRC) |

## Packet Switching Kya Hai

Data ko poora ek saath nahi bheja jaata — chhote packets mein todke independently network se bheja jaata hai, jo destination pe reassemble hote hain.

## Packet Switching vs Circuit Switching

| Packet Switching | Circuit Switching |
|---|---|
| Data chhote packets mein todke bheja jaata hai | Ek dedicated path pehle se establish hota hai (jaise purane telephone) |
| Multiple users same network share kar sakte hain | Poora path sirf ek call/connection ke liye reserved hota hai |
| Internet isi pe based hai | Traditional telephone lines isi pe based thi |
| Efficient resource use | Resources waste ho sakte hain agar underused ho |

> **Analogy**: Packet Switching = courier company jo alag-alag packages ko shared trucks mein bhejti hai (efficient). Circuit Switching = ek private taxi jo sirf tumhare liye reserved hai poori trip ke liye (dedicated but costly).

## Viva One-Liners

- **Q: Packet ke 2 main parts kya hain?**
 A: Header aur Payload (data).
- **Q: Internet kaunsi switching technique use karta hai?**
 A: Packet Switching.
