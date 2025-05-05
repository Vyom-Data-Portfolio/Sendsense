SpendSense
==========

SpendSense is a reproducible analytics mini‑stack that shows how to turn raw transaction data into interactive business insights with **dbt** and **Metabase**.

Problem statement
-----------------
> “Given consumer‑level transaction records, surface high‑value customers and spending trends that finance or growth teams can act on.”

Dataset
-------
* **Source:** Lending Club Loan Stats 2017‑2018 (public CSV, 2 MB sample)  
* **Fields used:** loan amount, funded amount, issue date, grade, interest rate, borrower state  
* Located in `data/raw/loan_stats_sample.csv`

Stack
-----
| Layer | Tool | Why |
|-------|------|-----|
| Storage | Postgres (Docker) | lightweight OLAP demo |
| Transform | dbt 1.x | versioned SQL + tests |
| Viz | Metabase OSS | self‑host, free |

Quick start
-----------

Run these commands in your terminal (first run downloads Docker images, ~2 min):

```bash
git clone https://github.com/vyom-ds-portfolio/spendsense.git
cd spendsense
docker compose up

