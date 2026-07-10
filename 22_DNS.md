# DNS (Domain Name System)

## DNS Kya Hai?

**DNS** ek system hai jo human-friendly **domain names** (jaise google.com) ko computer-friendly **IP addresses** (jaise 142.250.190.14) mein convert karta hai.

> **Analogy**: DNS ek phonebook jaisa hai — tum kisi ka naam jaante ho but unka phone number yaad nahi, phonebook check karke number mil jaata hai. Waise hi browser domain naam se IP address DNS se dhoondh ta hai.

## DNS Zaroori Kyun Hai?

Insaan ke liye naam (google.com) yaad rakhna easy hai, but computers sirf **IP address** se communicate karte hain — DNS is gap ko bridge karta hai.

## DNS Resolution Process (Simple Flow)

1. Tum browser mein `google.com` type karte ho
2. Tumhara device pehle apne **local cache** check karta hai (pehle se pata hai kya?)
3. Agar nahi pata, request jaati hai **DNS Resolver** (usually ISP ka) ke paas
4. Resolver **Root Server** se puchta hai
5. Root Server bata deta hai kahan `.com` domains ke liye jaana hai — **TLD Server**
6. TLD Server bata deta hai google.com ka **Authoritative Server** kaun sa hai
7. Authoritative Server final IP address deta hai
8. Browser ab us IP address pe connect karta hai

## DNS Hierarchy

| Level | Example |
|---|---|
| **Root Server** | Top level, sabse pehla point |
| **TLD Server** | `.com`, `.org`, `.in` jaise domains handle karta hai |
| **Authoritative Server** | Specific domain (google.com) ka actual record rakhta hai |

## Common DNS Record Types

| Record | Kaam |
|---|---|
| **A** | Domain → IPv4 address |
| **AAAA** | Domain → IPv6 address |
| **CNAME** | Ek domain ko dusre domain ka alias banata hai |
| **MX** | Mail server ka record (email ke liye) |

## Viva One-Liners

- **Q: DNS ka kaam kya hai?**
 A: Domain name ko IP address mein convert karna.
- **Q: DNS resolution ka pehla step kya hai?**
 A: Local cache check karna, agar nahi mila to DNS Resolver ko request jaati hai.
