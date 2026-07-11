# NetWare Core Protocol (NCP)

## NCP Kya Hai?

**NCP (NetWare Core Protocol)** **Novell NetWare** operating system ka core protocol hai — file aur print services ke liye use hota hai, client aur server ke beech communication ke liye.

## NCP Kaise Kaam Karta Hai

- **Client-Server model** follow karta hai — clients (workstations) NCP requests bhejte hain NetWare server ko
- Server requests process karta hai — file access, printing, authentication jaisi services deta hai
- Request-response based protocol hai

## NCP Ke Use Cases

| Use Case | Matlab |
|---|---|
| **File Services** | Files create, read, write, delete karna network ke through |
| **Print Services** | Network printers tak access dena |
| **Directory Services** | eDirectory (Novell ka directory service) ke saath integration — user info, authentication |
| **Authentication** | Login credentials verify karna |

## NCP Ki Position

NCP Session aur Presentation Layer ke concepts ko touch karta hai — session establish karta hai (client-server communication ke liye) aur data ko ek consistent format mein present karta hai, jo Novell NetWare environment ke saath compatible ho.

## NCP Ki Relevance Today

NCP ek **legacy protocol** hai — Novell NetWare aaj kal itna common nahi hai jitna 1990s-2000s mein tha. Modern networks mostly **SMB (Windows)** ya **NFS (Unix/Linux)** jaise protocols use karte hain file sharing ke liye. But NCP abhi bhi kuch legacy enterprise environments mein use hota hai jo purane Novell infrastructure pe based hain.

## Viva One-Liners

- **Q: NCP kis operating system ke liye develop kiya gaya tha?**
 A: Novell NetWare.
- **Q: NCP kis type ki services provide karta hai?**
 A: File services aur Print services.
- **Q: NCP aaj kal kitna common hai?**
 A: Legacy protocol hai — modern networks mein SMB/NFS jaise protocols zyada common hain.
