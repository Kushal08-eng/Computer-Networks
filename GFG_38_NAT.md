# Network Address Translation (NAT)

## NAT Kya Hai?

**NAT (Network Address Translation)** ek technique hai jo private network ke multiple devices ko **single public IP address** se internet access karne deti hai — private IP addresses ko public mein (aur vice-versa) translate karke.

| Fayda | Matlab |
|---|---|
| **IPv4 Address Conservation** | Limited IPv4 addresses efficiently use hote hain |
| **Security** | Internal network structure bahar se hidden rehta hai |
| **Cost-Effective** | Multiple public IPs kharidne ki zaroorat nahi |

## NAT Kaise Kaam Karta Hai

- **Inside Address**: Private network ke andar ka device address
- **Outside Address**: External/internet-facing address
- Translation tab hoti hai jab **inside devices outside networks** se communicate karte hain
- Router/NAT device ek **translation table** maintain karta hai — track karne ke liye kaunsi private IP kis public session se associated hai

## Types of NAT

### 1. Static NAT
Ek private IP **permanently** ek fixed public IP se mapped hoti hai — **one-to-one** mapping.

| Use Case | Servers host karna jo internet se accessible hone chahiye (jaise web server) |
|---|---|

### 2. Dynamic NAT
Private IPs ko public IPs se map kiya jaata hai, but ek **predefined pool** se — mapping fixed nahi hoti.

- Jab device connection initiate karta hai, NAT device pool se ek **available public IP** assign karta hai
- Session khatam hone pe, wo public IP wapas pool mein chali jaati hai (dusre device ke liye available)

### 3. PAT (Port Address Translation) — "NAT Overload"
Sabse common type — **multiple private IPs ek hi public IP** share karte hain, **different port numbers** se differentiate hote hue.

- Jab device communication start karta hai, PAT ek unique **source port number** assign karta hai
- Private IP + Port number ka combination har session ko uniquely identify karta hai
- Isiliye "NAT Overload" bhi kehte hain — ek hi public IP "overload" hoke thousands of sessions handle kar leta hai

## Static vs Dynamic vs PAT

| Feature | Static NAT | Dynamic NAT | PAT |
|---|---|---|---|
| Mapping | One-to-one (fixed) | One-to-one (pool se, temporary) | Many-to-one (port se differentiate) |
| Use Case | Servers (fixed accessibility) | Kabhi-kabhi internet use karne wale devices | Home/office networks — multiple devices, ek public IP |
| Public IPs Chahiye | Har device ke liye ek | Pool mein multiple, but reused | Sirf ek (ya kuch) |
| Most Common? | Nahi | Nahi | **Haan** — cost-effective, widely used |

## NAT Ka Real-World Example

> Ghar mein computer, smartphone, aur smart TV — teeno internet use kar rahe hain. NAT ke bina, har device ko apna alag public IP chahiye hota. NAT ke saath, router ek hi public IP se sabko internet access deta hai, port numbers se differentiate karke.

## Viva One-Liners

- **Q: NAT ka main purpose kya hai?**
 A: Multiple private IP devices ko ek (ya kuch) public IP addresses se internet access dena, IPv4 address conserve karte hue.
- **Q: PAT ko "NAT Overload" kyun kehte hain?**
 A: Kyunki ek hi public IP multiple private devices ke saath simultaneously use hoti hai, port numbers se differentiate karte hue.
- **Q: Static NAT kab use hota hai?**
 A: Jab device (jaise server) ko fixed, consistent public IP chahiye ho internet se accessibility ke liye.
