# Multipurpose Internet Mail Extension (MIME) Protocol

## MIME Kya Hai?

**MIME (Multipurpose Internet Mail Extensions)** ek standard hai jo email messages ke format ko **extend** karta hai — sirf plain text se aage, images, audio, video, aur attachments jaisa multimedia content bhi carry karne deta hai.

> Bell Communications ne 1991 mein introduce kiya tha.

## MIME Kyun Zaroori Hai

**SMTP (Simple Mail Transfer Protocol)** ki limitation:

| Limitation | Matlab |
|---|---|
| Sirf 7-bit NVT ASCII format | Non-English languages (French, Chinese, Japanese) support nahi karta |
| Binary files nahi bhej sakta | Images, audio, video jaise files nahi bhej sakta |

MIME in limitations ko solve karta hai — non-ASCII data ko encode karke SMTP ke through safely bhejta hai.

## MIME Kaise Kaam Karta Hai (Flow)

1. User non-ASCII format (jaise image ya doosri language) mein email compose karta hai
2. **MIME** us data ko **7-bit NVT ASCII** format mein convert karta hai
3. Message SMTP ke through transfer hota hai
4. Receiver ki taraf, MIME wapas data ko **original format** mein convert kar deta hai
5. Receiver ka email client attachment/content correctly display karta hai

## MIME Email Ke Key Components

| Component | Kaam |
|---|---|
| **MIME-Version** | MIME version specify karta hai (commonly 1.0) |
| **Content-Type** | Content ka type batata hai (text/plain, image/jpeg, audio/mpeg, etc.) |
| **Content-Transfer-Encoding** | Content kaise encode hua hai (base64, quoted-printable) |
| **Content-Disposition** | Content inline hai ya attachment |
| **Content-ID** | Embedded objects (jaise inline images) ka unique identifier |

## MIME Ke Fayde

| Fayda | Matlab |
|---|---|
| **Multiple Data Types** | Text, audio, video, images, application files sab bhej sakta hai |
| **Multilingual Support** | Hindi, French, Japanese, Chinese jaisi languages support karta hai |
| **Rich Formatting** | HTML/CSS ke saath customized emails |
| **Multipart Messages** | Boundary separators se ek email mein multiple parts (text + images + attachments) handle karta hai |

## S/MIME (Bonus)

**S/MIME (Secure/Multipurpose Internet Mail Extensions)** MIME ka upgraded, **secure** version hai — digital signatures aur encryption add karta hai (asymmetric cryptography use karke), email authenticity aur confidentiality ensure karne ke liye.

## Viva One-Liners

- **Q: MIME kis protocol ki limitation solve karne ke liye banaya gaya?**
 A: SMTP — jo sirf 7-bit ASCII text support karta tha, multimedia/non-English content nahi.
- **Q: MIME email data ko kis format mein convert karta hai transmission ke liye?**
 A: 7-bit NVT ASCII format.
- **Q: S/MIME, MIME se kaise different hai?**
 A: S/MIME encryption aur digital signatures add karta hai — secure email communication ke liye.
