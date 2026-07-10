# Structure of the Network

## Internet Ka Overall Structure

Internet ek single network nahi hai — ye **networks ka network** hai, jisme alag-alag layers/hierarchy hoti hai.

## Key Components

### 1. End Systems (Hosts)
Tumhare devices — laptop, phone, server — jo actual data generate/consume karte hain.

### 2. Access Network
Wo network jo end system ko internet se connect karta hai — jaise tumhara home WiFi, mobile data (4G/5G), ya office LAN.

### 3. ISP (Internet Service Provider)
Company jo internet connection provide karti hai (jaise Jio, Airtel). ISPs khud bhi hierarchy mein organized hote hain:

| Tier | Matlab |
|---|---|
| **Tier 1 ISP** | Sabse bade, poori duniya ka backbone (jaise AT&T, NTT) — kisi aur ko paisa nahi dete peering ke liye |
| **Tier 2 ISP** | Regional providers, kuch Tier 1 se connect, kuch khud peer karte hain |
| **Tier 3 ISP** | Local/last-mile providers jo directly consumers ko connection dete hain |

### 4. Core Network (Backbone)
High-speed routers aur cables jo bade traffic ko carry karte hain (including submarine cables) — internet ka "highway system".

## Structure Ka Flow (Simple)

```
Tumhara Device → Access Network (WiFi/Mobile) → Local ISP (Tier 3) 
→ Regional ISP (Tier 2) → Backbone (Tier 1) → Destination Server
```

> **Analogy**: Jaise tum apni gully se mukhya road pe aate ho, phir highway pe, phir dusre city ki gully tak pahunchte ho — internet ka data bhi chhoti se badi network hierarchy se hoke travel karta hai.

## Viva One-Liner

> "Internet ek hierarchical structure hai — end systems, access networks, aur multiple tiers ke ISPs milke poora network banate hain."
