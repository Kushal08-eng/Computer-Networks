# Secure Socket Layer (SSL)

## SSL Kya Hai?

**SSL (Secure Socket Layer)** ek internet security protocol hai jo web browser aur server ke beech data ko **encrypt** karta hai — privacy, authentication, aur data integrity ensure karta hai. Netscape ne 1995 mein banaya tha.

> Aaj SSL ki jagah **TLS (Transport Layer Security)** use hoti hai (1999 se) — but "SSL" term abhi bhi commonly use hoti hai. Websites jo SSL/TLS use karti hain, unki URL mein `HTTPS` dikhti hai (na ki plain `HTTP`).

## SSL Ke Core Kaam

| Kaam | Matlab |
|---|---|
| **Authentication** | Handshake process se client aur server dono ki legitimacy verify karta hai |
| **Data Integrity** | Digital signatures se ensure karta hai ki data transit mein tamper nahi hua |
| **Encryption** | Sensitive data (login credentials, financial info) ko encrypt karta hai |

## SSL Se Pehle Ki Problem

SSL se pehle, web data **plaintext** mein transmit hota tha — koi bhi intercept karke padh sakta tha. SSL isse solve karta hai encryption se.

## SSL Handshake Ke Phases

| Phase | Kya Hota Hai |
|---|---|
| **1. Hello Exchange** | Client aur server hello packets exchange karte hain — protocol version, cipher suite decide karte hain |
| **2. Server Certificate** | Server apna certificate aur key information bhejta hai |
| **3. Client Response** | Client apna certificate aur key exchange bhejta hai |
| **4. Change Cipher Spec** | Handshake finalize hota hai, secure communication activate ho jaata hai |

## SSL Certificates

**SSL Certificates** trusted **Certificate Authorities (CAs)** dwara issue kiye jaate hain — websites secure aur verify karne ke liye.

## SSL Alerts

| Alert Level | Matlab |
|---|---|
| **Warning (Level 1)** | Non-critical issues — jaise expired/unsupported certificates |
| **Fatal (Level 2)** | Critical errors — jaise handshake failures, illegal parameters — connection terminate ho jaata hai |

## Viva One-Liners

- **Q: SSL ka successor kaunsa protocol hai?**
 A: TLS (Transport Layer Security), 1999 se.
- **Q: SSL handshake mein kitne main phases hote hain?**
 A: 4 — Hello exchange, Server certificate, Client response, Change Cipher Spec.
- **Q: SSL/HTTPS use karne wali website kaise identify karte hain?**
 A: URL mein `HTTPS` dikhta hai (na ki plain `HTTP`).
