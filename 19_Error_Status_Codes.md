# HTTP Error / Status Codes

## Status Codes Kya Hain?

Server response ke saath ek **3-digit number** bhejta hai jo batata hai request successful thi ya nahi, aur kya problem hui.

## Categories

| Range | Category | Matlab |
|---|---|---|
| **1xx** | Informational | Request receive hui, processing chal rahi hai |
| **2xx** | Success | Request successful thi |
| **3xx** | Redirection | Further action chahiye (redirect) |
| **4xx** | Client Error | Client ne galat request bheji |
| **5xx** | Server Error | Server mein problem hui |

## Common Status Codes

| Code | Meaning | Kab Milta Hai |
|---|---|---|
| **200 OK** | Success | Request successfully complete hui |
| **201 Created** | Resource create hua | POST request ke baad naya data bana |
| **301 Moved Permanently** | Redirect | URL permanently badal gaya |
| **400 Bad Request** | Client ki galti | Request format galat hai |
| **401 Unauthorized** | Authentication missing | Login/token chahiye |
| **403 Forbidden** | Access denied | Permission nahi hai |
| **404 Not Found** | Resource nahi mila | URL exist nahi karta |
| **500 Internal Server Error** | Server crash/bug | Server side mein error aayi |
| **503 Service Unavailable** | Server overloaded/down | Server temporarily unavailable hai |

> **Analogy**: 2xx = "sab theek hai" (green signal), 4xx = "tumne galti ki" (tumhari request mein problem), 5xx = "humse galti hui" (server ki problem).

## Viva One-Liners

- **Q: 404 error kab aata hai?**
 A: Jab requested resource/URL server pe exist nahi karta.
- **Q: 401 aur 403 mein difference?**
 A: 401 = authentication missing (login chahiye), 403 = authenticated ho but permission nahi hai.
- **Q: 500 error kiski galti hai?**
 A: Server-side error hai, client ki nahi.
