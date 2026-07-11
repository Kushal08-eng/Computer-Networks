# Network Devices

## Network Devices Kya Hain?

**Network Devices** physical hardware appliances hain jo computers ke beech communication aur interaction ke liye zaroori hote hain.

**Inka Kaam:**

| Function | Matlab |
|---|---|
| Communication Enable Karna | Devices ke beech data transmit/receive karwana |
| Connection | Devices ko network se securely connect karna |
| Performance Improve Karna | Congestion kam karke traffic manage karna |
| Coverage Extend Karna | Signal loss/attenuation ki problem solve karna |

Network devices ko unke OSI layer ke hisaab se categorize kiya jaata hai — jitni upar wali layer, utni zyada "smart" processing device karti hai.

---

## Layer 1 Devices — Physical Layer

Ye devices raw electrical/optical signals (bits) ke saath kaam karte hain — inhe IP address ya MAC address ka pata nahi hota, ye sirf signal handle karte hain.

### 1. Hub
LAN mein devices ke liye ek central connection point.
- Ek port pe aane wale signal ko **blindly sabhi ports pe broadcast** kar deta hai, bina ye jaane ki data kiske liye hai
- High traffic collisions aur security risk (sabko sab ka data dikh jaata hai)
- Ab **obsolete** hai, Switches ne replace kar diya hai

### 2. Repeater
Signal ko regenerate karke network ka range extend karta hai.
- Weak signal (lambi cable ki wajah se attenuation) ko receive karke, amplify karke, retransmit karta hai
- Use: WiFi range ya Ethernet cable ko 100 meters se aage extend karna

### 3. Modem (Modulator-Demodulator)
Digital computer data aur analog signals ke beech pul (bridge) ka kaam karta hai.
- Ghar/office network ko ISP se connect karta hai
- Digital signal ko analog mein convert karta hai (**Modulation**) aur analog ko digital mein wapas (**Demodulation**)

---

## Layer 2 Devices — Data Link Layer

Ye devices **MAC Address** (Physical Address) ke saath kaam karte hain — Hub se zyada smart hote hain.

### 4. Switch
High-speed device jo LAN ke andar devices (computers, printers, servers) ko connect karta hai.
- Hub ke ulta, switch har connected device ka **MAC address seekhta** hai
- Data sirf us specific port pe bhejta hai jahan destination device connected hai
- Collisions kam karta hai, security aur speed improve karta hai

### 5. Bridge
Do alag LAN segments ko connect karke ek jaisa dikhata hai.
- MAC address ke basis pe traffic filter karta hai — local traffic ko local hi rakhta hai, congestion kam karta hai
- Ab zyada tar **Switches** ne replace kar diya hai (jo essentially multi-port bridges hi hote hain)

### 6. Access Point (AP)
WiFi-enabled devices (laptop, smartphone) ko wired network se connect karne deta hai.
- Wired Ethernet aur wireless WiFi devices ke beech bridge ka kaam karta hai
- Sirf WiFi signal provide karta hai — traffic route nahi karta, IP address assign nahi karta

---

## Layer 3 Devices — Network Layer

Ye devices **IP Address** (Logical Address) ke saath kaam karte hain aur alag-alag networks ko connect karte hain.

### 7. Router
Multiple networks ko connect karke unke beech data packets direct karta hai.
- IP address use karke best path decide karta hai
- Ek **Routing Table** maintain karta hai decisions lene ke liye
- Broadcast traffic ko rokta hai, networks ko isolate karta hai

### 8. Brouter (Bridging Router)
Bridge aur Router dono ke functions combine karta hai — Data Link aur Network dono layers pe operate karta hai.
- Known protocols (jaise TCP/IP) ko route kar sakta hai
- Unknown protocols ko bridge kar sakta hai — aaj kal rarely use hota hai

---

## Layer 4-7 Devices — Advanced Processing

### 9. Gateway
Do alag protocols use karne wale networks ke beech entry/exit point ka kaam karta hai, data translate karke compatibility ensure karta hai.
- Protocols, data formats, ya architectures convert kar sakta hai (jaise TCP/IP network ko legacy Mainframe network se connect karna)
- Internet Gateway private LAN requests ko public internet requests mein translate karta hai

### 10. Firewall
Network security system (hardware/software/dono) jo predetermined security rules ke basis pe incoming/outgoing traffic monitor aur control karta hai.
- Network edge pe physical appliance ho sakta hai
- Kisi specific server/PC pe install ho sakta hai
- Active connections track karta hai

---

## Hub vs Switch vs Router (Comparison)

| Feature | Hub | Switch | Router |
|---|---|---|---|
| **Layer** | Layer 1 (Physical) | Layer 2 (Data Link) | Layer 3 (Network) |
| **Address Type** | Koi nahi (sirf bits) | MAC Address | IP Address |
| **Data Flow** | Broadcast (sabko) | Unicast (destination ko) | Route (best path se) |
| **Intelligence** | Dumb | Smart | Smarter |
| **Used For** | Obsolete | Devices connect karna (LAN) | Networks connect karna (WAN) |

## Viva One-Liners

- **Q: Hub obsolete kyun ho gaya?**
 A: Kyunki wo data sabko blindly broadcast karta hai, jisse traffic collision aur security risk badhta hai — Switch better alternative hai.
- **Q: Switch aur Bridge mein kya similarity hai?**
 A: Dono MAC address use karke traffic filter karte hain — Switch ko essentially multi-port bridge kaha ja sakta hai.
- **Q: Brouter kya karta hai?**
 A: Bridge aur Router dono ka kaam karta hai — Data Link aur Network layer, dono pe operate karta hai.
- **Q: Gateway ka main use case kya hai?**
 A: Alag protocols wale networks ke beech data translate karke compatibility banana.
