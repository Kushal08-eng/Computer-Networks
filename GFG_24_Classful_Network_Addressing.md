# Classful Network Addressing

## Classful Addressing Kya Hai?

**Classful IP Addressing** ek early method tha (1981–1993) IP addresses assign karne ke liye — jisme IPv4 address space ko **fixed classes** mein divide kiya jaata tha. Har IP address ke leading bits usko ek class assign karte the, jo uska network aur host portion decide karti thi.

IP addresses ko **5 classes** mein divide kiya gaya: **A, B, C, D, E**.

| Class | Use |
|---|---|
| A, B, C | Unicast communication — large, medium, aur small networks ke liye |
| D | Multicast communication ke liye reserved |
| E | Experimental/research purposes ke liye |

## Har Class Ka Breakdown

### Class A
- Bade number of hosts wale networks ke liye
- Network ID: **8 bits**, Host ID: **24 bits**
- First octet ka higher-order bit hamesha **0**
- Default subnet mask: `255.0.0.0`
- Range: **1.0.0.0 – 126.255.255.255**
- Total networks: 2⁷ - 2 = 126

### Class B
- Medium se large-sized networks ke liye
- Network ID: **16 bits**, Host ID: **16 bits**
- First octet ke higher-order bits hamesha **10**
- Default subnet mask: `255.255.0.0`
- Range: **128.0.0.0 – 191.255.255.255**

### Class C
- Small-sized networks ke liye
- Network ID: **24 bits**, Host ID: **8 bits**
- First octet ke higher-order bits hamesha **110**
- Default subnet mask: `255.255.255.0`
- Range: **192.0.0.0 – 223.255.255.255**

### Class D
- **Multicasting** ke liye reserved
- First octet ke higher-order bits hamesha **1110**
- Range: **224.0.0.0 – 239.255.255.255**
- Koi subnet mask nahi hoti

### Class E
- **Experimental/research** purposes ke liye
- First octet ke higher-order bits hamesha **1111**
- Range: **240.0.0.0 – 255.255.255.254**
- Koi subnet mask nahi hoti

## Special/Reserved Addresses

| Address Range | Use |
|---|---|
| 127.0.0.0 – 127.255.255.255 | Loopback address (device khud se communicate karne ke liye) |
| 0.0.0.0 – 0.0.0.8 | Current network ke andar communicate karne ke liye |
| 169.254.0.0 – 169.254.0.16 | Link-local addresses |

## Advantages Aur Disadvantages

| Advantages | Disadvantages |
|---|---|
| Fixed classes se assign/manage karna simple tha | Internet grow hone pe significant IP wastage hui |
| Routers first bits dekhke class fast identify kar lete the | Routing inefficient ho gayi |
| Alag network sizes support karta tha (large aur small) | Class B allocation aksar zaroorat se bahut zyada address de deti thi |
| Complex subnetting ki zaroorat kam thi | Isi wajah se Classless Addressing (CIDR) 1993 mein introduce hua |

## Viva One-Liners

- **Q: Classful addressing mein kitni classes hain?**
 A: 5 classes — A, B, C, D, E.
- **Q: Class A ka default subnet mask kya hai?**
 A: 255.0.0.0.
- **Q: Class D kis ke liye reserved hai?**
 A: Multicast communication ke liye.
- **Q: Classful addressing ki sabse badi problem kya thi?**
 A: IP address wastage aur routing inefficiency — isi wajah se CIDR (classless addressing) laaya gaya.
