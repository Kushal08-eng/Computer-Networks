# Error Detection in Computer Networks

## Error Detection Kya Hai?

Transmission ke dauran data corrupt ho sakta hai (noise, interference ki wajah se) — **Error Detection** techniques ye check karti hain ki received data original transmitted data se match karta hai ya nahi.

## Main Error Detection Techniques

### 1. Parity Check
- Data ke bits mein ek extra **parity bit** add ki jaati hai taaki total 1's ki count even (ya odd) rahe
- Simple but limited — sirf odd number of bit errors detect kar sakta hai

### 2. Checksum
Networking protocols (IP, TCP, UDP) mein widely use hota hai.

- Data ko fixed-size blocks mein todke unka **sum** nikala jaata hai (1's complement method se)
- Ye checksum data ke saath bheja jaata hai
- Receiver wahi calculation apni taraf se karta hai — match nahi hua to error

| Advantages | Disadvantages |
|---|---|
| Fast to compute, easy implement karna | Kuch error patterns miss ho sakte hain (jaise errors jo cancel out ho jaayein) |
| Real-time applications ke liye ideal (network transfers) | CRC ke muqable kam reliable |
| Minimal computing resources | Error correction nahi kar sakta, sirf detection |

### 3. LRC (Longitudinal Redundancy Check)
2-D parity check bhi kehte hain — data ko rows/columns ke table mein organize karke, poori table ke liye ek redundant bit add hoti hai. Single-bit aur burst errors detect kar sakta hai, but same vertical slice ke 2-bit errors miss ho sakte hain.

### 4. CRC (Cyclic Redundancy Check)
Checksum se zyada reliable technique.

- Checksum addition use karta hai, CRC **binary division** use karta hai — redundant bits add ki jaati hain taaki data ek predefined **generator polynomial** se exactly divisible ban jaaye
- Receiver same polynomial se data divide karta hai — **zero remainder** = data accepted, **non-zero remainder** = transmission error
- Single-bit, multiple-bit, aur **burst errors** detect karne mein highly effective
- **Widely used**: Ethernet, HDLC, USB

## Comparison

| Method | Detection Capability | Speed | Complexity |
|---|---|---|---|
| Parity Bit | Low (sirf odd errors) | Fastest | Simplest |
| Checksum | Medium | Fast | Simple |
| CRC | Highest (burst errors bhi) | Thoda slow (division) | Complex |

## Viva One-Liners

- **Q: CRC checksum se zyada reliable kyun hai?**
 A: Kyunki CRC binary polynomial division use karta hai jo burst errors bhi effectively detect kar leta hai, checksum sirf simple addition use karta hai.
- **Q: Checksum kaunse layer/protocols mein use hota hai?**
 A: IP, TCP, UDP jaise networking protocols mein.
- **Q: CRC mein error kaise detect hota hai?**
 A: Agar received data ko generator polynomial se divide karne pe remainder zero nahi aata, to error detect hota hai.
