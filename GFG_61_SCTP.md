# Stream Control Transmission Protocol (SCTP)

## SCTP Kya Hai?

**SCTP (Stream Control Transmission Protocol)** ek **connection-oriented, reliable, aur message-oriented** transport layer protocol hai — TCP aur UDP dono ki achi features combine karta hai.

## SCTP Ki Key Features

| Feature | Matlab |
|---|---|
| **Message-Oriented** | TCP ke byte-stream approach ke ulta — messages ke boundaries preserve hote hain |
| **Multi-Streaming** | Ek connection ke andar multiple independent streams simultaneously bhej sakta hai |
| **Multi-Homing** | Ek endpoint multiple IP addresses use kar sakta hai — fault tolerance ke liye |
| **Full-Duplex** | Send aur receive dono simultaneously ho sakte hain |
| **Flow & Congestion Control** | TCP jaisa hi |

## Multi-Homing Kaise Kaam Karta Hai

- Host multiple IP addresses ke through connect ho sakta hai
- Agar primary path fail ho jaaye, data automatically **alternate path** pe switch ho jaata hai
- Har path ka Round Trip Time (RTT) monitor hota hai reliability ke liye

## SCTP Packet Structure

| Part | Matlab |
|---|---|
| **Common Header** | Fixed 12 bytes — source/destination ports, verification tag (32-bit random value, purani connection se differentiate karta hai), checksum (CRC32) |
| **Payload (Chunks)** | Variable — actual data chunks |

## SCTP Ke Security Features

SCTP kuch security threats se resistant hai:
- **Blind DoS attacks**
- **Masquerading**
- Service monopolization

## SCTP Ke Use Cases

| Use Case | Kyun SCTP |
|---|---|
| Telephony Signaling (SS7) | Multi-streaming aur reliability dono chahiye |
| VoIP | Multi-homing se better fault tolerance |

## SCTP vs TCP vs UDP

| Feature | TCP | UDP | SCTP |
|---|---|---|---|
| Reliability | Haan | Nahi | Haan |
| Ordering | Byte-stream order | Nahi | Per-stream order |
| Multi-homing | Nahi | Nahi | Haan |
| Multi-streaming | Nahi (single stream) | N/A | Haan |
| Data Type | Byte-stream | Datagram | Message |

## Viva One-Liners

- **Q: SCTP ki 2 unique features kya hain jo TCP/UDP mein nahi hain?**
 A: Multi-streaming aur Multi-homing.
- **Q: SCTP message-oriented kyun hai?**
 A: Kyunki ye TCP ki tarah continuous byte stream nahi bhejta — individual message boundaries preserve karta hai.
- **Q: Multi-homing ka fayda kya hai?**
 A: Agar primary network path fail ho jaaye, to data automatically alternate path pe switch ho jaata hai — better fault tolerance.
