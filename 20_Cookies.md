# Cookies

## Cookies Kya Hain?

**Cookies** chhote pieces of data hain jo server browser mein **store** karwata hai, taaki HTTP ke stateless nature ke bawajood server user ko "yaad" rakh sake.

> **Analogy**: Jaise kisi amusement park mein entry ke time haath pe stamp laga dete hain — dobara enter karte waqt stamp dikhake pehchaan ho jaati hai ki tum already registered ho. Cookie bhi browser mein wahi "stamp" hai.

## Cookies Kyun Zaroori Hain?

HTTP **stateless** hai — matlab server ko pichhli request yaad nahi rehti. Cookies is problem ko solve karti hain:

| Use Case | Example |
|---|---|
| **Login Session** | Ek baar login karne ke baad baar-baar login na maangna |
| **Shopping Cart** | Cart mein items yaad rakhna jab tak checkout na ho |
| **Preferences** | Dark mode, language preference yaad rakhna |
| **Tracking/Analytics** | User behavior track karna (ads ke liye) |

## Types of Cookies

| Type | Matlab |
|---|---|
| **Session Cookie** | Browser band hote hi delete ho jaati hai |
| **Persistent Cookie** | Fixed expiry date tak store rehti hai |
| **First-party Cookie** | Wahi website set karti hai jo visit kar rahe ho |
| **Third-party Cookie** | Doosri website (jaise ad network) set karti hai |

## Cookie Kaise Kaam Karti Hai (Flow)

1. Browser server ko request bhejta hai
2. Server response ke saath ek cookie bhejta hai (`Set-Cookie` header)
3. Browser cookie ko store kar leta hai
4. Agli baar jab bhi us server ko request jaati hai, browser automatically cookie attach kar deta hai

## Viva One-Liners

- **Q: Cookies kyun zaroori hain?**
 A: HTTP stateless hota hai, cookies server ko user session/state yaad rakhne mein help karti hain.
- **Q: Session cookie aur persistent cookie mein difference?**
 A: Session cookie browser band hote hi delete ho jaati hai, persistent cookie fixed time tak rehti hai.
