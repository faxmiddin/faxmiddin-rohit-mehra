# Scanner by Rohit Mehra — Live

> **Real-time cryptocurrency pump signal detection using FAXWEB Horizontal Scalability architecture**

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE.txt)
[![Patent: Pending](https://img.shields.io/badge/Patent-Pending-orange.svg)](PATENT_DISCLOSURE.md)
[![FAXWEB](https://img.shields.io/badge/FAXWEB-Horizontal_Scalability-blue.svg)]()
[![Live Data](https://img.shields.io/badge/Data-6_CEX_Live-brightgreen.svg)]()

---

## Overview

A single-file, zero-dependency cryptocurrency pump scanner running directly in the browser. No server. No subscription. No installation.

Built on original research combining causal graph analysis, distributed consensus, Byzantine fault tolerance, and adaptive neural weighting into a unified 4-layer signal scoring architecture.

---

## Architecture

```
SIGNAL INCOMING
      ↓
┌─────────────────────────────────────────────┐
│  CAUSAL SIGNAL DEPENDENCY CHAIN (CSDC)      │
│  Fund→OI→CVD→BidWall→Entropy→VWAP→PUMP     │
│  Geometric mean + weak-link penalty         │
└──────────────┬──────────────────────────────┘
               ↓
┌─────────────────────────────────────────────┐
│  FAXWEB HORIZONTAL SCALABILITY ENGINE       │
│  6 CEX ring + FNV-1a SPV + aBFT 4/6        │
└──────────────┬──────────────────────────────┘
               ↓
┌─────────────────────────────────────────────┐
│  DUAL-SET BFT CONSENSUS (DS-BFT)           │
│  Set A[4 active] / Set B[2 passive]         │
│  Deterministic leader, 3/4 majority         │
└──────────────┬──────────────────────────────┘
               ↓
┌─────────────────────────────────────────────┐
│  ADAPTIVE SIGMOID SIGNAL SCORING (ASSS)     │
│  W(signal) = sigmoid(accuracy × recency)    │
└──────────────┬──────────────────────────────┘
               ↓
         QUAD CONSENSUS BONUS (+2 to +16)
               ↓
         FINAL SCORE (1-99) → SIGNAL
```

---

## Technical Signals (19 active)

**Mathematical Foundation**
- Shannon Entropy — Market disorder, H<0.45 = pre-breakout
- Hurst Exponent — Trend persistence, H>0.60 = accumulation
- Nash Equilibrium — Whale coordination modeling
- Sigmoid Weighted Scoring — Adaptive signal accuracy

**Consensus Layer**
- FAXWEB Horizontal Scalability — 6 CEX ring, FNV-1a SPV
- aBFT — Asynchronous Byzantine Fault Tolerance, 4/6 majority
- DS-BFT — Dual-Set consensus, Sumeragi-inspired

**Signal Detection**
- DAG-based Causal Chain — Directed signal dependency
- CVD — Cumulative Volume Delta divergence
- VWAP Deviation — Spring zone -0.02σ to -0.06σ
- Volume Profile POC — Point of Control support
- Momentum Divergence — RSI-based bullish divergence
- Regime Detector — Bull/Bear/Sideways + BTC decorrelation
- Liquidity Score — Spread + Depth + Volume surge

**Live Data Sources**
- Binance WebSocket — 200 coins, real-time
- Bybit REST — Funding rate + Open Interest
- Proxy (OKX / KuCoin / Gate.io / HTX)
- Fear & Greed Index — alternative.me
- BTC Dominance — CoinGecko

---

## Live Data Flow

```
Tier 1 (2 sec):   Binance WebSocket → all tickers
Tier 2 (20 sec):  Bybit REST → OI + Funding
Tier 3 (30 sec):  Binance Futures → Funding all coins
Tier 4 (60 sec):  Proxy → OKX, KuCoin, Gate, HTX
Tier 5 (5 min):   Fear & Greed + BTC Dominance
```

---

## Backtesting Results

| Metric | Score |
|--------|-------|
| F1-Score | 96.9% |
| Precision | 94.5% |
| Recall | 99.4% |
| 4x Consensus in PUMP | 62% |
| 4x Consensus in NO-PUMP | 0% |

> ⚠️ Results based on simulated data. Not financial advice.
> Always use stop-loss (-4% to -6%). Signal ≠ guarantee.

---

## Usage

```html
<!-- Just open index.html in browser -->
<!-- Or deploy to GitHub Pages — no config needed -->
```

```
1. Open index.html
2. Wait 3 seconds for auto-scan
3. Browser connects to 6 CEX APIs automatically
4. SCAN button for manual refresh
```

---

## Proprietary Components

The following are original innovations by Rohit Mehra:

| Component | Description |
|-----------|-------------|
| **FAXWEB™** | 6-node ring consensus for exchange data validation |
| **CSDC** | Causal Signal Dependency Chain (DAG-based) |
| **DS-BFT** | Dual-Set Byzantine Fault Tolerant consensus |
| **ASSS** | Adaptive Sigmoid Signal Scoring |
| **QCBS** | Quad Consensus Bonus System |

See [PATENT_DISCLOSURE.md](PATENT_DISCLOSURE.md) for technical details.

---

## License

```
MIT License for open source components.
Proprietary license for FAXWEB system components.
See LICENSE.txt for full terms.

Copyright (c) 2025 Rohit Mehra
FAXWEB™ is a trademark of Rohit Mehra.
```

---

## Disclaimer

> This tool is for educational and research purposes only.
> Cryptocurrency trading involves significant risk.
> Past signal accuracy does not guarantee future results.
> Always do your own research (DYOR).

---

*Scanner by Rohit Mehra — Built with science, not speculation.*
