# Error Correction in Computer Networks

## Error Correction Kya Hai?

Error Detection sirf bata sakta hai ki error hua hai ya nahi — **Error Correction** techniques actually error ko **fix** bhi kar sakti hain, bina retransmission ke.

## Hamming Code

Sabse popular error-correcting code — single-bit errors detect **aur correct** kar sakta hai.

### Kaise Kaam Karta Hai

- Data mein specific positions pe **parity bits** (redundant bits) add kiye jaate hain
- Har parity bit apne assigned positions ke bits ka parity check karta hai
- Receiver in parity checks se ek binary number nikalta hai jo **exact error position** batata hai
- Us position ka bit **flip** karke error correct kar diya jaata hai

> **Example**: Agar parity checks se number "0110" (decimal 6) milta hai, to matlab **6th bit** mein error hai — us bit ko flip karke fix kar diya jaata hai.

### Key Points

| Point | Detail |
|---|---|
| Detects | Single-bit errors (aur double-bit errors detect kar sakta hai, correct nahi) |
| Corrects | Sirf single-bit errors |
| Use Case | ECC memory (RAM), satellite communication — jahan retransmission costly/impractical ho |

## Parity Bit (Basic)

Ek bit jo data mein add hota hai taaki total 1's ki count even ya odd ho jaaye — detection ke liye use hota hai, correction ke liye nahi (jab tak Hamming jaisa multi-parity approach na use ho).

## CRC vs Hamming Code

| Feature | CRC | Hamming Code |
|---|---|---|
| Kaam | Sirf **detection** (burst errors bhi) | **Detection + Correction** (single-bit) |
| Use Case | Ethernet, storage, downloads | ECC memory, satellite communication |
| Overhead | Kam | Zyada (multiple parity bits chahiye) |
| Multi-bit errors | Detect kar sakta hai | Correction sirf single-bit tak limited |

## Comparison Table (Parity vs CRC vs Hamming)

| Method | Detects | Corrects | Use |
|---|---|---|---|
| Parity Bit | Basic single-bit | Nahi | RAM, simple transmission |
| CRC | Burst errors, multi-bit | Nahi | Ethernet, downloads, storage |
| Hamming Code | Single + double-bit (detect) | Single-bit | ECC memory, satellite |

## Viva One-Liners

- **Q: Hamming Code kya kar sakta hai jo CRC nahi kar sakta?**
 A: Hamming Code errors ko actually correct kar sakta hai (flip karke), CRC sirf detect karta hai.
- **Q: Hamming code kitne bit errors correct kar sakta hai?**
 A: Single-bit errors.
- **Q: Hamming code kahan use hota hai jahan retransmission impractical hai?**
 A: ECC memory (RAM) aur satellite communication mein.
