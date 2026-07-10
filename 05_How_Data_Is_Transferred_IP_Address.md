# How Data is Transferred? IP Address

## Data Transfer Ka Basic Flow

1. Data ko chhote **packets** mein todha jaata hai
2. Har packet pe sender aur receiver ka **IP address** likha jaata hai
3. Packets network ke through (routers se hoke) travel karte hain — kabhi alag-alag raaston se
4. Destination pe pahunchke packets **reassemble** hoke original data ban jaate hain

> **Analogy**: Ek bada parcel courier company chhote boxes mein todke bhejti hai, har box pe address likha hota hai. Destination pe sab boxes jodke original saaman milta hai.

## IP Address Kya Hai?

**IP Address (Internet Protocol Address)** ek unique number hai jo network mein har device ko identify karta hai.

> **Analogy**: Jaise har ghar ka ek unique address hota hai (city, street, house number) — bina address ke courier delivery nahi ho sakti. IP address bhi wahi kaam karta hai devices ke liye.

## IP Address Ke Types

| Type | Example | Bits |
|---|---|---|
| **IPv4** | 192.168.1.1 | 32-bit |
| **IPv6** | 2001:0db8::1 | 128-bit |

## Public vs Private IP

| Public IP | Private IP |
|---|---|
| Internet pe directly visible/unique | Sirf local network (home/office) ke andar valid |
| ISP deta hai | Router assign karta hai (jaise 192.168.x.x) |
| Example: Website ka server IP | Example: Tumhare ghar ke devices ka IP |

## Static vs Dynamic IP

| Static IP | Dynamic IP |
|---|---|
| Fixed, change nahi hota | Har baar connect hone pe change ho sakta hai |
| Servers ke liye use hota hai | Home users ke liye common (DHCP se milta hai) |

## Viva One-Liners

- **Q: IP address ka kaam kya hai?**
 A: Network mein device ko uniquely identify karna, taaki data sahi destination tak pahunche.
- **Q: IPv4 aur IPv6 mein basic difference?**
 A: IPv4, 32-bit address hai; IPv6, 128-bit hai (zyada addresses ke liye banaya gaya).
