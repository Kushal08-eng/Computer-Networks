# Functions of Session Layer

## Session Layer Ke Detailed Functions

Session Layer, Presentation Layer se aaya data handle karti hai, aur kai important tasks perform karti hai:

### 1. Session Establishment
Sabse basic aur important function — communicating parties ke beech ek **connection (session)** establish karta hai. Ye connection files transfer, remote login, ya communication ko organized aur reliable tareeke se karne mein help karta hai.

### 2. Dialogue Control
Decide karta hai communication kis mode mein hogi:

| Mode | Matlab |
|---|---|
| **Simplex** | Sirf ek direction mein data flow |
| **Half-Duplex** | Dono directions, but ek time pe ek |
| **Full-Duplex** | Dono directions simultaneously |

Session Layer ye bhi manage karta hai ki kis waqt kis party ka "turn" hai data bhejne ka.

### 3. Synchronization
Long data transfers mein, Session Layer **checkpoints (synchronization points)** insert karti hai:

| Term | Matlab |
|---|---|
| **Synchronization Point** | Ek "save point" jahan tak data safely transfer ho chuka hai |
| **Restart** | Failure hone pe, poori transfer restart karne ki jagah, last synchronization point se resume kar sakte hain |

> **Analogy**: Video game mein "checkpoint" jaisa — agar beech mein game crash ho jaaye, to shuru se nahi, last checkpoint se resume ho jaata hai.

### 4. Session Management
Session ko maintain karna — including error detection/recovery jab transport connection fail ho jaaye. Agar underlying connection fail ho, session layer usse **re-establish** karne ki koshish kar sakti hai, taaki session continue ho sake.

## Session Layer Ke Protocols (Recap)

| Protocol | Kaam |
|---|---|
| PPTP | VPN tunnels |
| PAP | Authentication |
| RPCP | Remote procedure calls |
| SDP | RDMA-based socket communication |

## Viva One-Liners

- **Q: Session Layer ka sabse basic function kya hai?**
 A: Communicating parties ke beech session (connection) establish karna.
- **Q: Synchronization points ka fayda kya hai?**
 A: Failure hone pe, poori transfer restart karne ki jagah, last checkpoint se resume kar sakte hain.
- **Q: Dialogue control kya decide karta hai?**
 A: Communication simplex, half-duplex, ya full-duplex mode mein hogi, aur kiska turn hai data bhejne ka.
