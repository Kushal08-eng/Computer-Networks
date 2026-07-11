# Calculate Network, Broadcast, and Host Addresses

## Kyun Zaroori Hai Ye Calculations

Subnetting karte waqt, har subnet ke liye 3 cheezein calculate karni padti hain: **Network Address**, **Broadcast Address**, aur **Usable Host Range**.

## Key Formulas

| Calculation | Formula |
|---|---|
| **Number of Usable Hosts** | 2^h - 2, jahan h = host bits |
| **Number of Subnets** | 2^s, jahan s = borrowed bits (subnet ke liye) |
| **Total Addresses per Subnet** | 2^h |

> **-2** kyun? Kyunki har subnet mein 2 addresses reserved hote hain — **Network Address** (sabse pehla, host bits = sab 0) aur **Broadcast Address** (sabse aakhri, host bits = sab 1) — inhe kisi host ko assign nahi kiya ja sakta.

## Step-by-Step Process

### Step 1: IP Address Ki Class Identify Karo
Class A, B, ya C — first octet ki range dekh ke.

### Step 2: Network Address Nikalo (AND Operation)
```
IP Address:  192.168.254.1  →  Binary form
Subnet Mask: 255.255.255.0  →  Binary form
AND Operation → Network Address: 192.168.254.0
```

### Step 3: Broadcast Address Nikalo
Network address ke host bits ko **sab 1** kar do:
```
Network Address: 192.168.254.0
Broadcast Address: 192.168.254.255
```

### Step 4: Usable Host Range Nikalo
```
First Usable Host = Network Address + 1
Last Usable Host = Broadcast Address - 1
```

## Complete Example

**Given**: IP `192.168.116.32`, Subnet mask `/27` (255.255.255.224)

| Step | Calculation | Result |
|---|---|---|
| Host bits | 32 - 27 = 5 bits | — |
| Total addresses | 2⁵ | 32 |
| Usable hosts | 2⁵ - 2 | 30 |
| Network Address | Host bits = 0 | 192.168.116.32 |
| Broadcast Address | Host bits = 1 | 192.168.116.63 |
| First Usable Host | Network + 1 | 192.168.116.33 |
| Last Usable Host | Broadcast - 1 | 192.168.116.62 |

## Quick Reference Table (Common Subnet Masks)

| CIDR | Subnet Mask | Host Bits | Usable Hosts |
|---|---|---|---|
| /24 | 255.255.255.0 | 8 | 254 |
| /25 | 255.255.255.128 | 7 | 126 |
| /26 | 255.255.255.192 | 6 | 62 |
| /27 | 255.255.255.224 | 5 | 30 |
| /28 | 255.255.255.240 | 4 | 14 |
| /29 | 255.255.255.248 | 3 | 6 |
| /30 | 255.255.255.252 | 2 | 2 |

> **Special Case**: `/31` (2 usable addresses, RFC 3021) point-to-point links ke liye use hota hai jahan broadcast address ki zaroorat nahi hoti.

## Viva One-Liners

- **Q: Usable hosts ka formula kya hai?**
 A: 2^h - 2, jahan h = host bits ki count.
- **Q: -2 kyun karte hain formula mein?**
 A: Network address aur broadcast address kisi host ko assign nahi ho sakte.
- **Q: Broadcast address kaise nikalte hain?**
 A: Network address ke sab host bits ko 1 karke.
- **Q: /30 subnet mein kitne usable hosts hote hain?**
 A: 2 — isiliye point-to-point WAN links ke liye common use hota hai.
