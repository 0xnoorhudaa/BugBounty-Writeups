
# Finding Reflected XSS in 5 Minutes  
This guide explains how to quickly identify **Reflected Cross-Site Scripting (XSS)** vulnerabilities using simple techniques.  

## 🎯 **Target (Example Only)**  
In this example, we tested for **Reflected XSS** on a university website. However, this is for **educational purposes only**. Always follow **responsible disclosure** policies.  

## 🛠 **Steps to Find Reflected XSS**  
1️⃣ **Find Subdomains**  

```

 assetfinder --subs-only example.com | httpprobe | cookieless

```

2️⃣ Test for Reflection

- Input this URL-encoded string to check for reflection:

```

A(<testabcd)

```

- If reflected, replace A with an XSS payload.
3️⃣ Payload Injection
- Modify the input to test XSS:

```

- <script>alert('XSS')</script>

```
