<div align="center">

<img src="docs/images/banner.svg" alt="models — stock market financial models organized by ticker" width="900"/>

[![Format](https://img.shields.io/badge/format-Excel_·_PDF-217346.svg)](#whats-inside)
[![Regions](https://img.shields.io/badge/regions-US_·_JP_·_HK_·_KR-3b82f6.svg)](#per-ticker-files)
[![Sectors](https://img.shields.io/badge/sectors-11-fbbf24.svg)](#sector-files)
[![Disclaimer](https://img.shields.io/badge/not-investment_advice-ef4444.svg)](#disclaimer)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

**A personal reference set of stock market spreadsheets organized by ticker, sector, and therapeutic area.**

</div>

---

## Why this exists

Personal equity research collection. Each ticker gets its own `.xlsx` (and an annual-report PDF when available), with cross-cuts by **sector**, **disease area**, and **screens**. The repo is the long-term filing cabinet behind the analysis — useful as a snapshot, not a live data feed.

---

## What's inside

```mermaid
flowchart TD
    Master["📒 Master.xlsx<br/>central index"] --> Sector
    Master --> Disease
    Master --> Ticker
    Master --> Screen

    subgraph Sector["📊 Sector files · 11"]
        S1[Biopharma]
        S2[Software]
        S3[Medical Devices]
        S4[HC Services · HCIT]
        S5[Industrials · Consumer]
        S6[HardwareSemis · Telecom-Media]
        S7[Gaming · Crypto]
    end

    subgraph Disease["🧬 Disease files · 3"]
        D1[Cardiovascular]
        D2[Psychiatry]
        D3[Alzheimer's]
    end

    subgraph Ticker["🌐 Per-ticker files · 600+"]
        T1["US · ABBV, AMC, AZN…"]
        T2["JP · 4502 Takeda, 4519 Chugai…"]
        T3["HK · 2196, 2269 WuXi Bio…"]
        T4["KR · 005930 Samsung, 035420 Naver…"]
    end

    subgraph Screen["🔎 Screens/<br/>filtered short lists"]
        SC1[quant cuts]
        SC2[sector subsets]
    end

    subgraph Aux["📎 Reference"]
        A1[Hedge Funds.xlsx]
        A2[PDBs.xlsx]
        A3[Patents.xlsx]
    end
    Master --> Aux

    style Master fill:#fbbf24,color:#0c1e3a,stroke:#92400e
    style Sector fill:#0c1e3a,color:#bfdbfe,stroke:#3b82f6
    style Disease fill:#1f1010,color:#fecaca,stroke:#dc2626
    style Ticker fill:#0f1f17,color:#bbf7d0,stroke:#16a34a
    style Screen fill:#1f1410,color:#fed7aa,stroke:#f59e0b
```

<div align="center">
  <img src="docs/images/category-map.svg" alt="Category map — sectors, diseases, per-ticker files, screens, and master index" width="800"/>
  <br/>
  <sub><i>Master.xlsx at the center, cross-cuts by sector / disease / region radiating out.</i></sub>
</div>

---

## 🚀 Quick start

Clone and open whichever sheet matches what you're looking for. Everything is plain Excel — no scripts, no setup.

```bash
git clone https://github.com/Anic888/models.git
cd models
open Master.xlsx          # macOS
# or use your spreadsheet tool of choice
```

---

## Sector files

Top-down cuts across the universe. Use these when scanning a whole space.

| File | Coverage |
|------|----------|
| `Biopharma.xlsx` | Large- and mid-cap drug developers |
| `Software.xlsx` | Application + infrastructure software |
| `Telecom-Media.xlsx` | Carriers, broadcasters, streaming |
| `Medical Devices.xlsx` | Diagnostic and therapeutic device makers |
| `Industrials.xlsx` | Industrial conglomerates and machinery |
| `HCIT.xlsx` | Healthcare IT and analytics |
| `HC Services.xlsx` | Hospital systems, payers, services |
| `HardwareSemis.xlsx` | Semiconductors and hardware |
| `Gaming.xlsx` | Gaming publishers and platforms |
| `Crypto.xlsx` | Crypto-adjacent listed names |
| `Consumer.xlsx` | Consumer goods and brands |

---

## Disease files

Therapeutic-area views — used when the relevant unit of analysis is the indication, not the company.

| File | Focus |
|------|-------|
| `Cardiovascular.xlsx` | Heart-failure, lipids, antithrombotics |
| `Psychiatry.xlsx` | Antidepressants, antipsychotics, mood disorders |
| `Alzheimer's.xlsx` | AD-modifying therapies, diagnostics |

---

## Per-ticker files

One spreadsheet per ticker, plus an annual-report PDF where available. Examples by region:

| Region | Examples |
|--------|----------|
| US | `ABBV`, `AMC`, `APLS`, `AZN`, … |
| JP | `4502 Takeda`, `4503 Astellas`, `4519 Chugai`, `4523 Eisai`, `4568 Daiichi Sankyo`, `6758 Sony`, … |
| HK | `1177 Sino`, `1211 BYD`, `1877`, `2196`, `2269 WuXi Biologics`, `3692 Hansoh`, … |
| KR | `005930 Samsung`, `035420 Naver`, `068270 Celltrion`, `207940 Samsung Biologics`, `302440`, … |

Folder-form names (e.g. `068270 Celltrion/`) contain the spreadsheet plus supporting files.

---

## Reference sheets

Cross-sectional data not tied to a single ticker.

| File | Purpose |
|------|---------|
| `Master.xlsx` | Central index across the entire repo |
| `Hedge Funds.xlsx` | Ownership and 13F-style tracking |
| `PDBs.xlsx` | Drug-target / structural reference |
| `Patents.xlsx` | Patent landscape for selected molecules |

---

## Screens

The `Screens/` folder contains short lists generated by quant criteria (revenue growth, margin expansion, pipeline catalysts, etc.). Useful as a starting point to find ideas, not as a recommendation list.

---

## Disclaimer

**Not investment advice.** These spreadsheets are personal reference models for study and analysis only. Data may be stale, incomplete, or wrong. Numbers and notes reflect snapshots from when each file was last touched — verify with primary sources before relying on anything here.

---

## Contributing

Issues and PRs welcome for:

- Correcting factual errors
- Adding regional coverage (EU, LatAm, MENA tickers)
- New therapeutic-area files

---

## License

[MIT](./LICENSE) — the spreadsheets themselves are personal reference; the repository structure and README are MIT.
