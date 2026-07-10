# Data Transfer, IP Address & Port Number 📦

## 1. Data Transfer Kaise Hota Hai (Short Overview)

Jab bhi tum internet pe kuch bhejte ho (message, file, request), wo data ek saath poora nahi jaata — usko chhote-chhote tukdo mein todke bheja jaata hai jinhe **packets** kehte hain.

**Steps (simple flow):**
1. **Data break** hota hai chhote packets mein.
2. Har packet pe **sender ka IP + Port** aur **receiver ka IP + Port** likha jaata hai (jaise address label).
3. Packets network se travel karte hain (routers ke through), kabhi-kabhi alag-alag raaste se.
4. Destination pe pahunchke sab packets **reassemble** (jodna) hote hain original data banane ke liye.

> **Analogy**: Ek bada parcel courier company todke chhote boxes mein bhejti hai, har box pe address likha hota hai, aur destination pe sab boxes jodke original saaman wapas milta hai.

---

## 2. IP Address Kya Hai?

**IP Address** = device ka unique address network mein, jisse pata chalta hai data **kis device tak** jaana hai.

> **Analogy**: Jaise ghar ka address (city, street, house no.) — bina address ke courier kisi ke ghar nahi pahunch sakta.

**Types:**
| Type | Example | Matlab |
|---|---|---|
| **IPv4** | 192.168.1.1 | 32-bit address, purana format |
| **IPv6** | 2001:0db8::1 | 128-bit address, naya format (zyada addresses ke liye) |

---

## 3. Port Number Kya Hai?

**Port Number** = ek number jo batata hai device ke andar **kaunsi application/service** ko data jaana hai.

> **Analogy**: IP address = poori building ka address, Port number = building ke andar konsa flat/room number hai. Ek hi building (device) mein multiple flats (apps) ho sakte hain.

**Common Port Numbers:**
| Port | Service |
|---|---|
| 80 | HTTP (website) |
| 443 | HTTPS (secure website) |
| 21 | FTP (file transfer) |
| 25 | SMTP (email) |
| 22 | SSH (remote login) |

---

## 4. IP + Port Combo (Socket)

IP address + Port number milke ek **Socket** banate hain, jo exact batata hai — kaunsa device, aur us device ke andar kaunsi application.

> Example: `192.168.1.5:443` matlab — us IP wale device pe HTTPS (secure website) service se connect ho rahe ho.

---

## 5. Quick Viva-Ready One-Liners ✅

- **Q: Data kaise transfer hota hai network mein?**
 A: Chhote packets mein todke bheja jaata hai, destination pe reassemble hota hai.

- **Q: IP address ka kaam kya hai?**
 A: Network mein device ko uniquely identify karta hai.

- **Q: Port number ka kaam kya hai?**
 A: Device ke andar sahi application/service tak data pahunchata hai.

- **Q: Socket kise kehte hain?**
 A: IP address + Port number ka combination.

---

## 6. One-Look Summary

| Concept | Key Point |
|---|---|
| Packet | Data ka chhota tukda jo network mein travel karta hai |
| IP Address | Device ko identify karta hai (konsa ghar) |
| Port Number | Application ko identify karta hai (konsa flat) |
| Socket | IP + Port ka combo |