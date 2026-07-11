# OSI Model (7 Layers)

## OSI Model Kya Hai?

**OSI (Open Systems Interconnection) Model** ek conceptual framework hai jo ISO (International Organization for Standardization) ne banaya — ye batata hai data network mein kaise transmit hota hai, ek structured **7-layer architecture** ke through.

**OSI Model Kya Karta Hai:**

| Kaam | Matlab |
|---|---|
| 7 Functional Layers | Network communication ko 7 layers mein divide karta hai |
| Specific Responsibilities | Har layer ki apni fixed responsibility hoti hai |
| Compatibility | Alag-alag networking systems ke beech compatibility promote karta hai |
| Simplification | Network design, implementation, aur troubleshooting simple banata hai |

---

## Layer 1: Physical Layer

OSI model ki foundation — devices ke beech actual physical connection ka kaam karta hai. Iska main mission hai raw bits (0s aur 1s) ko physical medium se transmit karna.

- **Core Kaam**: Individual bits ka hardware-level transmission manage karta hai; receive karte waqt signals ko wapas digital 0s/1s mein convert karta hai
- **Hardware**: Hubs, Repeaters, Modems, Cables
- **Bit Synchronization**: Clock signal se sender-receiver ko "sync" mein rakhta hai
- **Bit Rate Control**: Transmission speed decide karta hai
- **Topology & Transmission Mode**: Bus/Star/Mesh jaisi topology, aur Simplex/Half-Duplex/Full-Duplex jaisa data flow direction decide karta hai

## Layer 2: Data Link Layer (DLL)

Physical hardware aur logical network ke beech pul — reliable node-to-node data delivery ensure karta hai, error-free transfer ka goal rakhta hai.

1. **Framing**: Network layer se aaye data packets ko chhote "Frames" mein divide karta hai — start/stop bits add karke
2. **Addressing**: MAC addresses use karta hai hosts identify karne ke liye; sender-receiver MAC addresses ko frame header mein daalta hai. Devices: **Switches, Bridges**
3. **Sublayers**:
   - **LLC (Logical Link Control)**: Flow/error control manage karta hai, upper-layer protocols ke liye interface
   - **MAC (Media Access Control)**: Device kaise transmission medium access karega, hardware addressing decide karta hai
4. **Error Control**: Damaged/lost frames detect karke retransmit karta hai
5. **Flow Control**: Fast sender aur slow receiver ke beech data rate sync karta hai
6. **Access Control**: Multiple devices ek channel share karein to kiska turn hai transmit karne ka, decide karta hai

## Layer 3: Network Layer

Different networks ke beech hosts ke beech data transmission manage karta hai — logical addressing aur best path finding.

| Feature | Detail |
|---|---|
| Data Unit | Packets |
| Logical Addressing | Unique IP addresses (sender/receiver) packet header mein |
| Routing | Source se destination tak best path decide karta hai |
| Hardware | Routers, Switches |
| Inter-networking | Alag networks ke beech traffic sahi jagah direct karta hai |

## Layer 4: Transport Layer

Poore messages ka end-to-end delivery ensure karta hai — Application layer ko service deta hai, Network layer ka infrastructure use karke.

- **Data Unit**: Segments
- **Service Point Addressing**: Port Numbers use karta hai (jaise Port 80 web traffic ke liye) — data specific application tak pahunche, na ki sirf device tak
- **Segmentation & Reassembly**: Bade messages ko chhote segments mein split karta hai, destination pe sahi order mein reassemble karta hai
- **Protocols**: TCP (reliable), UDP (fast)
- **Connection-Oriented (TCP)**: Handshake zaroori hai; error checking aur acknowledgements se reliability
- **Connectionless (UDP)**: Bina formal connection ke turant data bhej deta hai; faster but no delivery guarantee

## Layer 5: Session Layer

"Dialogue manager" ka kaam karta hai — do devices ke beech communication channel ka opening, closing, aur security govern karta hai.

- **Session Lifecycle**: Applications ke beech connections establish/maintain/terminate karta hai
- **Authentication & Security**: Communicating parties verify karta hai, connection secure rakhta hai
- **Synchronization**: Data stream mein checkpoints insert karta hai — failure hone pe last saved point se resume ho sake, poora restart na karna pade
- **Dialog Control**: Half-duplex ya full-duplex communication decide karta hai
- **Example**: Web messenger mein Session Layer active link maintain karta hai jab tak chat open hai

## Layer 6: Presentation Layer

"Translation Layer" bhi kehlaata hai — data ko format, secure, aur compress karta hai taaki receiving application usko correctly interpret kar sake.

- **Translation**: Application Layer se data extract karke standardized format mein convert karta hai
- **Standards & Formats**: JPEG, MPEG, GIF jaise encoding standards handle karta hai
- **Encryption/Decryption**: Plain text ko ciphertext mein convert karta hai (encryption) aur wapas (decryption) — typically TLS/SSL se
- **Compression**: Bits ki total count kam karke transmission efficiency badhata hai

## Layer 7: Application Layer

OSI stack ke top pe — software user aur network ke beech direct interface. Data produce karta hai jo bheja jaayega, aur dusri layers se aaya information display karta hai.

- **User Interface**: Network applications (browser, email client) ke liye "window" ka kaam karta hai
- **Core Protocols**: HTTP/S (Web), SMTP (Email), FTP (File Transfer), DNS (Domain Name Resolution)
- **NVT (Network Virtual Terminal)**: Remote host mein login karke interact karne deta hai
- **FTAM**: Remote computer pe files retrieve/manage/manipulate karne ka framework deta hai
- **Directory Services**: Global information ke liye distributed database access deta hai

---

## Data Flow in OSI Model

Jab ek device se dusre device tak information transfer hoti hai, wo 7 layers se hoke travel karti hai — sender ki taraf se **neeche** jaati hai (Layer 7 → 1), receiver ki taraf **upar** aati hai (Layer 1 → 7).

| Layer | Kya Hota Hai |
|---|---|
| Application | Applications data create karte hain |
| Presentation | Data format aur encrypt hota hai |
| Session | Connections establish/manage hoti hain |
| Transport | Data reliable delivery ke liye segments mein todha jaata hai |
| Network | Segments packets mein package hoke route hote hain |
| Data Link | Packets frame hoke next device tak bheje jaate hain |
| Physical | Frames bits mein convert hoke physically transmit hote hain |

> **Example**: Person A, Person B ko email bhejta hai:
> 1. **Application**: Gmail mein email likhta hai
> 2. **Presentation**: Data encrypt/format hota hai
> 3. **Session**: Sender-receiver ke beech connection establish hota hai
> 4. **Transport**: Email data segments mein todha jaata hai, sequence number aur error-checking add hoti hai
> 5. **Network**: Best route ke liye packets ko address kiya jaata hai
> 6. **Data Link**: Packets frames mein encapsulate hote hain, MAC address add hoti hai, error check hota hai
> 7. **Physical**: Frames electrical/optical signals ki form mein cable/WiFi se transmit hoti hain
>
> Receiver ki taraf ye process **reverse** hoti hai.

## Protocols Used in OSI Layers

| Layer | PDU (Data Unit) | Protocols |
|---|---|---|
| Physical | Bits | USB, SONET/SDH |
| Data Link | Frames | Ethernet, PPP, PPTP |
| Network | Packets | IP, ICMP, IGMP, OSPF |
| Transport | Segments (TCP)/Datagrams (UDP) | TCP, UDP, SCTP |
| Session | Data | RPC |
| Presentation | Data | TLS/SSL, MIME |
| Application | Data | FTP, SMTP, DNS, DHCP, NetBIOS |

## Viva One-Liners

- **Q: OSI model mein kitni layers hain aur kaunsi organization ne banaya?**
 A: 7 layers, ISO (International Organization for Standardization) ne banaya.
- **Q: Data Link Layer ka Frame kya hai?**
 A: Network layer se aaye data packet ko chhote units mein divide karke banaya gaya structure, jisme MAC addressing hoti hai.
- **Q: Transport layer segments ko sahi application tak kaise pahunchata hai?**
 A: Port Numbers use karke (jaise Port 80 HTTP ke liye).
- **Q: Encryption/Decryption kaunsi layer handle karti hai?**
 A: Presentation Layer.
