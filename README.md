# Regulatory Risk Audit Analytics

## Project Overview

This project simulates a data-driven Internal Audit review of regulatory risk processes in a banking environment.

The objective is to demonstrate how SQL and Python can support Internal Audit testing across key financial risk and prudential regulation areas, including:

* Capital & RWA
* ICAAP
* Risk Appetite Framework
* ILAAP
* IFRS 9 staging and expected credit loss

The project does not aim to replicate a full regulatory reporting, capital, liquidity or IFRS 9 model. Its purpose is to show how Internal Audit can use data analytics to test controls, identify exceptions, challenge assumptions and produce audit evidence.

---

## Why This Project Matters

Internal Audit functions in banking are increasingly expected to move from sample-based testing to data-driven assurance.

Instead of reviewing a limited number of cases manually, auditors can use SQL and Python to analyse full populations, detect exceptions, identify control weaknesses and generate reproducible evidence.

This project follows a simplified audit workflow:

```text
Synthetic banking data
↓
SQL-based control testing
↓
Python exception consolidation
↓
Findings summary
↓
Audit-style executive report
```

---

## Regulatory Areas Covered

### 1. Capital & RWA Testing

This module performs reasonableness testing over simulated regulatory exposure data.

It identifies:

* exposures without regulatory classification;
* exposures without risk weight;
* differences between reported RWA and simplified recalculated RWA;
* concentration of RWA exceptions by exposure class.

Audit objective:

> Assess whether capital and RWA data is complete, reasonable and traceable for prudential reporting purposes.

---

### 2. ICAAP & Risk Appetite Framework Testing

This module reviews whether material risks are properly identified, owned, reviewed, capitalised and monitored against risk appetite limits.

It identifies:

* material risks without assigned internal capital;
* material risks without clear risk owner;
* material risks not reviewed within the expected period;
* RAF breaches;
* RAF breaches not escalated to committee.

Audit objective:

> Assess whether the ICAAP and RAF processes are properly governed, monitored and escalated.

---

### 3. ILAAP Liquidity Risk Testing

This module reviews whether liquidity risk data supports effective monitoring of maturity gaps, funding concentration and liquidity buffer adequacy.

It identifies:

* negative liquidity gaps by maturity bucket;
* liquidity gaps by currency;
* funding concentration by counterparty;
* short-term funding concentration;
* non-eligible assets included in the liquidity buffer population.

Audit objective:

> Assess whether liquidity risk monitoring under ILAAP is supported by reliable, complete and well-controlled data.

---

### 4. IFRS 9 Staging & Expected Credit Loss Testing

This module reviews whether IFRS 9 staging and expected credit loss data are complete, reasonable and consistent with credit deterioration indicators.

It identifies:

* loans with 30+ days past due still classified as Stage 1;
* loans with 90+ days past due not classified as Stage 3;
* significant PD increases not reflected in staging;
* missing PD, LGD or EAD inputs;
* differences between reported ECL and simplified recalculated ECL.

Audit objective:

> Assess whether IFRS 9 staging and ECL outputs are reasonable, traceable and supported by complete model inputs.

---

## Repository Structure

```text
Regulatory-Risk-Audit-Analytics/
│
├── 01_generate_synthetic_regulatory_data.py   # Generates all synthetic datasets
├── 02_generate_audit_findings_summary.py      # Consolidates exceptions and generates audit outputs
│
├── 01_capital_rwa_testing.sql                 # SQL audit tests for Capital & RWA
├── 02_icaap_raf_testing.sql                   # SQL audit tests for ICAAP & RAF
├── 03_ilaap_liquidity_testing.sql             # SQL audit tests for ILAAP
├── 04_ifrs9_staging_ecl_testing.sql           # SQL audit tests for IFRS 9
│
├── 01_capital_rwa_testing_explanation.md       # Audit explanation for Capital & RWA tests
├── 02_icaap_raf_testing_explanation.md         # Audit explanation for ICAAP & RAF tests
├── 03_ilaap_liquidity_testing_explanation.md   # Audit explanation for ILAAP tests
├── 04_ifrs9_staging_ecl_testing_explanation.md # Audit explanation for IFRS 9 tests
│
├── exposures.csv                              # Synthetic credit exposure data
├── rwa_calculations.csv                       # Synthetic RWA calculation data
├── capital_position.csv                       # Synthetic capital position data
├── risk_inventory.csv                         # Synthetic ICAAP risk inventory
├── risk_appetite_limits.csv                   # Synthetic RAF limit data
├── liquidity_cashflows.csv                    # Synthetic liquidity cashflow data
├── funding_sources.csv                        # Synthetic funding source data
├── liquidity_buffer.csv                       # Synthetic liquidity buffer data
├── ifrs9_loans.csv                            # Synthetic IFRS 9 loan data
│
├── findings_summary.csv                       # Consolidated audit findings output
├── audit_summary.md                           # Audit-style executive summary report
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Tools Used

* **Python** — synthetic data generation and audit findings consolidation
* **SQL** — regulatory risk control testing and reasonableness checks
* **Pandas** — data manipulation and exception analysis
* **NumPy** — synthetic data generation

---

## How to Run the Project

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Generate synthetic data

```bash
python 01_generate_synthetic_regulatory_data.py
```

This generates synthetic CSV datasets in the project root.

### 3. Generate audit findings summary

```bash
python 02_generate_audit_findings_summary.py
```

This generates:

* `findings_summary.csv` — consolidated audit exceptions
* `audit_summary.md` — audit-style executive summary report

### 4. Review SQL audit tests

The SQL files can be run independently against the CSV datasets loaded into any SQL-compatible database or tool. They demonstrate Internal Audit control testing logic.

---

## Outputs

The project generates two main audit outputs:

### 1. Findings Summary

File: `findings_summary.csv`

> Consolidates exceptions across Capital & RWA, ICAAP & RAF, ILAAP and IFRS 9.

### 2. Audit Summary Report

File: `audit_summary.md`

> Provides an audit-style executive summary of exceptions, risk ratings, audit interpretations and recommended next steps.

---

## Important Disclaimer

All data used in this project is fully synthetic.

The tests are simplified and are not intended to replicate full regulatory, capital, liquidity or IFRS 9 models.

The purpose of the project is to demonstrate how Internal Audit can use SQL and Python to support:

* data quality testing;
* control testing;
* reasonableness checks;
* exception identification;
* audit evidence;
* risk-based prioritisation.

Final audit conclusions would always require professional judgement, validation with process owners, assessment of data lineage and review of control design.

---

## Professional Positioning

This project reflects my target positioning as a data-driven Internal Audit and Regulatory Risk professional.

It combines:

* financial risk knowledge;
* prudential regulation;
* internal controls;
* audit methodology;
* SQL-based testing;
* Python-based exception analysis.

The objective is not to act as a developer, but as a risk and audit professional capable of using data analytics to challenge processes, test controls and generate better audit evidence.

---
