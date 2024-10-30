## Recon
```bash
subfinder -d example.com -o subfinder:example.com -all # ProjectDiscovery Chaos

httpx -l subfinder:example.com -sc -cl -ct -title -fc 301,302,307,308 -silent | awk -f ~/MyAwkScripts/httpx-format-general.awk | sort

httpx -l subfinder:example.com -sc -ct -fr -silent | awk -f ~/MyAwkScripts/httpx-format-redirects.awk | sort

ffuf -w wordlist.txt -u https://FUZZ.example.com

ffuf -w wordlist.txt -u https://www.example.com -H "Host: FUZZ.example.com"

katana -u scope.txt -o katana.txt -d 5 -jc
```
