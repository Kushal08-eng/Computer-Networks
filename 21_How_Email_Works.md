# How Email Works?

## Basic Flow

Jab tum email bhejte ho, ye multiple protocols aur mail servers se hoke guzarta hai:

1. Tum **compose** karte ho aur "Send" dabaate ho
2. Tumhara mail client **SMTP** (Simple Mail Transfer Protocol) use karke email tumhare mail server tak bhejta hai
3. Tumhara mail server DNS se receiver ke mail server ka address dhoondh ta hai
4. SMTP se hi email receiver ke mail server tak forward hoti hai
5. Receiver apna mail client (Gmail app, Outlook) use karke **POP3** ya **IMAP** protocol se email download/access karta hai

> **Analogy**: Email bhejna dak (post) system jaisa hai — SMTP "postman" hai jo letter ko sender ke post office se receiver ke post office tak le jaata hai. POP3/IMAP wo tareeka hai jisse receiver apne post office se letter collect karta hai.

## Key Protocols Involved

| Protocol | Kaam |
|---|---|
| **SMTP** | Email **bhejne** ke liye (sender → mail server → receiver's mail server) |
| **POP3** | Email **download** karke local device pe store karta hai (server se delete ho jaata hai generally) |
| **IMAP** | Email server pe hi rehta hai, multiple devices se sync hoke access hota hai |

## POP3 vs IMAP

| POP3 | IMAP |
|---|---|
| Email download hoke device pe store hota hai | Email server pe rehta hai, sync hota hai |
| Ek hi device se best access | Multiple devices se access easy |
| Offline access easy | Internet chahiye sync ke liye |

## Email Address Ka Structure

```
username@domain.com
```
- **username**: Specific mailbox
- **domain**: Mail server jahan mailbox host hai (jaise gmail.com)

## Viva One-Liners

- **Q: Email bhejne ke liye kaunsa protocol use hota hai?**
 A: SMTP.
- **Q: Email receive/download karne ke liye kaunse protocols hain?**
 A: POP3 aur IMAP.
