# HTTP Methods (GET, POST, PUT, DELETE)

## HTTP Methods Kya Hain?

HTTP Methods batate hain client server se **kya action** perform karna chahta hai.

## Main Methods

| Method | Kaam | Example |
|---|---|---|
| **GET** | Data **fetch/read** karna | Webpage load karna, list of users leke aana |
| **POST** | Naya data **create** karna | Naya user register karna, form submit karna |
| **PUT** | Existing data **completely update** karna | Poora user profile update karna |
| **PATCH** | Existing data **partially update** karna | Sirf email change karna |
| **DELETE** | Data **delete** karna | User account delete karna |

> **Analogy**: Socho ek library ka system —
> - **GET** = kitab padhna (sirf dekhna, kuch change nahi)
> - **POST** = nayi kitab library mein add karna
> - **PUT** = poori kitab ki details replace karna
> - **PATCH** = sirf kitab ka title update karna
> - **DELETE** = kitab ko library se hata dena

## GET vs POST (Common Confusion)

| GET | POST |
|---|---|
| Data URL mein visible hota hai (query params) | Data body mein bheja jaata hai (hidden) |
| Cache ho sakta hai | Cache nahi hota generally |
| Sensitive data ke liye use nahi karna chahiye | Sensitive data (password) bhejne ke liye better |
| Idempotent (baar-baar call karne se same result) | Har call se naya data create ho sakta hai |

## PUT vs PATCH

| PUT | PATCH |
|---|---|
| Poora resource replace karta hai | Sirf specific fields update karta hai |
| Idempotent | Idempotent ho sakta hai but partial update focus |

## Viva One-Liners

- **Q: GET aur POST mein basic difference?**
 A: GET data fetch karta hai (read-only), POST naya data create karta hai.
- **Q: PUT aur PATCH mein difference?**
 A: PUT poora resource replace karta hai, PATCH sirf specific part update karta hai.
