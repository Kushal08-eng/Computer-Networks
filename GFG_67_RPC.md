# Remote Procedure Call (RPC)

## RPC Kya Hai?

**RPC (Remote Procedure Call)** ek communication protocol/mechanism hai jo ek program ko **dusre computer (remote server) pe koi procedure execute** karne deta hai — bilkul aise jaise wo local function call ho.

> **Analogy**: Jaise tum apne dost ko phone karke bolo "mera kaam kar do" aur wo kaam karke result bhej de — tumhe pata bhi nahi chalta kaam kahan hua, bas result mil jaata hai. RPC bhi complexity hide karta hai — developer normal function call jaisa hi likhta hai, network ka kaam RPC khud handle kar leta hai.

## RPC Kaise Kaam Karta Hai (Steps)

| Step | Kya Hota Hai |
|---|---|
| **1. Client Calls Stub** | Client ek local procedure ("stub") call karta hai, jaise normal function |
| **2. Marshalling** | Stub input parameters ko ek message mein "pack" karta hai |
| **3. Send to Server** | Message network ke through server tak jaata hai |
| **4. Server Stub** | Server ka stub message ko "unpack" karta hai aur actual procedure call karta hai |
| **5. Execution & Return** | Server procedure run karta hai, result wapas bhejta hai |
| **6. Back to Client** | Server stub result bhejta hai, client stub use unpack karke deta hai |

## RPC Ke Types

| Type | Matlab |
|---|---|
| **Callback RPC** | Client aur server dono ek dusre ko call kar sakte hain — interactive applications ke liye useful |
| **Broadcast RPC** | Client ka request sab servers ko broadcast hota hai — jab multiple servers request handle kar sakte hon |
| **Batch-Mode RPC** | Multiple requests group karke ek saath bheji jaati hain — network overhead kam karta hai |

## RPC Ke Advantages

| Advantage | Matlab |
|---|---|
| **Easy Communication** | Normal procedure calls jaisa syntax, samajhna easy |
| **Hidden Complexity** | Network communication ki complexity developer se hidden rehti hai |
| **Flexibility** | Local aur distributed environments dono mein use ho sakta hai |

## RPC Ke Disadvantages

| Disadvantage | Matlab |
|---|---|
| **Limited Parameter Passing** | Sirf value se pass ho sakta hai, pointers nahi |
| **Slower Than Local Calls** | Network communication involve hone se time lagta hai |
| **Vulnerable to Failures** | Network connections, remote machines pe depend karta hai — fail hone ke chances zyada |

## RPC OSI Model Mein Kahan Fit Hota Hai

RPC primarily **Session Layer** se associate hota hai (session establish/manage karne ke liye), but iski functionality **Application Layer** aur kabhi-kabhi **Presentation Layer** tak bhi extend hoti hai. TCP/IP model mein, RPC **Application Layer** ka part maana jaata hai.

## Viva One-Liners

- **Q: RPC ka main kaam kya hai?**
 A: Program ko remote server pe procedure execute karne dena, bilkul local function call jaisa.
- **Q: Marshalling kya hai?**
 A: Parameters/data ko network transmission ke liye byte stream mein convert karna.
- **Q: RPC ka sabse bada disadvantage kya hai?**
 A: Network dependency ki wajah se local calls se slower aur zyada failure-prone hai.
