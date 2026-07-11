# Transmission Media

## Transmission Media Kya Hai?

**Transmission Media** wo physical ya wireless communication channel hai jo data signals ko ek device se dusre tak carry karta hai — network ke devices ke beech connectivity ka fundamental pathway.

**Medium Choose Karte Waqt Factors:**

| Factor | Matlab |
|---|---|
| Transmission Distance | Kitni dur tak data bhejna hai |
| Data Transfer Speed | Bandwidth kitni chahiye |
| Interference/Noise | Kitna susceptible hai disturbance ke liye |
| Cost & Installation | Kitna expensive/complex hai lagana |

Transmission media 2 broad types mein classify hoti hai: **Guided Media** aur **Unguided Media**.

---

## Guided Media (Wired)

Data signals **physical cables** ke through travel karte hain — signal ek fixed route pe confined/guided hota hai.

| Feature | Detail |
|---|---|
| Types | Twisted Pair, Coaxial, Optical Fiber |
| Data Rate | Wireless se generally zyada |
| Security | Better (physical connectivity ki wajah se) |

### 1. Twisted Pair Cable

Do individually insulated copper conductors ko helical pattern mein twist kiya jaata hai — interference aur crosstalk kam karne ke liye.

**(a) Unshielded Twisted Pair (UTP)**: Koi extra metallic shielding nahi hoti.

| Advantages | Disadvantages |
|---|---|
| Sabse sasta guided media | STP se kam performance/capacity |
| Install/maintain karna easy | Limited distance (attenuation) |
| Short distances pe high data rate | Noise/EMI ke liye zyada susceptible |

**(b) Shielded Twisted Pair (STP)**: Extra metallic shielding layer hoti hai — better EMI protection.

| Advantages | Disadvantages |
|---|---|
| UTP se better performance high data rates pe | UTP se costly |
| EMI aur crosstalk kaafi kam | Installation complex |
| Noisy environments mein reliable | Bulkier, kam flexible |

### 2. Coaxial Cable

Central copper conductor + insulating layer + metallic shielding + outer jacket.

| Advantages | Disadvantages |
|---|---|
| Twisted pair se zyada bandwidth | Twisted pair se costly |
| Better signal quality/reliability | Grounding zaroori |
| FDM se multiple channels support | Bulky, kam flexible |
| EMI se kam affected | Physically tap ho sakti hai (security risk) |

### 3. Optical Fiber Cable

Glass/plastic core ke through **light signals** ki form mein data transmit karta hai (total internal reflection principle se).

| Advantages | Disadvantages |
|---|---|
| Bahut high bandwidth, data-carrying capacity | Installation/maintenance complex (precise splicing) |
| Lightweight, compact | High initial cost |
| Low signal attenuation, long-distance ke liye best | Copper cables se fragile |
| EMI-immune, electrical noise se unaffected | — |
| Corrosion-resistant | — |

**Applications**: Medical (endoscopy), Defense/Aerospace, Internet backbones/undersea cables, Industrial/Automotive.

---

## Unguided Media (Wireless)

**Electromagnetic waves** use karke bina physical medium ke data transmit hota hai — signals free space (air/vacuum) se propagate hote hain.

| Feature | Detail |
|---|---|
| Propagation | Air/free space se |
| Security | Kam (broadcast nature ki wajah se) |
| Use | Long-distance communication ke liye suitable |

### 1. Radio Waves
Easily generate ho sakte hain, buildings/obstacles ke through propagate ho sakte hain — line-of-sight zaroori nahi.

- **Frequency**: 3 kHz – 300 GHz
- **Types**: Shortwave (AM radio), VHF (FM/TV), UHF (TV, mobile)
- **Applications**: AM/FM radio, television, cordless phones

### 2. Microwaves
**Line-of-sight** communication chahiye — antennas properly aligned hone chahiye.

- **Frequency**: 1 GHz – 300 GHz
- **Applications**: Mobile communication, satellite links, TV distribution

| Advantages | Disadvantages |
|---|---|
| Cables lagane se cost-effective | Bina encryption ke less secure |
| Land acquisition ki zaroorat nahi | Weather (rain/fog) se affect hota hai |
| Difficult terrains/oceans ke liye suitable | Obstacles se affected (line-of-sight zaroori) |
| High data rates support | Antenna design/installation costly |

### 3. Infrared
Short-range wireless communication ke liye use hota hai, solid obstacles ke through penetrate nahi kar sakta.

- **Frequency**: 300 GHz – 400 THz
- **Applications**: TV remotes, wireless keyboards/mice, printers

### Comparison: Radio vs Microwave vs Infrared

| Feature | Radio Waves | Microwaves | Infrared |
|---|---|---|---|
| Direction | Omnidirectional | Highly directional | Directional (LOS chahiye) |
| Obstacle Penetration | Buildings ke through easily | Poor, LOS zaroori | Penetrate nahi karta |
| Frequency | 3 kHz – 300 GHz | 1 GHz – 300 GHz | 300 GHz – 400 THz |
| Security | Low | Medium (encryption possible) | Relatively high but limited range |
| Cost | Low to Moderate | High | Low |

---

## Causes of Transmission Impairment

Transmission ke dauran signal loss/distortion, jo errors ya quality degradation cause karta hai.

| Cause | Matlab |
|---|---|
| **Attenuation** | Signal strength travel karte waqt kam hoti jaati hai (resistance/energy loss ki wajah se) — amplifiers (analog) ya repeaters (digital) se fix hota hai |
| **Distortion** | Transmitted signal ki shape change ho jaati hai (composite signals mein alag frequencies alag speed se travel karti hain) |
| **Noise** | Unwanted electrical/electromagnetic signals jo original signal ko corrupt kar sakte hain (thermal noise, crosstalk, impulse noise) |

## Factors for Designing Transmission Media

| Factor | Matlab |
|---|---|
| **Bandwidth** | Medium kitni frequency range support karta hai — jyada bandwidth = jyada data rate |
| **Transmission Impairment** | Received signal transmitted signal se kitna different hai |
| **Interference** | External sources se signal disturbance |

## Applications Summary

| Media | Application |
|---|---|
| UTP | LAN, telephones |
| STP | Industrial networks, high interference environments |
| Optical Fiber | Long-distance, internet backbones |
| Coaxial | Cable TV, broadband, CCTV |
| Radio | Wireless communication, AM/FM, mobile phones |
| Infrared | Remote controls, short-range communication |
| Microwave | Satellite communication, radar, long-distance links |

## Viva One-Liners

- **Q: Guided aur Unguided media mein basic difference?**
 A: Guided media physical cables use karti hai (twisted pair, coaxial, fiber), Unguided media electromagnetic waves se wireless transmit karti hai.
- **Q: Optical Fiber sabse zyada kis cheez ke liye best hai?**
 A: High bandwidth aur long-distance, low-attenuation communication ke liye.
- **Q: Microwave communication ke liye kya zaroori hai?**
 A: Line-of-sight — transmitting aur receiving antennas properly aligned hone chahiye.
- **Q: Attenuation kya hai?**
 A: Signal ki strength ka travel karte waqt kam hona.
