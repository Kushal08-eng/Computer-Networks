# TCP vs UDP Protocol

## Basic Difference

| Feature | TCP | UDP |
|---|---|---|
| **Connection Type** | Connection-oriented | Connectionless |
| **Reliability** | Reliable (acknowledgments, retransmission) | Unreliable (best-effort) |
| **Ordering** | Guaranteed order | No ordering guarantee |
| **Speed** | Slower (overhead ki wajah se) | Faster |
| **Header Size** | 20-60 bytes (variable) | 8 bytes (fixed) |
| **Error Checking** | Mandatory checksum + retransmission | Optional checksum, no retransmission |
| **Flow/Congestion Control** | Haan | Nahi |
| **Use Case** | Web, email, file transfer | Streaming, gaming, VoIP, DNS |

## TCP — Jab Accuracy Important Ho

- Web browsing, file downloads, emails jaise applications ke liye best hai jahan **poora, sahi data** pahunchna zaroori hai
- Connection establish karta hai transfer se pehle
- Data missing ho to page load nahi hota properly — TCP isse rokta hai

## UDP — Jab Speed Important Ho

- Live video streaming, online gaming, VoIP calls jaise applications ke liye — jahan **delay se badhtar hai thoda data loss**
- Koi connection setup nahi, seedha data bhej deta hai
- Broadcast aur Multicast applications ke liye suitable (ek message multiple recipients ko)

## Practical Difference Table

| Aspect | TCP | UDP |
|---|---|---|
| Data Transfer | Sequence mein, guaranteed | Koi guarantee nahi |
| OS Dependency | Independent nahi | Independent |
| Routing Protocol Support | Zyada support karta hai | Kam |
| Speed Adjustment | Receiver ki speed ke hisaab se adjust hota hai | Nahi |
| Multicast/Broadcast | Nahi | Haan |
| MTU (typical) | 65495 bytes (theoretical) | 1500 bytes (Fast Ethernet) |

## Real-Life Examples

| TCP Uses | UDP Uses |
|---|---|
| Netflix/YouTube (streaming setup, buffering control) | Live sports streaming (real-time, kam latency) |
| Email (SMTP) | Online multiplayer games |
| Website loading (HTTPS) | DNS lookups |
| File transfer (FTP) | Video conferencing |

## Viva One-Liners

- **Q: TCP aur UDP mein sabse basic difference kya hai?**
 A: TCP reliable, connection-oriented hai; UDP fast, connectionless aur unreliable hai.
- **Q: UDP header, TCP se kitna chhota hai?**
 A: UDP header fixed 8 bytes hai, TCP 20-60 bytes (variable).
- **Q: Multicast/Broadcast applications ke liye kaunsa protocol use hota hai?**
 A: UDP.
