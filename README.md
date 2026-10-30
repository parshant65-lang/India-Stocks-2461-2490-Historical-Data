# India-Stocks-2461-2490-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2461 to 2490)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2461-2490-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2461 to 2490)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2461 | `UDAYJEW` | Uday Jewellery Industries Limited | `UDAYJEW.NS` |
| 2462 | `UDS` | Updater Services Limited | `UDS.NS` |
| 2463 | `UEL` | Ujaas Energy Limited | `UEL.NS` |
| 2464 | `UFBL` | United Foodbrands Limited | `UFBL.NS` |
| 2465 | `UFLEX` | UFLEX Limited | `UFLEX.NS` |
| 2466 | `UFO` | UFO Moviez India Limited | `UFO.NS` |
| 2467 | `UGARSUGAR` | The Ugar Sugar Works Limited | `UGARSUGAR.NS` |
| 2468 | `UGROCAP` | Ugro Capital Limited | `UGROCAP.NS` |
| 2469 | `UJJIVANSFB` | Ujjivan Small Finance Bank Limited | `UJJIVANSFB.NS` |
| 2470 | `ULTRAMAR` | Ultramarine & Pigments Limited | `ULTRAMAR.NS` |
| 2471 | `UMAEXPORTS` | Uma Exports Limited | `UMAEXPORTS.NS` |
| 2472 | `UMESLTD` | Usha Martin Education & Solutions Limited | `UMESLTD.NS` |
| 2473 | `UMIYA-MRO` | UMIYA BUILDCON LIMITED | `UMIYA-MRO.NS` |
| 2474 | `UNICHEMLAB` | Unichem Laboratories Limited | `UNICHEMLAB.NS` |
| 2475 | `UNIDT` | United Drilling Tools Limited | `UNIDT.NS` |
| 2476 | `UNIECOM` | Unicommerce Esolutions Limited | `UNIECOM.NS` |
| 2477 | `UNIENTER` | Uniphos Enterprises Limited | `UNIENTER.NS` |
| 2478 | `UNIINFO` | Uniinfo Telecom Services Limited | `UNIINFO.NS` |
| 2479 | `UNIMECH` | Unimech Aerospace and Manufacturing Limited | `UNIMECH.NS` |
| 2480 | `UNIPARTS` | Uniparts India Limited | `UNIPARTS.NS` |
| 2481 | `UNITECH` | Unitech Limited | `UNITECH.NS` |
| 2482 | `UNITEDPOLY` | United Polyfab Gujarat Limited | `UNITEDPOLY.NS` |
| 2483 | `UNITEDTEA` | The United Nilgiri Tea Estates Company Limited | `UNITEDTEA.NS` |
| 2484 | `UNIVASTU` | Univastu India Limited | `UNIVASTU.NS` |
| 2485 | `UNIVCABLES` | Universal Cables Limited | `UNIVCABLES.NS` |
| 2486 | `UNIVPHOTO` | Universus Photo Imagings Limited | `UNIVPHOTO.NS` |
| 2487 | `UPHOT` | U P Hotels Limited | `UPHOT.NS` |
| 2488 | `URAVIDEF` | Uravi Defence and Technology Limited | `URAVIDEF.NS` |
| 2489 | `URJA` | Urja Global Limited | `URJA.NS` |
| 2490 | `USK` | Udayshivakumar Infra Limited | `USK.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream UDAYJEW 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2461-2490-Historical-Data/main/UDAYJEW/1m/2026/10/UDAYJEW_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
