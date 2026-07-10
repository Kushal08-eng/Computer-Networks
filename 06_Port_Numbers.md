# Port Numbers

## Port Number Kya Hai?

**Port Number** ek number hai jo batata hai device ke andar **kaunsi application/service** tak data jaana hai.

> **Analogy**: IP address = poori building ka address. Port number = building ke andar konsa flat/room number hai. Ek hi device (building) mein multiple applications (flats) chal sakte hain — port batata hai kaunse flat mein jaana hai.

## Port Number Range

| Range | Type |
|---|---|
| 0 – 1023 | **Well-Known Ports** (reserved, standard services ke liye) |
| 1024 – 49151 | **Registered Ports** |
| 49152 – 65535 | **Dynamic/Private Ports** |

## Common Well-Known Ports

| Port | Service |
|---|---|
| 20/21 | FTP (File Transfer) |
| 22 | SSH (Remote Login) |
| 25 | SMTP (Email sending) |
| 53 | DNS |
| 80 | HTTP (Website) |
| 443 | HTTPS (Secure Website) |
| 110 | POP3 (Email receiving) |
| 143 | IMAP (Email receiving) |

## IP + Port = Socket

IP address aur Port number milke ek **Socket** banate hain — jo exact batata hai kaunsa device aur us device ke andar kaunsi application.

> Example: `142.250.190.14:443` → us IP wale server pe HTTPS service se connect ho rahe ho.

## Viva One-Liners

- **Q: Port number kyun zaroori hai?**
 A: Ek device pe multiple applications chal sakti hain, port batata hai data kaunsi application tak jaaye.
- **Q: HTTP aur HTTPS ke default ports kya hain?**
 A: HTTP → 80, HTTPS → 443.
