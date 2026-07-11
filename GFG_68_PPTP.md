# Point-to-Point Tunneling Protocol (PPTP)

## PPTP Kya Hai?

**PPTP (Point-to-Point Tunneling Protocol)** ek networking protocol hai jo **public network (internet) ke upar secure private connection** banata hai — VPN (Virtual Private Network) ke earliest protocols mein se ek, Microsoft ne 1990s mein develop kiya.

> PPTP ek **tunnel** banata hai do points ke beech — jisse remote user private network se aise connect ho sakta hai jaise wo directly connected ho, chahe wo internet ke through kahin bhi ho.

## PPTP Ki Working

| Component | Kaam |
|---|---|
| **Encapsulation** | Original data ko extra headers ke saath wrap karta hai, tunnel ke through properly transmit karne ke liye |
| **Authentication** | User identity verify karta hai private network access dene se pehle |
| **Encryption** | Data ko unauthorized access se protect karta hai (though PPTP ki encryption modern standards ke hisaab se **weak** maani jaati hai) |

## PPTP Technical Details

| Detail | Value |
|---|---|
| **Layer** | Layer 2 tunneling protocol (PPP frames carry karta hai), but IP (Layer 3) network pe operate karta hai |
| **Control Connection** | TCP port **1723** |
| **Data Tunnel** | **GRE (Generic Routing Encapsulation)** use karta hai PPP frames transport karne ke liye |
| **Encryption** | MPPE (Microsoft Point-to-Point Encryption), up to 128-bit keys |

## PPTP Kaise Kaam Karta Hai (Flow)

1. VPN client PPTP server ko connection request bhejta hai
2. Server request receive karta hai aur user ko **authenticate** karta hai
3. **Control Messages** tunnel establish/manage/terminate karte hain (TCP se)
4. **Data Packets** tunnel ke through user traffic carry karte hain (GRE se)

## PPTP Ke Advantages

| Advantage | Matlab |
|---|---|
| Simple Setup | Zyada operating systems/devices pe easily configure ho jaata hai |
| Lightweight | Kam encryption/processing overhead — better speed |
| Wide Compatibility | Legacy clients/servers support karta hai |

## PPTP Ke Disadvantages (Security Concerns)

| Disadvantage | Matlab |
|---|---|
| **Weak Security** | Known vulnerabilities hain authentication aur encryption mein |
| **MS-CHAPv2 Attacks** | Weak passwords ke saath compromise ho sakta hai |
| **GRE Blocking** | Firewalls/NAT environments mein GRE (IP protocol 47) aksar blocked hoti hai — connection fail ho sakti hai |
| **Obsolete** | Modern VPN protocols (jaise OpenVPN, IKEv2) zyada secure hain |

> Isi wajah se PPTP ko sensitive data ke liye recommend nahi kiya jaata — sirf basic, low-security-requirement tunneling ke liye theek hai.

## Viva One-Liners

- **Q: PPTP ka main kaam kya hai?**
 A: Public network (internet) ke upar secure private connection (VPN tunnel) banana.
- **Q: PPTP kaunsa control port aur data protocol use karta hai?**
 A: Control: TCP port 1723; Data: GRE (Generic Routing Encapsulation).
- **Q: PPTP ko modern use ke liye kyun recommend nahi kiya jaata?**
 A: Kyunki iski encryption/authentication mein known security vulnerabilities hain.
