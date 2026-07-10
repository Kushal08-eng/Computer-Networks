# Peer to Peer (P2P) Architecture

## Kya Hai?

**Peer-to-Peer (P2P)** architecture mein har device (peer) dono kaam kar sakta hai — client bhi, server bhi. Koi ek fixed central server nahi hota.

> **Analogy**: Dosto ke group mein sab ek dusre se directly notes share karte hain — koi ek fixed "provider" nahi hota, sab equal hote hain.

## Kaise Kaam Karta Hai

- Har peer apne paas kuch resources/files rakhta hai
- Jab koi file chahiye hoti hai, peer directly dusre peer se connect hoke le leta hai
- Koi central authority control nahi karti

## Advantages

| Fayda | Matlab |
|---|---|
| No single point of failure | Ek peer down ho to baaki system chalta rahta hai |
| Cost-effective | Koi expensive central server maintain nahi karna |
| Scalable | Zyada peers = zyada resources available |

## Disadvantages

| Nuksaan | Matlab |
|---|---|
| Security kam | Har peer directly connect hota hai, control karna mushkil |
| Reliability inconsistent | Peer offline ho jaaye to us peer ka data unavailable ho jaata hai |
| Management difficult | Koi central control nahi hota |

## Client-Server vs P2P

| Client-Server | Peer-to-Peer |
|---|---|
| Centralized control | Decentralized |
| Server crash = sab affected | Ek peer fail = baaki chalte rehte hain |
| Security better manage hoti hai | Security manage karna mushkil |
| Example: Gmail, YouTube | Example: BitTorrent, old Skype |

## Real Example

**BitTorrent**: File ko chhote pieces mein todke multiple peers se simultaneously download karte ho — jitne zyada peers "seed" kar rahe hain, utni fast download hoti hai.

## Viva One-Liner

> "P2P architecture mein koi central server nahi hota — har device client aur server dono ka kaam karta hai."
