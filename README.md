# rcon

> A simple reconnaissance workflow for Bug Bounty, VDP, and Penetration Testing.

`rcon` is a Bash script that automates common reconnaissance tasks by combining multiple open-source security tools into a single workflow. Instead of running each tool manually, `rcon` executes them in sequence and stores the results in an organized directory structure.

The goal is to simplify repetitive reconnaissance while keeping the workflow transparent and easy to customize.

---

## Features

- Automated reconnaissance workflow
- Subdomain enumeration
- DNS resolution
- HTTP probing
- URL collection
- Historical URL gathering
- Web crawling
- JavaScript discovery
- Organized output directory
- Easy to modify
- Easy to extend

---

## Workflow

```
Targets
   │
   ▼
Subdomain Enumeration
   │
   ▼
DNS Resolution
   │
   ▼
HTTP Probing
   │
   ├─────────────┐
   ▼             ▼
 Crawling   Historical URLs
   │             │
   └──────┬──────┘
          ▼
     URL Collection
          │
          ▼
 JavaScript Discovery
          │
          ▼
     Organized Results
```

---

## Requirements

`rcon` uses existing open-source tools. Install them before running.

Examples:

- subfinder
- dnsx
- httpx
- katana
- gau
- waybackurls
- hakrawler
- anew
- jq
- curl

Additional tools may be required depending on the enabled modules.

---

## Installation

```bash
git clone https://github.com/ayodyadsr/rcon.git
cd rcon
chmod +x rcon
```

---

## Usage

Single target

```bash
./rcon example.com
```

Multiple targets

```bash
./rcon targets.txt
```

---

## Output

```
recon_YYYYMMDD_HHMMSS/

├── subdomains/
├── http/
├── urls/
├── javascript/
├── screenshots/
├── reports/
└── logs/
```

---

## Philosophy

`rcon` does not attempt to replace existing reconnaissance tools.

Instead, it focuses on:

- Reducing repetitive manual work
- Keeping reconnaissance organized
- Providing a simple and customizable workflow
- Making it easy to integrate new tools

---

## Roadmap

- [ ] Automatic dependency detection
- [ ] Configuration file
- [ ] Resume previous scan
- [ ] Parallel module execution
- [ ] Docker support
- [ ] Better reporting

---

## License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.

See the [LICENSE](LICENSE) file for details.
