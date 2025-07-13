# 🔐 SentinelHeaders – HTTP Security Headers Scanner

<div align="center">

![SentinelHeaders Logo](https://raw.githubusercontent.com/sneckey0day/SentinelHeaders/main/images/HEADER.png)
---
**Professional HTTP header security assessment for red teams, defenders, and auditors**
[![Live Scan](https://img.shields.io/badge/🌐_Live_Scan-local-00d4aa?style=for-the-badge)](#)
[![GitHub Stars](https://img.shields.io/github/stars/sneckey0day/SentinelHeaders?style=for-the-badge&color=yellow)](https://github.com/sneckey0day/SentinelHeaders/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/sneckey0day/SentinelHeaders?style=for-the-badge&color=red)](https://github.com/sneckey0day/SentinelHeaders/issues)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

*Scan • Score • Secure*
</div>

## 🚀 What is SentinelHeaders?

SentinelHeaders is a powerful, **Python-based CLI tool** that inspects and scores HTTP security headers across web targets. Designed by red teamers for offensive and defensive use, it offers actionable insights and compliance-ready reporting.

### ✨ Key Features

- 🔍 **Comprehensive scanning** with severity levels (CRITICAL → LOW)  
- ⚡ **Bulk multi-threaded scans** for high-volume engagements  
- 📊 **Scoring engine (0–100)** with letter grades (A+ → F)  
- 📝 **Verbose mode** for deep-dive recommendations  
- 🗂️ **CSV reports** ready for compliance and audit docs  
- ⚙️ **Fully configurable** (threads, delays, proxy, User-Agent)  
- 🎨 **Colorized output** (optional `--no-color`)  
- 📚 **Built-in header reference** (`--help-headers`)

---



## 🛠️ Installation

```bash
git clone https://github.com/sneckey0day/SentinelHeaders.git
cd SentinelHeaders
pip install -r requirements.txt
````

---

## 🚀 Usage

### 🔍 Scan a Single URL

```bash
python3 sentinelheaders.py -u https://example.com
```

### 📂 Scan Multiple Targets

```bash
python3 sentinelheaders.py -f targets.txt --threads 10
```

### 📢 Verbose Mode

```bash
python3 sentinelheaders.py -u https://example.com -v
```

### 📊 Export to CSV

```bash
python3 sentinelheaders.py -f targets.txt -o results --threads 5
```

### ⚙️ Custom Threads

```bash
python3 sentinelheaders.py -f targets.txt --threads 15
```

### 🌐 Proxy & User-Agent

```bash
python3 sentinelheaders.py -u https://example.com \
  --proxy http://127.0.0.1:8080 \
  --user-agent "Mozilla/5.0"
```

### 🧾 View Header Reference

```bash
python3 sentinelheaders.py --help-headers
```
![SentinelHeaders Logo](https://raw.githubusercontent.com/sneckey0day/SentinelHeaders/main/images/FILE.png)

---

## 🔍 Headers Checked

| Header                        | Severity | Purpose                                    |
| ----------------------------- | -------- | ------------------------------------------ |
| **Strict-Transport-Security** | CRITICAL | Enforces HTTPS to prevent MITM attacks     |
| **Content-Security-Policy**   | CRITICAL | Mitigates XSS and data injection attacks   |
| **X-Frame-Options**           | HIGH     | Prevents clickjacking via iframe embedding |
| **X-Content-Type-Options**    | HIGH     | Stops MIME-type sniffing vulnerabilities   |
| **Referrer-Policy**           | MEDIUM   | Controls Referer header leakage            |
| **Permissions-Policy**        | MEDIUM   | Regulates browser API access               |
| **Cache-Control**             | MEDIUM   | Prevents caching of sensitive assets       |
| **X-XSS-Protection**          | LOW      | Legacy XSS protection (mostly deprecated)  |

---

## 🤝 Contributing

Contributions are welcome from the security and open-source community:

1. Fork this repository
2. Create a feature branch (`feature/xyz` / `fix/issue123`)
3. Follow PEP‑8 style guidelines
4. Submit a well-documented pull request

Please include detailed descriptions, use cases, and tests wherever possible.

---

## 🪪 License

SentinelHeaders is released under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 🧠 Credits & Palette

<div align="left">
<table>
<tr>
<td align="left" width="50%">
<a href="https://github.com/sneckey0day">
<img src="https://github.com/sneckey0day.png" width="150" height="150" style="border-radius: 50%; border: 3px solid #00d4aa;" alt="Sneckey0Day">
</a>
<br><br>
<h3><a href="https://github.com/sneckey0day" style="text-decoration: none; color: #333;">Sneckey0Day</a></h3>
<p>
<a href="https://github.com/sneckey0day">
<img src="https://img.shields.io/badge/GitHub-sneckey0day-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub">
</a>
<br>
<a href="https://www.linkedin.com/in/sneckey0day/">
<img src="https://img.shields.io/badge/LinkedIn-sneckey0day-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn">
</a>
</p>
</td>

<td align="left" width="50%">
<a href="https://github.com/prash0xd">
<img src="https://github.com/prash0xd.png" width="150" height="150" style="border-radius: 50%; border: 3px solid #00d4aa;" alt="prash0xd">
</a>
<br><br>
<h3><a href="https://github.com/prash0xd" style="text-decoration: none; color: #333;">prash0xd</a></h3>
<p>
<a href="https://github.com/prash0xd">
<img src="https://img.shields.io/badge/GitHub-prash0xd-181717?style=flat-square&logo=github&logoColor=white" alt="">
</a>
<br>
<a href="https://www.linkedin.com/in/prash0xd/">
<img src="https://img.shields.io/badge/LinkedIn-prash0xd-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn">
</a>
</p>
</tr>
</table>
</div>


Built with expertise in red teaming, security tooling, and professional ethics.


## ⚖️ Legal Disclaimer

SentinelHeaders is designed for **authorized testing** and **educational use only**. By using this tool, you confirm that you have proper authorization to scan the provided targets. The authors disclaim responsibility for misuse.
