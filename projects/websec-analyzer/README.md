# 🔍 WebSec Analyzer
A Python-based tool for analyzing the security posture of a domain, covering HTTP headers, TLS configuration, DNS records, cookies, and potential exposure points.

---
### Overview
**WebSec Analyzer** is a lightweight tool that analyzes the security posture of a domain from different angles. It evaluates aspects such as web security headers, TLS/SSL configuration, cookie security, DNS records (including SPF and DMARC), WHOIS information, and the exposure of sensitive files.

This project was developed as part of a security course in my Computer Systems Engineering program. It focuses on understanding how a domain is exposed from the outside and identifying common security misconfigurations.

At the same time, it reflects my interest in Cloud Security, as I aim to build practical skills in analyzing real-world systems and their attack surface.

---
### Features

- Multi-module security analysis
- Interactive CLI (choose what to scan)
- JSON report generation
- Detection of missing security controls
- Exposure checks for sensitive files

---
### Project Structure
```
websec-analyzer/ 
    ├── analyzer.py 
    ├── README.md 
    ├── .gitignore 
    └── reports/      # Generated reports (not tracked by git)
```

---
### Installation
Clone the repository:
```
git clone https://github.com/oscaarlab/oscaarlab.git
cd oscaarlab/projects/websec-analyzer
```
Install dependencies:
```
pip install requests dnspython python-whois
```

---
### Usage
Run the analyzer:
```
python analyzer.py example.com
```
Then select what you want to analyze:

1. Response Headers
2. Security Headers
3. Cookie Analysis
4. TLS Analysis
5. DNS Records
6. WHOIS Information
7. Special Files
8. All

You can select: 
- A single option: `1`
- Multiple options (comma-separated): `1,4,5`
- Or run a full analysis: `8`

---
### Output
The tool can generate a JSON report:
```
reports/example_com_analysis.json
```

This includes:
- Headers
- TLS details
- DNS records
- Cookie analysis
- Security findings

---
### Example Use Cases
- Perform a quick security baseline assessment of any public-facing domain
- Support reconnaissance during penetration testing engagements
- Identify missing security headers and weak TLS configurations
- Analyze DNS records to detect misconfigurations (SPF, DMARC, etc.)
- Discover exposed sensitive files such as .env, backups, or config files
- Learn and practice web, network, and application security concepts
- Build and extend custom security tooling using Python
- Generate structured reports for documentation or further analysis

---
### Disclaimer
This tool is intended for educational and authorized testing purposes only.
Do not use it against systems you do not own or have permission to analyze.

---
### Skills Demonstrated
- Python scripting for security tooling
- TLS and certificate inspection
- DNS analysis (SPF, DMARC)
- Web security headers evaluation
- Basic OSINT techniques