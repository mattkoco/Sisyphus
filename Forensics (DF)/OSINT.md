# OSINT (Rarer category to be found in CTF)

## Introduction
Open Source Intelligence (OSINT) involves gathering information from publicly available sources. It's commonly used in CTF challenges to uncover details about individuals, organizations, or systems.

## Key OSINT Techniques

### People Search
- **Search Engines:**
  - Use Google, Bing, DuckDuckGo with advanced search operators.
  - Example: `site:linkedin.com "John Doe"`

- **Social Media:**
  - Platforms: Facebook, Twitter, LinkedIn, Instagram
  - Look for: Profiles, posts, comments, connections

- **People Search Engines:**
  - Pipl, Spokeo, PeekYou, BeenVerified

### Domain and Website Information
- **Whois Lookup:**
  - Tools: `whois [domain]`
  - Websites: Whois.net, ICANN WHOIS

- **DNS Information:**
  - Tools: `nslookup`, `dig`
  - Websites: MXToolbox, DNSdumpster

- **Website Analysis:**
  - Tools: Wappalyzer, BuiltWith
  - Look for: Technologies used, subdomains, metadata

### Email Address Search
- **Email Verification:**
  - Tools: Hunter.io, VerifyEmailAddress.org
  - Check: Validity, associated social media accounts

- **Email Breaches:**
  - Websites: Have I Been Pwned, Dehashed

### IP Address Information
- **Geolocation:**
  - Tools: IPinfo.io, MaxMind GeoIP
  - Look for: Location, ISP, organization

- **Open Ports:**
  - Tools: Shodan, Censys, Nmap
  - Look for: Open services, vulnerabilities

### Document Metadata
- **Metadata Extraction:**
  - Tools: ExifTool, FOCA, PDF-XChange Viewer
  - Look for: Author, creation date, software used

### Image Analysis
- **Reverse Image Search:**
  - Tools: Google Images, TinEye, Yandex
  - Use: Identify origins, similar images

- **Image Metadata:**
  - Tools: ExifTool, Jeffrey’s Image Metadata Viewer
  - Look for: Camera details, geotags, timestamps

## Tools and Resources

### General OSINT Tools
- **Maltego:** Graphical link analysis tool.
- **theHarvester:** Email, subdomain, and name search tool.
- **Recon-ng:** Web reconnaissance framework.
- **SpiderFoot:** Automated OSINT tool.

### Search Engine Operators
- **Google Dorks:**
  - `site:example.com filetype:pdf`
  - `intitle:"index of" "parent directory"`
  - `inurl:admin login`

### Useful Websites
- **Shodan:** Search engine for Internet-connected devices.
- **Censys:** Internet-wide search engine.
- **Wayback Machine:** Internet Archive’s digital archive of the web.

## Common OSINT Challenges in CTFs
- **Finding hidden information:** Use search engines and social media to find hidden or deleted information.
- **Connecting the dots:** Use link analysis tools to connect disparate pieces of information.
- **Metadata analysis:** Extract and analyze metadata from documents and images.
- **Domain investigation:** Investigate domains and subdomains for useful information.

## References
- [OSINT Framework](https://osintframework.com/)
- [Google Hacking Database](https://www.exploit-db.com/google-hacking-database)
- [Awesome OSINT](https://github.com/jivoi/awesome-osint)
- [OSINT Techniques](https://www.osinttechniques.com/)

