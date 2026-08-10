# Adam Alfano — President Sales Pulse

A self-contained, single-file HTML snapshot report tracking Adam Alfano's sales
performance for FQ3 FY2027 (Aug–Oct 2026).

**⚠️ Confidential.** This report contains internal deal names, account names,
ACV/Commit figures, and direct Salesforce record links. Keep this repository
private and do not share its contents externally.

## Contents

- `index.html` — the report snapshot. Open it directly in a browser (no build
  step or server required).

## What's in the report

- Daily / Monthly / Quarterly business-won KPIs vs. targets and Commit
- AE spotlight (top MTD deal)
- Daily velocity chart and per-leader "daily horse race"
- Top 10 deals closed (today / MTD) and top 10 open deals closing (today / this month)
- Deal movement since the prior snapshot
- Watchlist of at-risk (UP−/OUT) open-pipe deals
- Per-card "AI Trust" verification notes documenting data sources and methodology

## Data sources

Generated from Tableau Next SDM `Sls_Forecasting_Metrics_Expanded` via
`analyze_data`, with Salesforce SOQL used for record links and
stage/forecast-judgment lookups. See the report footer and each card's
"verification details" for full methodology and caveats.

## Updating the snapshot

Each report is a point-in-time snapshot (see the masthead for the exact
timestamp). To add a new snapshot, replace `index.html` and commit — git
history preserves prior snapshots for comparison over time.
