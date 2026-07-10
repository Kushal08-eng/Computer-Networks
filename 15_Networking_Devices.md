# Networking Devices

## Common Networking Devices

| Device | Layer (OSI) | Kaam |
|---|---|---|
| **Hub** | Physical (L1) | Data ko sabko broadcast karta hai (bina soche kisko chahiye) |
| **Switch** | Data Link (L2) | Data ko sahi destination device tak hi bhejta hai (MAC address se) |
| **Router** | Network (L3) | Ek network se dusre network tak data route karta hai |
| **Modem** | Physical (L1) | Digital ↔ Analog signal conversion (ISP connection ke liye) |
| **Gateway** | Multiple layers | Do alag type ke networks ko connect karta hai (translator jaisa) |
| **Repeater** | Physical (L1) | Signal ko boost karta hai lambi distance ke liye |
| **Bridge** | Data Link (L2) | Do LAN segments ko connect karta hai |
| **Access Point** | Data Link (L2) | Wireless devices ko wired network se connect karta hai (WiFi) |
| **Firewall** | Multiple layers | Security ke liye traffic filter karta hai |

## Detailed Comparison: Hub vs Switch vs Router

| Feature | Hub | Switch | Router |
|---|---|---|---|
| Intelligence | Dumb (broadcast sabko) | Smart (MAC address se target) | Smartest (IP-based routing) |
| Layer | Physical | Data Link | Network |
| Use | Purane networks mein | LAN ke andar devices connect karna | Networks ke beech connect karna |

> **Analogy**: Hub = ek insaan jo poori class mein zor se chillake announcement karta hai (sabko sunta hai chahe zaroorat ho ya na ho). Switch = ek smart peon jo exact us bande tak note pahunchata hai jiske liye hai. Router = wo person jo decide karta hai note kis building (network) mein bhejna hai.

## Viva One-Liners

- **Q: Hub aur Switch mein difference?**
 A: Hub sabko data broadcast karta hai, Switch sirf specific destination device ko.
- **Q: Router ka main kaam kya hai?**
 A: Alag-alag networks ke beech data packets ko route karna.
