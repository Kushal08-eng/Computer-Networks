# TCP/IP Model (5 Layers)

## TCP/IP Model Kya Hai?

**TCP/IP Model** bhi OSI jaisa hi hai, but zyada practical/simplified — **5 layers** mein organize hota hai (kabhi-kabhi 4 layers bhi kaha jaata hai, jab Physical + Data Link ko combine kar dete hain).

## 5 Layers

| Layer No. | Layer Name | OSI Ke Equivalent Layers | Protocol Examples |
|---|---|---|---|
| 5 | **Application** | Application + Presentation + Session | HTTP, FTP, DNS, SMTP |
| 4 | **Transport** | Transport | TCP, UDP |
| 3 | **Network (Internet)** | Network | IP, ICMP |
| 2 | **Data Link** | Data Link | Ethernet |
| 1 | **Physical** | Physical | Cables, Signals |

## OSI vs TCP/IP Comparison

| OSI Model | TCP/IP Model |
|---|---|
| 7 layers | 5 (ya 4) layers |
| Theoretical/conceptual model | Practically used model (real internet isi pe based hai) |
| Application, Presentation, Session alag hain | Ye teeno TCP/IP mein ek hi "Application" layer mein combine hain |

> **Analogy**: OSI ek detailed textbook diagram hai (theory ke liye best), TCP/IP model wo actual "engine" hai jo real duniya mein internet chalata hai.

## Kyun Zaroori Hai Ye Model Samajhna

- Real internet TCP/IP model pe based hai, na ki pure OSI pe
- Debugging karte waqt pata chalta hai issue kaunsi layer pe hai (jaise DNS issue = Application layer, cable issue = Physical layer)

## Viva One-Liners

- **Q: TCP/IP model mein kitni layers hain?**
 A: 5 (ya kabhi 4, agar Physical+Data Link combine kiya jaaye).
- **Q: Real internet kaunse model pe based hai?**
 A: TCP/IP Model.
