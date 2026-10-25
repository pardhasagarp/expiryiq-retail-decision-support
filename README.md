# ExpiryIQ

**Evidence-led expiry and waste decision support for independent UK convenience stores**

ExpiryIQ is a working proof-of-concept for a lightweight decision-support layer that sits alongside existing EPOS/till data. It combines SKU-level sales and stock information with batch-level expiry records so that a retailer can identify stock requiring action, distinguish food-safety dates from quality dates, record waste and use expiry information when reviewing reorder decisions.

## Project scope

The project focuses on **single-site independent UK convenience stores** with digital till/stock data and short-life product ranges. It does not attempt to replace an EPOS platform. The current artefact demonstrates functional feasibility with **synthetic demonstration data**; it does not claim live retailer adoption, realised waste reduction or validated willingness to pay.

## Key functions

- EPOS/CSV-oriented product and stock workflow
- batch-level expiry capture
- use-by and best-before date handling
- prioritised expiry action queue
- transparent at-risk stock logic
- advisory markdown prompts
- waste-cost recording
- expiry-aware reorder support
- operational reports and evidence/rule view

## Repository structure

```text
expiryiq-retail-decision-support/
├── README.md
├── .gitignore
├── index.html
├── data/
│   └── ExpiryIQ_Synthetic_Sample_Data.csv
├── models/
│   └── ExpiryIQ_Final_Financial_and_Evidence_Model.xlsx
└── docs/
    ├── ExpiryIQ_Artefact_Overview.pdf
    └── EVIDENCE_MAP.md
```

## Run the prototype

The artefact is self-contained and has no external package dependencies.

1. Clone or download the repository.
2. Open `index.html` in a modern browser.
3. Use the left navigation to inspect the dashboard, expiry queue, batch capture, waste log, reorder support, reports and evidence/rules views.

For local HTTP serving:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/`.

## Evidence and modelling

The financial/evidence workbook contains the current market evidence, competitor benchmark, bottom-up sales funnel, 12-month cash-flow scenario, three-year planning model, sensitivity analysis, KPI gates and risk register.

See [`docs/EVIDENCE_MAP.md`](docs/EVIDENCE_MAP.md) for the role of each repository item.

## Evidence boundary

The prototype uses synthetic records to test logic and presentation. Commercial assumptions such as price, conversion rates, acquisition targets and operating costs are planning scenarios unless explicitly identified as published evidence. Real customer demand, actual waste reduction and return on investment require a controlled live-store pilot.

## Academic submission boundary

The assessed business plan, ethics documentation and detailed research log are intentionally not published in the public repository. They remain part of the private academic submission/evidence pack.
