# INVENTION DISCLOSURE DOCUMENT
## Prior Art Establishment & Copyright Notice

**Title:** Multi-Layer Cryptocurrency Pump Signal Detection System  
**Inventor:** Rohit Mehra  
**Date of First Creation:** 2025  
**Document Type:** Invention Disclosure for Prior Art Establishment

---

## ABSTRACT

A novel multi-layer signal scoring system for detecting cryptocurrency
pump patterns in real-time, combining causal dependency analysis,
distributed consensus voting across multiple exchanges, deterministic
Byzantine fault tolerance, and adaptive sigmoid-weighted signal scoring
into a unified 4-layer detection architecture called the
**FAXWEB Horizontal Scalability System**.

---

## 1. FIELD OF INVENTION

This invention relates to:
- Real-time cryptocurrency market signal detection
- Distributed consensus mechanisms applied to market data validation
- Causal graph analysis of financial microstructure signals
- Adaptive weighted scoring for trading signal aggregation

---

## 2. PROBLEM BEING SOLVED

Existing cryptocurrency pump detection systems:
- Analyze signals independently without causal relationship modeling
- Use single-exchange data susceptible to manipulation
- Apply static weights that do not adapt to signal accuracy history
- Cannot distinguish coordinated whale activity from organic buying

---

## 3. PROPRIETARY INNOVATIONS

### 3.1 FAXWEB Horizontal Scalability Engine
*Core Innovation — Novel Combination*

A ring-topology consensus system connecting 6 cryptocurrency exchanges
(C0=Binance, C1=OKX, C2=Bybit, C3=KuCoin, C4=Gate.io, C5=HTX) using:

- **FNV-1a Successive Proof of Verification (SPV):**
  Each node hashes its state as:
  `H(node_id | block_height | prev_hash | buy_ratio)`
  using the FNV-1a non-cryptographic hash function for speed

- **Ring Neighbor Verification:**
  Node adjacency map: {0:[1,5], 1:[0,2], 2:[1,3], 3:[2,4], 4:[3,5], 5:[4,0]}
  A node is verified when ≥1 neighbor confirms its hash

- **aBFT Supermajority Rule:**
  Signal is valid when ≥4/6 nodes (67%) agree on accumulation
  This tolerates up to f=2 Byzantine (manipulated) exchange nodes

**Novel aspect:** Applying blockchain-style hash-chained SPV verification
to real-time multi-exchange market data for signal validation — not
transaction validation.

---

### 3.2 Causal Signal Dependency Chain (CSDC)
*Core Innovation — Novel Architecture*

A directed acyclic graph (DAG) model of cryptocurrency pump causality:

```
Funding Rate → Open Interest → CVD → Bid Wall
     → Shannon Entropy → VWAP Deviation → Regime → PUMP
```

**Scoring formula:**
```
chain_strength = (c1 × c2 × c3 × c4 × c5 × c6)^(1/6)

Where each c_i ∈ {0.40, 0.50, 0.60, 0.65, 1.00}
based on causal condition satisfaction.

Weak-link penalty: if weak_links ≥ 2: chain_strength × 0.75
```

**Causal conditions:**
- c1: Fund<-0.02 AND OI>5 → 1.0 (else 0.5-0.6)
- c2: OI>8 AND CVD>2 → 1.0 (else 0.5-0.65)
- c3: CVD>2.5 AND BidWall>0.65 → 1.0 (else 0.5-0.6)
- c4: BidWall>0.68 AND Entropy<0.40 → 1.0 (else 0.5-0.65)
- c5: Entropy<0.35 AND VWAP<-0.02 → 1.0 (else 0.4-0.65)
- c6: VWAP<-0.03 AND Regime>0.02 → 1.0 (else 0.45-0.65)

**Novel aspect:** Modeling pump signal causality as a directed dependency
graph with geometric mean strength and penalty for broken causal links.

---

### 3.3 Dual-Set Byzantine Consensus (DS-BFT)
*Core Innovation — Novel Application*

Applying Sumeragi-inspired 3f+1 Byzantine consensus to exchange
signal validation:

- **Set A** (active validators): nodes C0, C1, C2, C3 (2f+1 = 4)
- **Set B** (passive observers): nodes C4, C5 (f = 2)
- **Leader selection:** `leader_index = block_number % 4` (deterministic)
- **Consensus threshold:** ≥3/4 Set A votes required
- **Fallback:** If Set A fails, Set B activates with ≥1/2 votes

**Scoring:**
```
score = 0.5 + (set_a_votes / 4) × 0.5   [if consensus]
score = 0.35                              [if fallback]
score = 0.15                              [if no consensus]
```

**Novel aspect:** Applying permissioned BFT consensus with active/passive
validator sets to real-time cryptocurrency exchange data aggregation.

---

### 3.4 Adaptive Sigmoid Signal Scoring (ASSS)
*Core Innovation — Novel Method*

A neural-inspired weighting system where each signal component has
a historical accuracy weight updated over time:

**Weight formula:**
```
W(signal) = sigmoid(10 × (accuracy - 0.5))
           = 1 / (1 + e^(-10×(accuracy-0.5)))
```

**Signal accuracy registry:**
```
CVD:    0.82    Entropy: 0.78
Funding: 0.75   OI:      0.72
Hurst:  0.70    VWAP:    0.76
Regime: 0.68    Divergence: 0.65
```

**Composite score:**
```
neural_score = Σ(W(i) × normalized_signal(i)) / Σ W(i)
```

**Novel aspect:** Applying sigmoid-activated historical accuracy weighting
to aggregate heterogeneous cryptocurrency market signals.

---

### 3.5 Quad Consensus Bonus System (QCBS)
*Core Innovation — Novel Combination*

A four-protocol validation framework with additive bonus scoring:

```
base_score = Spring(25%) + Flow(20%) + Micro(28%) + Regime(27%)

dag_bonus      = +5 (DAG>0.75) | +3 (DAG>0.62) | 0
sumeragi_bonus = +4 (DS-BFT 4/4) | +2 (3/4) | 0
neural_bonus   = +3 (sigmoid>0.68) | +1 (>0.55) | 0
spark_bonus    = +2 (slope 0.02-0.08) | 0
consensus_bonus= +2 (all 4 layers agree) | 0

final_score = clamp(base_score + all_bonuses, 1, 99)
```

**Novel aspect:** Combining 4 independent validation protocols
(causal graph + hash consensus + BFT voting + sigmoid weighting)
into a unified additive scoring system with maximum +16 bonus points.

---

## 4. COMBINATION NOVELTY CLAIM

**The primary patent claim is the COMBINATION:**

> A system and method for real-time cryptocurrency pump signal detection
> comprising: (a) a causal dependency graph scoring module analyzing
> fund→OI→CVD→entropy→VWAP signal chain strength, (b) a hash-chained
> multi-exchange ring consensus engine with aBFT supermajority validation,
> (c) a dual-set Byzantine fault tolerant consensus mechanism with
> deterministic leader selection, and (d) an adaptive sigmoid-weighted
> neural scoring layer, wherein scores from all four layers are combined
> using an additive bonus system to produce a final pump probability score.

---

## 5. PRIOR ART DISTINGUISHED

| Component | Prior Art | Our Novel Application |
|-----------|-----------|----------------------|
| Shannon Entropy | 1948 (Shannon) | Applied to crypto bid-ask entropy collapse |
| Hurst Exponent | 1951 (Hurst) | Applied to crypto momentum trend detection |
| Nash Equilibrium | 1950 (Nash) | Applied to whale coordination modeling |
| DAG structure | 1736 (Euler) | Applied as causal signal dependency graph |
| BFT consensus | 1982 (Lamport) | Applied to exchange data validation |
| Sigmoid function | 1844 (Verhulst) | Applied to signal accuracy weighting |
| CVD | Known in trading | Combined in causal chain with entropy |

**The COMBINATION of all above in a unified pump detection system
applied to cryptocurrency markets is the novel contribution.**

---

## 6. COPYRIGHT NOTICE

```
Copyright (c) 2025 Rohit Mehra
All Rights Reserved.

Software: Scanner by Rohit Mehra — Live
Components: FAXWEB Horizontal Scalability System,
            CSDC, DS-BFT, ASSS, QCBS

This document establishes prior art dated 2025.
```

---

## 7. TRADEMARK NOTICE

**FAXWEB™** is a trademark of Rohit Mehra.
Unauthorized commercial use of this mark is prohibited.

---

## 8. NEXT STEPS FOR FORMAL PATENT

1. **File Provisional Patent** (12 oy vaqt, $320 USPTO fee)
   — Provides "Patent Pending" status immediately
   — Establishes priority date

2. **Full Patent Application** ($5,000-15,000 with attorney)
   — Claims 3.1 through 3.5 as independent claims
   — International filing via PCT ($3,000+)

3. **Trademark Registration**
   — USPTO: ~$250 per class
   — Class 42 (Software/Technology services)

---

*This document was created on the date of software creation and
establishes prior art for the innovations described herein.*

*Rohit Mehra — 2025*
