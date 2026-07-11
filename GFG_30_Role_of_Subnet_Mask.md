# Role of Subnet Mask

## Subnet Mask Ka Role Kya Hai?

**Subnet Mask** IP address ko **network ID** aur **host ID** mein separate karta hai — routers isse decide karte hain ki packet **locally** forward karna hai ya **dusre network** ko bhejna hai.

## Subnet Mask Ke Kaam

| Kaam | Matlab |
|---|---|
| IP Address Split Karna | Network ID aur Host ID mein separate karta hai |
| Network Ko Divide Karna | Bade network ko chhote subnets mein todta hai, better organization ke liye |
| Efficiency Improve Karna | Unnecessary broadcast traffic kam karke network efficiency badhata hai |
| Routing Decision | Router decide karta hai packet local hai ya external network ko bhejna hai |

## Subnetting Ki Zaroorat — Example

**Class A network** ~16 million hosts support karta hai — poore organization mein ek hi flat network rakhna:

- **Maintenance** mushkil ho jaati hai itne saare connected devices ki wajah se
- **Security risks** badh jaate hain — sab devices same network share karte hain

Isko solve karne ke liye, organization apne network ko **subnets** mein divide karta hai — jaise har department (Sales, HR, Accounts) ko apna alag subnet mil jaaye.

## Subnetting Ka Example (Class C)

Suppose ek Class C network `200.1.2.0/24` ko **4 subnets** mein divide karna hai:

1. 4 subnets ke liye **2 bits** borrow karne honge (host part se)
2. Naya subnet mask: `255.255.255.192` (yani `/26`)
3. Har subnet mein 62 usable hosts honge (64 - 2)

### Router Kaise Decide Karta Hai (AND Operation)

```
IP Address:  200.1.2.20   →  11001000.00000001.00000010.00010100
Subnet Mask: 255.255.255.192 → 11111111.11111111.11111111.11000000
------------------------------------------------------------
Result:      200.1.2.0    →  11001000.00000001.00000010.00000000
```

Result batata hai ki IP `200.1.2.20` subnet **`200.1.2.0/26`** ka part hai.

> Agar network ID kisi bhi routing table entry se match nahi hota, packet **default route** pe bhej diya jaata hai. Agar multiple entries match ho jaayein, **longest subnet mask** (zyada 1's) wali entry select hoti hai.

## Subnet Mask Ke Fayde

| Fayda | Matlab |
|---|---|
| **Reduces Congestion** | Broadcast traffic limit karke performance improve karta hai |
| **Efficient IP Usage** | Zaroorat ke hisaab se IPs allocate karta hai, wastage kam |
| **Enhanced Security** | Sensitive data ko specific subnets mein isolate karta hai |
| **Departmental Segmentation** | Specific teams/services ke traffic ko prioritize karta hai |

## Viva One-Liners

- **Q: Subnet mask ka main kaam kya hai?**
 A: IP address ko network ID aur host ID mein separate karna, jisse router decide kar sake packet local hai ya external.
- **Q: Router agar routing table mein multiple matches paaye to kya karta hai?**
 A: Longest subnet mask (zyada 1's) wali entry select karta hai.
- **Q: Subnet mask kaise apply hota hai IP address pe?**
 A: Bitwise AND operation ke through, jisse network address milta hai.
