# Unix Terminal:

### Extract subdomains and check if it's active

```
sublist3r -d scope.com -o extracted_subdomains.txt;cat extracted_subdomains.txt | httpx -silent -o verified_subdomains.txt;cat verified_subdomains.txt | awk -F[/:] '{print $4}' | anew > subdomains.txt;rm verified_subdomains.txt extracted_subdomains.txt

cat domains.txt | assetfinder -subs-only | httpx -silent | awk -F[/:] '{print $4}' | tee -a subdomains.txt
```

### Extract subdomains (manually)

```
for scope in $(cat domains.txt);do curl "https://web.archive.org/cdx/search/cdx?url=*.$scope/*&output=text&fl=original&collapse=urlkey" | awk -F[/:] '{print $4}' | anew | sed -e 's/:80//' | httpx -silent | awk -F[/:] '{print $4}' | tee -a subdomains.txt;done
```
