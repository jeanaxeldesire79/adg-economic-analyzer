# 📊 ADG Economic Analyzer

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![HTML](https://img.shields.io/badge/HTML-5-orange)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS-3-blueviolet)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Status](https://img.shields.io/badge/status-BETA-yellow)]()

> Interactive economic indicator explorer for 15 ECOWAS member states. 44K+ data points covering 88 indicators from 1960–2023.

**Part of the [Axel Dev Group (ADG)](https://axeldevlab.com) portal ecosystem.**

---

## 🚀 Live Demo

Visit **[portal.axeldevlab.com](https://portal.axeldevlab.com)** → Navigate to **Economic Analyzer**

> ⚠️ Portal access requires login credentials. Contact the ADG team for access.

![Economic Analyzer Screenshot](docs/screenshot.png)

---

## ✨ Features

- 📈 **Interactive Charts** — Time-series line charts for any indicator-country combination
- 🌍 **15 ECOWAS Countries** — Full member state coverage with metadata
- 🔍 **88+ Indicators** — GDP, inflation, trade, education, health, infrastructure, and more
- 📅 **Year Range 1960–2023** — Deep historical data for trend analysis
- 🏷️ **Indicator Search & Filter** — Find indicators by name, category, or code
- 📊 **Data Table View** — Raw data export for further analysis
- 🌙 **Dark Theme** — Optimized for extended data exploration sessions
- 📱 **Responsive Design** — Works on desktop, tablet, and mobile

---

## 🏗️ Architecture

```
┌──────────────┐     ┌──────────────────────┐     ┌──────────────────┐
│   Browser    │────▶│   Portal API         │────▶│   PostgreSQL     │
│  (Vanilla    │     │   (Python FastAPI)   │     │   (datasci_db)   │
│   HTML/CSS/  │◀────│                      │◀────│                  │
│   JS)        │     │  /api/data/economic/*│     │  political_      │
│              │     │                      │     │  economy.*       │
└──────────────┘     └──────────────────────┘     └──────────────────┘
                                                          │
                                                          ▼
                                                  ┌──────────────────┐
                                                  │  public.*_world- │
                                                  │  bank (500K rows)│
                                                  └──────────────────┘
```

The app is a **single-file HTML application** with zero build dependencies. All data is fetched live from the portal API.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | Vanilla HTML5, CSS3 (custom properties), JavaScript (ES6+) |
| **Charts** | Chart.js (via CDN) |
| **Icons** | Font Awesome (via CDN) |
| **Backend** | Python FastAPI |
| **Database** | PostgreSQL 15 (`datasci_db`) |
| **Data Sources** | World Bank API, UNDP HDR API, Google Drive CSV |
| **Deployment** | Portal module viewer on `portal.axeldevlab.com` |

---

## 📊 Data Sources

| Source | Data | Coverage |
|--------|------|----------|
| **World Bank API** | WDI indicators (GDP, inflation, trade, etc.) | 1960–2023 |
| **World Bank CSV (Google Drive)** | 44K+ ECOWAS-specific indicators | 1960–2023 |
| **UNDP HDR API** | Human Development Index components | 1990–2022 |
| **Natural Earth** | Country boundaries and metadata | Static |

---

## 📁 Repository Structure

```
adg-economic-analyzer/
├── README.md               # This file
├── LICENSE                 # MIT License
├── CHANGELOG.md            # Version history
├── CONTRIBUTING.md         # How to contribute
├── src/
│   └── index.html          # Single-file app (production HTML)
├── docs/
│   └── screenshot.png      # App screenshot
├── data/
│   └── schema.md           # Database schema reference
├── scripts/
│   └── deploy.sh           # Deployment script
└── .github/
    └── workflows/          # GitHub Actions (future)
```

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.
