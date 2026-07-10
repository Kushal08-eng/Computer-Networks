# Checksum

## Checksum Kya Hai?

**Checksum** ek error-detection technique hai jo check karta hai ki data transmission ke dauran **corrupt** to nahi hua.

> **Analogy**: Socho tum apne dosto ko ek list of numbers bhejte ho aur unka total (sum) bhi bata dete ho. Receiver apni taraf se bhi numbers add karke check karega — agar total match nahi hua, matlab kahin galti ho gayi.

## Kaise Kaam Karta Hai

1. **Sender**: Data ke sabhi bits/bytes ka ek mathematical calculation karta hai aur ek "checksum value" nikalta hai — usse data ke saath bhej deta hai
2. **Receiver**: Wahi calculation apni taraf se karta hai received data pe
3. Agar dono checksum values **match** hui → data sahi hai
4. Agar **match nahi** hui → data corrupt ho gaya, dobara bhejne ki request hoti hai

## Kyun Zaroori Hai

Network transmission ke dauran noise, interference, ya hardware issues se data ke bits change ho sakte hain — checksum in errors ko detect karne mein help karta hai.

## Checksum Ka Use

| Layer | Use |
|---|---|
| Transport Layer (TCP/UDP) | Header + Data ka checksum verify karta hai |
| IP Layer | IP header ka checksum verify karta hai |

## Limitation

Checksum sirf **error detect** kar sakta hai, **fix** nahi kar sakta — agar mismatch mila to poora packet firse maangna padta hai (retransmission).

## Viva One-Liners

- **Q: Checksum ka kaam kya hai?**
 A: Data transmission ke dauran errors/corruption detect karna.
- **Q: Checksum mismatch hone pe kya hota hai?**
 A: Packet ko corrupt maan liya jaata hai aur retransmission request hoti hai.
