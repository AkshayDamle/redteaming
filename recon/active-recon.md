# Active Recon Notes

## Port Scanning
```bash
# Fast scan first
nmap -T4 -F target.com

# Full TCP
nmap -sS -p- -T4 --open target.com -oA full_tcp

# Service + version
nmap -sV -sC -p <open_ports> target.com -oA services

# UDP (slow)
nmap -sU --top-ports 100 target.com
```

## Web Enumeration
```bash
# Directory brute force
ffuf -u https://target.com/FUZZ -w /usr/share/wordlists/dirb/common.txt -mc 200,301,302,403

# Vhost discovery
ffuf -u https://target.com -H "Host: FUZZ.target.com" -w subdomains.txt -fs <size>
```

## Common Ports to Note
| Port | Service |
|------|---------|
| 21   | FTP     |
| 22   | SSH     |
| 25   | SMTP    |
| 80/443 | HTTP/S |
| 445  | SMB     |
| 3306 | MySQL   |
| 5432 | PostgreSQL |
| 6379 | Redis   |
| 8080 | Alt HTTP |
