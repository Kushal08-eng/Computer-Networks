# OSI Model (7 Layers)

## OSI Model Kya Hai?

**OSI (Open Systems Interconnection) Model** ek conceptual framework hai jo networking ko **7 layers** mein divide karta hai — har layer ka apna specific kaam hota hai.

> **Analogy**: Jaise ek company mein alag departments hote hain (HR, Finance, Tech) — har department apna specific kaam karta hai, but milke company chalti hai. Waise hi OSI ke layers milke poora communication complete karte hain.

## 7 Layers (Top to Bottom)

| Layer No. | Layer Name | Kaam | Example/Protocol |
|---|---|---|---|
| 7 | **Application** | User ke saath direct interaction | HTTP, FTP, SMTP |
| 6 | **Presentation** | Data ka format, encryption, compression | SSL/TLS, JPEG |
| 5 | **Session** | Connection establish/maintain/terminate karta hai | NetBIOS, RPC |
| 4 | **Transport** | Reliable/unreliable data delivery, end-to-end | TCP, UDP |
| 3 | **Network** | Routing, logical addressing (IP) | IP, ICMP |
| 2 | **Data Link** | Physical addressing (MAC), error detection | Ethernet, PPP |
| 1 | **Physical** | Actual bits ka transmission (electrical/light signals) | Cables, Hubs |

## Mnemonic (Yaad Rakhne Ke Liye)

**"All People Seem To Need Data Processing"**
(Application, Presentation, Session, Transport, Network, Data Link, Physical)

## Layer-Wise Simple Explanation

- **Physical**: Raw bits (0s and 1s) ko electrical/light signal mein bhejta hai
- **Data Link**: Same network ke devices ke beech data frame bhejta hai, MAC address use karta hai
- **Network**: Different networks ke beech routing karta hai, IP address use karta hai
- **Transport**: Data ko reliably (TCP) ya fast (UDP) end-to-end deliver karta hai
- **Session**: Connection ko open/maintain/close karta hai
- **Presentation**: Data ko encrypt/decrypt, compress/decompress karta hai
- **Application**: User-facing services (browser, email client)

## Viva One-Liners

- **Q: OSI model mein kitni layers hain?**
 A: 7 layers.
- **Q: Data link layer kya use karta hai addressing ke liye?**
 A: MAC address.
- **Q: Network layer ka main kaam?**
 A: Routing aur logical (IP) addressing.
