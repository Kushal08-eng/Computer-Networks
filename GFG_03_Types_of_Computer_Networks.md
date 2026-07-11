# Types of Computer Networks

## Overview

Computer networks ko classify karne ke 3 major tareeke hain:

1. **Geographical Area** ke basis pe
2. **Transmission Medium** ke basis pe
3. **Ownership aur Access Control** ke basis pe

---

## 1. Classification Based on Geographical Area

### a) Personal Area Network (PAN)
Ek single user ke personal devices ko bahut short range mein connect karta hai.

| Detail | Value |
|---|---|
| Range | 1–10 meters |
| Technologies | Bluetooth, NFC, Infrared |
| Example | Smartphone se wireless earbuds connected |

### b) Local Area Network (LAN)
Ek limited area (ghar, office, building) ke andar devices ko connect karta hai.

| Detail | Value |
|---|---|
| Range | Ek room, building, ya chhota campus |
| Technologies | Ethernet, WiFi |
| Example | Ghar ya office ka WiFi network |

### c) Campus Area Network (CAN)
Ek campus ya nearby buildings ke group ke andar multiple LANs ko connect karta hai.

| Detail | Value |
|---|---|
| Range | University ya corporate campus |
| Technologies | Ethernet, Fiber Optics |
| Example | College ya corporate campus network |

### d) Metropolitan Area Network (MAN)
Ek city ya metropolitan region ke andar multiple networks ko connect karta hai.

| Detail | Value |
|---|---|
| Range | City ya bada town |
| Technologies | Fiber Optics, Microwave, Metro Ethernet |
| Example | City-wide ISP network |

### e) Wide Area Network (WAN)
Bade geographical areas (countries, continents) ke networks ko connect karta hai.

| Detail | Value |
|---|---|
| Range | Country, continent, ya global |
| Technologies | Leased lines, Satellite links, Internet |
| Example | Internet khud |

> **Analogy**: PAN = tumhara personal bag, LAN = tumhare ghar/office ka network, CAN = poore college campus ka network, MAN = pura city connected, WAN = pura duniya connected.

---

## 2. Classification Based on Transmission Medium

### a) Broadcast Network
Sab connected devices ek shared communication medium use karte hain.

- Ek node se bheja gaya data **sab dusre nodes ko** milta hai
- Har packet mein destination address hota hai — sirf wahi device usko process karta hai jiske liye hai
- **One-to-many** communication model
- Sender aur receiver ke beech koi dedicated physical path nahi hota

**Examples**: Ethernet (bus-based), Wireless LAN (WiFi)

### b) Point-to-Point Network
Communicating devices ke beech **dedicated links** use hote hain.

- Data seedha ek node se dusre node tak jaata hai
- **One-to-one** communication model
- Data intermediate devices (routers/switches) se hoke bhi guzar sakta hai
- Best path decide karne ke liye routing algorithms chahiye hote hain

**Examples**: Internet, Leased line networks, Telephone networks

---

## 3. Classification Based on Ownership and Access Control

### a) Private Network
Kisi individual, organization, ya institution dwara owned aur managed hota hai.

- Access sirf authorized users tak restricted
- Authentication zaroori (username, password, VPN, access tokens)
- Mainly internal communication ke liye use hota hai
- Higher security, privacy, aur control offer karta hai

**Examples**: Corporate intranet, Office LAN, Private cloud network

### b) Public Network
Service providers ya government authorities dwara owned hota hai.

- General public ke liye accessible
- Connect karne ke liye kam ya koi authorization nahi chahiye
- Wide accessibility deta hai, but security kam hoti hai
- Bade number of users share karte hain

**Examples**: Internet, Public WiFi networks, Mobile cellular networks

### c) Hybrid Network
Private aur Public networks ka combination.

- Kuch parts restricted hote hain, kuch publicly accessible
- Organizations internal security maintain karte hue external connectivity bhi de sakte hain
- Modern enterprise/cloud-based systems mein common

**Examples**: Corporate network jo Internet se connected ho, Enterprise cloud networks, Online banking systems

---

## Internetwork

**Internetwork** do ya zyada independent networks ka collection hai jo aapas mein jud ke ek single logical network ki tarah kaam karte hain.

- Different networks ke devices ke beech communication enable karta hai
- Internet khud sabse bada internetwork example hai
- Sirf individual computers nahi, balki multiple networks se milkar banta hai
- Networking devices use hote hain interconnect karne ke liye

### Intranet
Ek organization ke andar use hone wala **private** network — sirf authorized users (jaise employees) ke liye accessible.

| Detail | Info |
|---|---|
| Ownership | Single organization control karti hai |
| Access | Login credentials se restricted |
| Use | Internal communication aur collaboration |

**Uses**: Employee portals, Internal emails/messaging, Company policies sharing, Internal applications (HR, payroll)

**Examples**: Corporate internal website, University campus portal, Government department internal system

### Extranet
Intranet ka extension jo **limited access** external users ko deta hai — organization ke internal network ko trusted outsiders se connect karta hai.

| Detail | Info |
|---|---|
| Type | Partially private network |
| Access | Partners, vendors, suppliers, customers ko |
| Security | Authentication/authorization zaroori, aksar VPN ya secure web access se implement hota hai |

**Uses**: B2B communication, Supply chain management, Customer portals, Partner collaboration platforms

**Examples**: Supplier management system, Online banking portals, Vendor access portals

> **Analogy**: Intranet ek office ka andaruni WhatsApp group jaisa hai (sirf employees). Extranet ek group jisme kuch trusted outside vendors/partners ko bhi add kiya gaya ho, but sabko sab kuch dikhna zaroori nahi.

## Viva One-Liners

- **Q: Networks ko classify karne ke 3 main tareeke kaunse hain?**
 A: Geographical area, Transmission medium, aur Ownership/Access control ke basis pe.
- **Q: Broadcast aur Point-to-Point network mein basic difference?**
 A: Broadcast mein data sabko milta hai (one-to-many), Point-to-Point mein dedicated link se ek-dusre tak (one-to-one) jaata hai.
- **Q: Intranet aur Extranet mein difference?**
 A: Intranet sirf organization ke andar (employees) accessible hota hai, Extranet trusted outsiders (partners/vendors) ko bhi limited access deta hai.
- **Q: CAN aur MAN mein difference?**
 A: CAN ek campus ke multiple LANs ko connect karta hai, MAN ek poori city ke networks ko.
