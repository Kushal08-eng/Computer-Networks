# Framing in Data Link Layer

## Frame Kya Hai?

**Frame** Data Link Layer pe data transmission ki basic unit hai — bits ka structured group jo actual data ke saath control information (addressing, error detection) bhi carry karta hai.

## Framing Kya Hai?

**Framing** Data Link Layer (DLL) pe perform hoti hai — continuous stream of bits ko manageable aur meaningful units (frames) mein divide karti hai.

| Fayda | Matlab |
|---|---|
| Reliable Transmission | Frames ki wajah se receiver end pe proper processing hoti hai |
| Synchronization | Sender-receiver ke beech timing sync help karta hai |
| Clear Boundaries | Receiver correctly identify kar sakta hai ki ek frame kahan khatam ho raha hai aur dusra kahan shuru |

> **Note**: Framing especially important hai techniques jaise **Time Division Multiplexing (TDM)** mein, jahan data fixed time slots mein bheja jaata hai.

## Kaunsi Technologies Framing Use Karti Hain

Ethernet, Token Ring, aur Frame Relay jaisi Data Link Layer technologies well-defined frame formats use karti hain — proper data identification aur reliable communication ke liye.

## Framing Ke Purposes

- Clear frame boundaries define karta hai taaki receiver har frame correctly identify kar sake
- Control information (addressing, error detection) carry karta hai
- Sender-receiver ke beech synchronization enable karta hai

## Framing Ki Challenges

| Challenge | Matlab |
|---|---|
| **Start/End Detection** | Receiver ko delimiters/flags se frame boundaries correctly identify karni hoti hain |
| **Synchronization** | Sender-receiver ko frame timing pe aligned rehna padta hai, especially high-speed networks mein |
| **Error Handling** | Noise se data/delimiters corrupt ho sakte hain — CRC ya checksum jaise error detection methods use hote hain |
| **Overhead** | Headers/trailers control info add karte hain, but usable bandwidth kam kar dete hain |
| **Efficiency** | Goal hai payload maximize karna aur overhead/processing delays minimize karna |

## Bit Stuffing (Example)

Jab actual data mein ek special pattern (jaise flag bits) accidentally aa jaaye, to confusion avoid karne ke liye extra bit "stuff" ki jaati hai:

```
Data = 011100011110, ED (End Delimiter) = 0111
After bit stuffing -> 011010001101100
```

## Viva One-Liners

- **Q: Frame kya hai?**
 A: Data Link Layer pe data transmission ki basic unit, jisme actual data + control information hoti hai.
- **Q: Framing kis layer pe hoti hai?**
 A: Data Link Layer.
- **Q: Framing ki 2 main challenges kya hain?**
 A: Frame boundaries correctly detect karna, aur sender-receiver ke beech synchronization maintain karna.
