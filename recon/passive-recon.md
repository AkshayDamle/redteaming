# Passive Recon Checklist

## OSINT
- [ ] WHOIS lookup (`whois target.com`)
- [ ] DNS enumeration (`dig`, `dnsx`, `subfinder`)
- [ ] Reverse IP lookup
- [ ] Certificate transparency logs (`crt.sh`)
- [ ] Shodan/Censys for exposed services
- [ ] Google dorks (`site:`, `filetype:`, `inurl:`)

## Subdomain Discovery
```bash
subfinder -d target.com -o subs.txt
amass enum -passive -d target.com
dnsx -l subs.txt -resp -o live.txt
```

## Email Harvesting
- theHarvester
- hunter.io
- LinkedIn scraping

## Tech Stack Fingerprinting
- Wappalyzer
- whatweb
- BuiltWith
