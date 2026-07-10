# HTTP (HyperText Transfer Protocol)

## HTTP Kya Hai?

**HTTP** ek application-layer protocol hai jo **web browsers aur web servers** ke beech communication ke liye use hota hai — websites load karne ka main protocol.

> **Analogy**: Tum browser mein URL type karte ho — ye ek "request letter" bhejne jaisa hai server ko, aur server webpage (response) wapas bhejta hai.

## HTTP Request-Response Model

1. **Client (Browser)** ek HTTP request bhejta hai server ko
2. **Server** request process karta hai
3. **Server** ek HTTP response wapas bhejta hai (HTML, CSS, JSON, etc.)

## HTTP Request Ka Structure

| Part | Matlab |
|---|---|
| **Method** | Kya action karna hai (GET, POST, etc.) |
| **URL** | Kaunsa resource chahiye |
| **Headers** | Extra info (browser type, content type) |
| **Body** | Data jo bheja jaa raha hai (optional, jaise form data) |

## HTTP Ki Key Properties

- **Stateless**: Har request independent hoti hai — server ko pichhli request yaad nahi rehti (isiliye Cookies ka use hota hai state maintain karne ke liye)
- **Text-based**: Human-readable format mein data bhejta hai

## HTTP vs HTTPS

| HTTP | HTTPS |
|---|---|
| Data plain text mein jaata hai | Data encrypted hota hai (SSL/TLS) |
| Port 80 | Port 443 |
| Less secure | Secure (banking, login pages ke liye must) |

## Viva One-Liners

- **Q: HTTP stateless kyun hai?**
 A: Kyunki har request independent hoti hai, server pichhli request ka context store nahi karta.
- **Q: HTTP ka default port?**
 A: 80 (HTTPS ka 443).
