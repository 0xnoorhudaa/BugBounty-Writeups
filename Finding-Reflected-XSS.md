🔥 Contoh File untuk GitHub (README.md atau .md file lain)
Buat file Finding-Reflected-XSS.md di dalam repositori GitHub-mu.

Contoh Isi File
md
Salin
Edit
# Finding Reflected XSS in 5 Minutes  
This guide explains how to quickly identify **Reflected Cross-Site Scripting (XSS)** vulnerabilities using simple techniques.  

## 🎯 **Target (Example Only)**  
In this example, we tested for **Reflected XSS** on a university website. However, this is for **educational purposes only**. Always follow **responsible disclosure** policies.  

## 🛠 **Steps to Find Reflected XSS**  
1️⃣ **Find Subdomains**  
   ```sh
   assetfinder --subs-only example.com | httpprobe | cookieless


### Scan ports on a host quickly

```
SCOPE=192.168.0.0/24;RPORT=22,80,443;rustscan -b 500 -a $SCOPE -p $RPORT | grep "Open $SCOPE[0-9]*" | tee -a ports_scanned.txt
