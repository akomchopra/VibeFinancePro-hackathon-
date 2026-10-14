# ⚡ VibeFinance Pro — Argan-4 Multi-Agent Financial Intelligence Terminal

> **PS 04 — VibeFinance: Multi-Agent Autonomous Financial Intelligence for Retail Investors**  
> **Principal Quant Desk & Team Lead:** Shreyan Joshi  
> **Core Engine:** Argan-4 Parallel Multi-Agent Architecture (`ThreadPoolExecutor` + Live SEBI RAG + Risk Guardrails)

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/)
[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-00d09c.svg)](https://www.python.org/)
[![NSE Live Telemetry](https://img.shields.io/badge/NSE_Telemetry-yfinance_%2B_Fallback-38bdf8.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-ffb300.svg)]()

---

## 🎯 Executive Summary

India's retail investors have unprecedented access to raw market streams—NSE price feeds, SEBI Regulation 30 corporate filings, earnings call transcripts, FII/DII bulk flows, and derivatives options chains. However, existing retail platforms operate in silos: chart screeners flag technical breakouts without checking regulatory headwinds, and news aggregators surface headlines without evaluating the user's personal drawdown limits or portfolio concentration.

**VibeFinance Pro** bridges this gap. Powered by the **Argan-4 Autonomous Multi-Agent Core**, it ingests live NSE market data and regulatory disclosures, executes **four specialized AI agents in parallel worker threads**, grounds claims in verifiable SEBI/NSE citations via cosine-similarity Retrieval-Augmented Generation (RAG), and adapts every trade recommendation to the investor's active risk mandate and behavioral history.

---

## 🏗️ System Architecture & Decision Logic

```text
[Raw Market & Regulatory Feeds]
  ├── NSE Price/Volume Socket (yfinance Live API + Deterministic Fallback Engine)
  ├── SEBI Reg 30 Filings & Live Vector Search Corpus (Dynamic Document Injector)
  └── NSE Derivatives Options Chain (Strike OI, IV%) & FII Flow Ledger
          │
          ▼
[Parallel Multi-Agent Execution Layer (concurrent.futures.ThreadPoolExecutor)]
  ├── Thread 1: Agent 1 — Quant Technical Classifier (14D RSI, MACD, 20-SMA, Bollinger, Vol Z-Score)
  ├── Thread 2: Agent 2 — RAG Fundamental Analyst (Live Token-Vector Cosine Similarity + Citations)
  ├── Thread 3: Agent 3 — Institutional & Options Flow Agent (PCR, Max Pain, Delivery Spikes)
  └── Thread 4: Agent 4 — Personalized Risk & Behavioral Guard (Drawdown Cap, HHI Concentration, Veto Gate)
          │
          ▼
[Argan-4 Meta-Synthesizer & Confidence Calibration Gate]
  ├── Penalizes Composite Conviction under Inter-Agent Disagreement (-28%) or Degraded Feeds (-14%)
  ├── Cross-checks consensus against Shreyan Joshi's Active Risk Mandate (Aggressive / Balanced / Capital Preservation)
  └── Outputs: Explainable Verdict + Verifiable Citations + Position Sizing + Exportable IC Memo (.md)