# 🔍 Advanced OSINT Username Scanner  
**A high-performance OSINT username scanner for 55+ platforms — powered by async Python, Playwright, HTTP caching, rate limiting, and interactive investigation graphs.**

<p align="left">
  <img src="https://img.shields.io/badge/Language-Python%203.11+-blue?logo=python" />
  <img src="https://img.shields.io/badge/License-MIT-green" />
  <img src="https://img.shields.io/badge/OSINT-Tool-orange?logo=target" />
  <img src="https://img.shields.io/badge/Async-Enabled-success" />
</p>

---

## 📌 Table of Contents
- [Introduction](#introduction)  
- [Key Features](#key-features)  
- [Tech Stack](#tech-stack)  
- [Architecture Overview](#architecture-overview)  
- [Screenshots / Preview](#screenshots--preview)  
- [Installation](#installation)  
- [Usage](#usage)  
  - [CLI](#cli)  
  - [Web Interface](#web-interface)  
- [Performance](#performance)  
- [Ethical Usage](#ethical-usage)  
- [Project Structure](#project-structure)  
- [Roadmap](#roadmap)  
- [Contributing](#contributing)  
- [License](#license)

---

## 🧠 Introduction
This tool performs **mass parallel username scanning** across 55+ platforms using modern asynchronous Python.  
It is designed for:

- Cybersecurity professionals  
- OSINT investigators  
- Threat analysts  
- Researchers  
- People checking their digital footprint  

Powered by `asyncio`, `aiohttp`, `Playwright`, caching, and rate limiting — it gives **fast & ethical OSINT results** with rich visualizations.

---

## 🚀 Key Features

### ⚡ 1. Fully Asynchronous Scanning  
55+ platforms scanned within **15–30 seconds** using `asyncio` + `aiohttp`.

---

### 🗄️ 2. SQLite HTTP Caching  
80% faster re-scans • 24-hour caching • Reduced server load.

---

### 🚦 3. Per-Domain Rate Limiting  
Avoids blocks & throttling using:  
`aiolimiter → 2 requests/sec per domain`.

---

### 🌐 4. Playwright JS Rendering  
Supports React/Vue/SPA websites requiring JavaScript rendering.

---

### 🧩 5. Rich CLI Interface  
Clean tables, colors, statistics, and live progress indicators.

---

### 💻 6. Flask Web UI  
User-friendly web dashboard with real-time scanning and exports.

---

### 🕸️ 7. Interactive Relationship Graphs  
Using `NetworkX + PyVis`, generates HTML visualizations showing patterns across accounts.

---

## 🛠 Tech Stack

| Component | Tech |
|----------|------|
| Language | Python 3.11+ |
| Async HTTP | aiohttp |
| Cache | aiohttp-client-cache (SQLite) |
| Rate Limit | aiolimiter |
| JS Rendering | Playwright |
| CLI | rich |
| Web UI | Flask |
| Graphs | NetworkX + PyVis |
| Image Matching | Pillow + imagehash |

---

## 🏗 Architecture Overview

             ┌─────────────────────┐
             │    User Input       │
             └─────────┬───────────┘
                       │ username
                       ▼
            ┌────────────────────────┐
            │ Async Engine (asyncio) │
            └─────────┬──────────────┘
                      │ tasks
     ┌────────────────┼───────────────────┐
     ▼                ▼                   ▼

---

## 🖼 Screenshots / Preview  
*(Add screenshots later)*  

Coming soon...

---

## 🛠 Installation

### Clone the repo  
```bash
git clone https://github.com/paviAzmira/advanced-osint-username-scanner.git
cd advanced-osint-username-scanner
Install dependencies
pip install -r requirements.txt
install playwright browser
playwright install
Usage
# Basic scan
python -m src.cli johndoe

# Custom scan
python -m src.cli johndoe --concurrency 100 --timeout 15 --out reports/johndoe
Web interface
python webapp/app.py
.  .  Performance  55 platforms: 15-30 seconds Cache hit rate: ~80%  Rate limit: 2 req/sec RAM: 50-100MB average  Ethical Usage  This tool is for authorized OSINT, security research, and personal investigation only.  v Respects robots.txt vUses only public information v No bypassing protections V No unauthorized access  You are responsible for your usage.

PROJECT STRUCTURE
advanced-osint-username-scanner/
│
├── src/                    # core async engine
├── webapp/                 # Flask web interface
├── data/                   # sqlite cache + reports
├── requirements.txt
├── LICENSE
└── README.md

