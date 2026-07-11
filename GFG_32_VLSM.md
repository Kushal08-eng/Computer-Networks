# Variable Length Subnet Masking (VLSM)

## VLSM Kya Hai?

**VLSM (Variable Length Subnet Mask)** ek subnetting technique hai jisme network administrators ek IP network ko **different sizes** ke subnets mein divide kar sakte hain — same network ke andar **multiple subnet masks** use karke, har subnet ki actual host requirement ke hisaab se.

> Isko "**subnetting the subnet**" bhi kaha jaata hai.

## FLSM vs VLSM

| FLSM (Fixed Length Subnet Mask) | VLSM (Variable Length Subnet Mask) |
|---|---|
| Sab subnets ka **same size** hota hai | Har subnet ka size **alag** ho sakta hai (requirement ke hisaab se) |
| IP wastage zyada hoti hai | IP wastage minimum hoti hai |
| Simple but inefficient | Complex but efficient |
| Private IPs ke liye preferred | Public IPs ke liye best (wastage minimize karna zaroori hai) |

## FLSM Ki Problem (Example)

Agar tumhe 2 departments ke liye subnets chahiye — ek mein 100 hosts, dusre mein sirf 5 hosts — aur FLSM use karo (`/24` mask, 254 hosts har subnet mein), to dono departments ko **254 IPs** milengi, chahe dusre department ko sirf 5 chahiye the. Ye **huge wastage** hai.

## VLSM Kaise Kaam Karta Hai

VLSM mein tumhe har subnet ke liye **block size zaroorat ke barabar ya thoda zyada** choose karna hota hai — jitna kam wastage utna better.

### Example (4 Departments)

Suppose ek admin ke paas `192.168.1.0/24` hai, aur 4 departments hain:

| Department | Hosts Chahiye | Allocated Subnet | Subnet Mask | Valid Hosts |
|---|---|---|---|---|
| Sales & Purchase | 120 | 192.168.1.0/25 | 255.255.255.128 | 126 |
| Development | 50 | 192.168.1.128/26 | 255.255.255.192 | 62 |
| Accounts | 26 | 192.168.1.192/27 | 255.255.255.224 | 30 |
| Management | 5 | 192.168.1.224/29 | 255.255.255.248 | 6 |

> **Process**: Sabse **badi requirement** ko pehle allocate karo (highest IP block), phir chhoti requirements ko baad mein — isse minimum wastage hoti hai.

## VLSM Ke Advantages

| Advantage | Matlab |
|---|---|
| **Minimum IP Wastage** | Har subnet ko exact zaroorat ke hisaab se size milta hai |
| **Scalability** | Naye subnets add karna easy, bina poore IP plan ko redesign kiye |
| **Reduced Broadcast Traffic** | Well-sized subnets se unnecessary traffic kam hoti hai |
| **Real-World Use** | OSPF, EIGRP, BGP jaise routing protocols mein widely use hota hai |

## VLSM Ke Disadvantages

| Disadvantage | Matlab |
|---|---|
| Advanced Planning Chahiye | Deep subnetting knowledge zaroori hai |
| Zyada Configuration | More subnets = more documentation/management |
| Fragmented IP Space | Subnets scattered ho sakte hain, track karna mushkil |
| Legacy Support | Purana hardware/protocols VLSM support nahi kar sakte |

## Viva One-Liners

- **Q: VLSM kya hai?**
 A: Ek subnetting technique jisme same network ke andar different-sized subnets, alag subnet masks use karke banaye jaate hain.
- **Q: VLSM ko "subnetting the subnet" kyun kehte hain?**
 A: Kyunki ye ek subnet ko further chhote subnets mein divide karta hai, alag mask lengths ke saath.
- **Q: VLSM allocation kis order mein karni chahiye?**
 A: Sabse badi requirement pehle, phir chhoti requirements — isse wastage minimum hoti hai.
