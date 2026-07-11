# Services and Segment Structure in TCP

## TCP Ki Services (Recap)

TCP ye services provide karta hai: process-to-process communication, stream-oriented data transfer, full-duplex service, connection-oriented service, reliability, aur multiplexing.

*(Detail "TCP Protocol" wali note file mein hai.)*

## TCP Segment Ka Structure

TCP segment ka header **20 se 60 bytes** tak hota hai (20 bytes default, options ke saath 60 tak).

| Field | Size | Kaam |
|---|---|---|
| **Source Port** | 16 bits | Sending application identify karta hai |
| **Destination Port** | 16 bits | Receiving application identify karta hai |
| **Sequence Number** | 32 bits | Segment ke pehle byte ka position — reassembly ke liye |
| **Acknowledgement Number** | 32 bits | Receiver ka next expected byte number |
| **Header Length (HLEN)** | 4 bits | Header ki length (32-bit words mein) — 5 (min) se 15 (max) |
| **Control Flags** | 6 bits (1 bit each) | Connection setup/termination/abort, flow control control karte hain |
| **Window Size** | 16 bits | Flow control ke liye — receiver kitna data accept kar sakta hai |
| **Checksum** | 16 bits | Error control ke liye — TCP mein mandatory hai |
| **Urgent Pointer** | 16 bits | URG flag set ho to, urgent data ka location batata hai |
| **Options** | Variable | Extra features (jaise MSS, window scaling) |

## Control Flags Detail

| Flag | Full Form | Kaam |
|---|---|---|
| **SYN** | Synchronize | Connection start karna |
| **ACK** | Acknowledge | Data receive hone ka confirmation |
| **FIN** | Finish | Connection close karna (graceful) |
| **RST** | Reset | Connection abruptly close karna |
| **PSH** | Push | Data turant application ko deliver karna, buffer fill hone ka wait na karna |
| **URG** | Urgent | Segment mein urgent data hai, priority se process karna |

## Sequence Number Ka Example

> Agar sender ke pehle byte ka sequence number **50000** hai, aur segment mein **500 bytes** data hai, to agla segment sequence number **50501** (50000+500+1) se start hoga.

## Viva One-Liners

- **Q: TCP header ki minimum aur maximum size kya hai?**
 A: Minimum 20 bytes, maximum 60 bytes (options ke saath).
- **Q: Acknowledgement number kya represent karta hai?**
 A: Receiver ka next expected byte number.
- **Q: PSH flag ka kaam kya hai?**
 A: Data ko turant application tak deliver karna, bina segment fill hone ka wait kiye.
