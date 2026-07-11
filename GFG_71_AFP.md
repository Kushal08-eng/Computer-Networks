# Apple Filing Protocol (AFP)

## AFP Kya Hai?

**AFP (Apple Filing Protocol)** ek network protocol hai jo **macOS** ke liye file-sharing services deta hai — clients ko servers ke files access karne deta hai, jaise wo local ho.

> AFP ek Application aur Session layer protocol hai (kuch classifications mein Presentation Layer pe bhi consider kiya jaata hai — file representation/formatting ki wajah se).

## AFP Ki Key Features

| Feature | Matlab |
|---|---|
| **Unicode File Names Support** | Alag-alag languages ke file names support karta hai |
| **POSIX Support** | Portable Operating System Interface — Unix-jaise permission model deta hai |
| **ACL Permissions** | Access Control Lists — decide karta hai kaun kya kar sakta hai (read, write, delete) |
| **Resource Fork & Data Fork** | Structured data (Resource Fork) aur unstructured data (Data Fork) dono ke liye storage deta hai |
| **TCP/IP aur AppleTalk Support** | Dono protocols se communicate kar sakta hai |

## AFP Ke Commands (Examples)

- Create Directory
- Close Directory
- Copy File
- Delete File
- Close Volume

## AFP Ke Advantages

| Advantage | Matlab |
|---|---|
| **Security** | Advanced file-locking mechanisms se hazaarnak files ka unauthorized access limit hota hai |
| **Cross-Platform Support** | Windows aur Novell NetWare jaise systems mein bhi AFP support add kiya ja sakta hai |
| **Efficient File Sharing** | macOS environments mein fast, native file sharing |

## AFP Ka Historical Context

- Pehle **AFP macOS ka primary file-sharing protocol** tha
- macOS 10.9 (Mavericks) ke baad, **SMB (Server Message Block)** primary protocol ban gaya
- Newer macOS versions (Big Sur onwards) mein AFP server support **remove** ho chuka hai — legacy protocol ban gaya hai

## Viva One-Liners

- **Q: AFP kis operating system ke liye design kiya gaya tha?**
 A: macOS (Apple ke devices).
- **Q: AFP ne kisse apni jagah replace ki modern macOS mein?**
 A: SMB (Server Message Block).
- **Q: Resource Fork aur Data Fork mein difference?**
 A: Resource Fork structured data (jaise icons, metadata) store karta hai, Data Fork unstructured actual file data store karta hai.
