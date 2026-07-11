# TCP Connection Termination

## TCP Termination Kya Hai?

TCP connection ko **orderly close** karne ka process — 4-step handshake (FIN-ACK exchange) use karta hai, taaki dono devices confirm kar sakein ki data transfer poora ho chuka hai.

## Connection Release Ke 2 Types

| Type | Matlab |
|---|---|
| **Graceful Release** | Connection tab tak open rehta hai jab tak dono parties apni taraf close na kar dein |
| **Abrupt Release** | RST segment se force karke connection close kiya jaata hai (errors ki wajah se) |

## 4-Way Handshake Ke Steps

| Step | Kaun Bhejta Hai | Flag | Matlab |
|---|---|---|---|
| 1 | Client (ya jo close karna chahta hai) → Server | **FIN** | "Mai apni taraf se close karna chahta hoon" |
| 2 | Server → Client | **ACK** | FIN receive hone ka confirmation |
| 3 | Server → Client | **FIN** | Server bhi apni taraf close karna chahta hai |
| 4 | Client → Server | **ACK** | Final confirmation — connection fully closed |

## 4-Way Handshake Kyun Zaroori Hai (Na Ki 3-Way)

TCP **full-duplex** hota hai — dono directions independently close karni padti hain. Isliye:

- Pehle client apni taraf se data bhejna band karta hai (**FIN**), server **ACK** karta hai
- Client **FIN_WAIT_2** state mein wait karta hai server ke FIN ka
- Server bhi apna FIN bhejta hai jab uska data bhejna khatam ho jaata hai
- Client final **ACK** bhejta hai

> Kabhi-kabhi steps 2 aur 3 ek hi packet mein combine ho sakte hain (agar server ke paas bhi turant bhejne ke liye FIN ho) — is case mein ye "3-way" jaisa dikh sakta hai, but conceptually 4 steps hote hain.

## RST (Abrupt Termination)

**RST segment** in cases mein bheja jaata hai:
- Jab non-existing connection ke liye non-SYN segment receive ho
- Unrecoverable errors ki wajah se
- Jab connection ko turant, bina graceful closure ke, terminate karna ho

## Viva One-Liners

- **Q: TCP termination mein kitne steps hote hain, aur kyun?**
 A: 4 steps — kyunki TCP full-duplex hai, dono directions ko independently close karna padta hai.
- **Q: Graceful aur Abrupt release mein difference?**
 A: Graceful mein dono taraf se properly FIN-ACK exchange hota hai; Abrupt mein RST se force karke turant close kiya jaata hai.
- **Q: RST flag kab use hota hai?**
 A: Errors ya invalid connections ki wajah se, connection ko abruptly terminate karne ke liye.
