# Classless Network Addressing (CIDR)

## Classless Addressing Kya Hai?

**Classless Addressing**, jise **CIDR (Classless Inter-Domain Routing)** bhi kehte hain, 1993 mein classful addressing ki jagah introduce hua — IP address allocation ko flexible banane aur wastage kam karne ke liye.

- Fixed classes (A, B, C) pe depend nahi karta
- Host bits ka kuch part **network bits** ki tarah use karta hai — actual requirement ke hisaab se subnets banata hai
- IP address ke saath ek **prefix length** likhi jaati hai (jaise `192.168.1.1/28`)

## Classful Se Classless Kyun Shift Hui

> Agar kisi ko 1000 hosts chahiye the, Class C (256 addresses) kam padta tha, aur Class B (65,536 addresses) mein bahut zyada wastage hoti thi. CIDR ne is problem ko solve kiya — flexible-sized blocks allow karke.

## Subnet Mask Kya Karta Hai

**Subnet Mask** ek 32-bit binary value hai jo IP address ke **network portion** aur **host portion** ko separate karta hai.

- IP address aur subnet mask ke beech **bitwise AND** operation karke, network address milta hai
- Classful addressing mein har class ka ek **default (predefined) subnet mask** hota tha
- Classless mein subnet mask **variable** ho sakta hai — kahin bhi cut ho sakta hai, octet boundary pe hona zaroori nahi

## CIDR Notation Example

```
192.168.1.1/28
```
Yahan `/28` batata hai ki pehle 28 bits **network portion** hain, baaki 4 bits **host portion** hain.

## Important Calculations (Classless Addressing)

| Calculation | Formula |
|---|---|
| Number of Hosts per Subnet | 2^(32 - prefix length) - 2 |
| Broadcast Address | Host bits ko 1 karke, network bits same rakhke |
| First Host ID | Subnet address + 1 |
| Last Host ID | Subnet address + Number of Hosts |

## Supernetting

CIDR **supernetting** bhi support karta hai — jisme **multiple contiguous Class C networks** ko combine karke ek bada network (jaise `/23` ya `/22`) banaya jaata hai. Isse routing efficient hoti hai aur IPv4 address space better use hoti hai.

*(Supernetting ka detailed breakdown alag note file mein hai.)*

## Classful vs Classless — Quick Comparison

| Feature | Classful | Classless (CIDR) |
|---|---|---|
| Structure | Fixed classes (A-E) | Flexible, variable-length subnet masks (VLSM) |
| Notation | Class-based default mask | Prefix length (jaise /24) |
| Efficiency | Kam (wastage zyada) | Zyada (need-based allocation) |
| Introduced | 1981 | 1993 |

## Viva One-Liners

- **Q: CIDR ka full form kya hai?**
 A: Classless Inter-Domain Routing.
- **Q: CIDR mein network aur host portion kaise likhi jaati hai?**
 A: IP address ke saath prefix length (jaise `/24`) likhkar.
- **Q: Number of usable hosts per subnet ka formula kya hai?**
 A: 2^(32 - prefix length) - 2.
- **Q: Supernetting kya hai?**
 A: Multiple contiguous Class C networks ko combine karke ek bada network block banana.
