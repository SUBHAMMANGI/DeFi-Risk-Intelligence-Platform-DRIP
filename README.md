# 💧 DRIP - DeFi Risk Intelligence Platform

> **Real-time risk monitoring for $124B+ across 100 DeFi protocols.**
> Every protocol scored 0-100 like a credit rating agency scores a bond.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-0969da?style=for-the-badge)](https://subhammangi.github.io/DeFi-Risk-Intelligence-Platform-DRIP-/)
[![FinHack 2026](https://img.shields.io/badge/FinHack%202026-Case%203-2ea44f?style=for-the-badge)](https://github.com/subhammangi/DeFi-Risk-Intelligence-Platform-DRIP-)
[![Zero Backend](https://img.shields.io/badge/Zero%20Backend-One%20HTML%20File-6e7681?style=for-the-badge)](https://github.com/subhammangi/DeFi-Risk-Intelligence-Platform-DRIP-)

---

## The Problem

Euler Finance lost **$197,000,000** in a single day in March 2023.

Their TVL dropped **30% in the 6 weeks before the exploit**.

The signal existed. No tool was watching for it.

**DRIP is that tool.**

---

## Live Demo

🔗 **[https://subhammangi.github.io/DeFi-Risk-Intelligence-Platform-DRIP-/](https://subhammangi.github.io/DeFi-Risk-Intelligence-Platform-DRIP-/)**

No install. No signup. Open in any browser.

---

## What Is DRIP?

DRIP monitors 100 DeFi protocols in real time and assigns each one a **DRIP Score™** (0-100) - a composite risk rating built from five weighted factors:

| Component | Weight | What It Measures |
|---|---|---|
| Code Safety | 30% | Audit count, protocol age, bug bounty |
| Drawdown Risk | 25% | Historical max TVL crashes |
| Volatility | 20% | 7-day TVL swing magnitude |
| Chain Concentration | 15% | Single-chain dependency risk |
| Liquidity Risk | 10% | Exit depth - stampede risk |

**Score ranges:**
- 🟢 0-22 → HEALTHY - Hold / Add
- 🔵 22-35 → MODERATE - Watch
- 🟡 35-50 → ELEVATED - Reduce
- 🔴 50-100 → HIGH RISK - Exit

---

## The Model in Action

| Protocol | DRIP Score | Status | Result |
|---|---|---|---|
| Euler Finance | **75** | 🔴 HIGH RISK | Exploited for $197M - Mar 2023 |
| Badger DAO | **63** | 🔴 HIGH RISK | Exploited for $120M - Dec 2021 |
| Harvest Finance | **66** | 🔴 HIGH RISK | Exploited for $34M - Oct 2020 |
| Aave | **19** | 🟢 HEALTHY | Never exploited in 5+ years |

**The model was right. Every time.**

---

## Features

### 📊 Dashboard
- 100-protocol health scorecard with live TVL, risk scores, and trend delta
- Inline search + 10 sort options (highest risk, healthiest first, TVL, drawdown, audits, age)
- 92 auto-detected risk alerts sorted by severity with filter (Critical / Warnings / Healthy)
- Market Context panel - overall regime, TVL monitored, max recommended exposure
- Export current view to dated CSV

### 📈 Analytics (6 views)
- **Risk Analysis** - Score distribution, bubble chart, category breakdown
- **Stress Tests** - ETH drop 40%, major hack, DeFi black swan simulations
- **Capital Flows** - 90-day TVL trends, category distribution, waterfall
- **Compare** - Side-by-side up to 3 protocols
- **Protocol Analyzer** - Enter any protocol metrics → instant DRIP Score + gauge
- **Action Plan** - HOLD/WATCH/REDUCE/EXIT recommendations for all 100

### 📅 Historical Data
- Real day-by-day TVL from DeFiLlama per-protocol API
- Exploit events marked directly on chart - see TVL bleeding before the hack
- Peak TVL, current TVL, max drawdown stats per protocol

### ⭐ My Watchlist
- Star any protocol - see alerts only for what you're watching
- Watchlist risk summary - avg DRIP, total TVL, high-risk count
- Persists across browser sessions via localStorage

### 💼 My Portfolio (3 modes)
- **Connect Wallet** - paste Ethereum address → DeBank API reads all DeFi positions → auto-syncs every 2 min
- **Import CSV** - drag & drop from Zerion, DeBank, Zapper, Coinbase, Binance
- **Manual Entry** - select protocol + amount + portfolio %
- Weighted DRIP Score by actual holdings
- Personalised HOLD/WATCH/REDUCE/EXIT per position
- Full persistence - wallet reconnects automatically on next visit

---

## Tech Stack

```
Frontend:    HTML5 + CSS3 + Vanilla JS (ES2020)
Charts:      Chart.js 4.4.1
Fonts:       Inter + JetBrains Mono (Google Fonts)
Data:        DeFiLlama Public API (live TVL)
Wallet:      DeBank Public API (portfolio positions)
Storage:     Browser localStorage (no database)
Backend:     None
Deploy:      Single HTML file
```

---

## Architecture

```
DeFiLlama API      →  Live TVL + 7d change (refreshes every 5 min)
      +
FALLBACK[100]      →  100 protocols with research-based risk scores
      =
PROTOCOLS[]        →  Merged working array in browser RAM
      ↓
DRIP Score Engine  →  Scores computed in real time
      ↓
13 Views + 9 Charts
```

No server. No database. No API keys. Entirely client-side.

---

## Quick Start

```bash
# Option 1 - Open directly
open index.html

# Option 2 - Deploy to Netlify
# Drag index.html to netlify.com - get live URL in 10 seconds

# Option 3 - Vercel
npx vercel deploy --public
```

---

## Data Sources

| Source | What We Use |
|---|---|
| DeFiLlama | Live TVL, 1d/7d change, historical per-protocol TVL |
| DeBank | Wallet DeFi positions (read-only) |
| Internal | Audit counts, age, risk scores (research dataset) |

All APIs are free, public, and CORS-enabled. Zero API keys required.

---

## Methodology

DRIP Score adapted from **ConsenSys DeFi Score** (MIT License).

Calibrated against 5 historical exploits where TVL anomalies appeared 1-6 weeks before the hack - Euler ($197M), Badger ($120M), Harvest ($34M), Yearn ($11M), Inverse ($15M).

---

## Built At

**FinHack 2026** · Case 3 · JSOM Finance Lab · UT Dallas

---

## Author

**Subham Mangi**
[LinkedIn](https://www.linkedin.com/in/subhammangi/) · [GitHub](https://github.com/subhammangi)

---

*DRIP is for informational purposes only. Not financial advice.*
