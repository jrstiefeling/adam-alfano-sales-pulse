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

## Interactive controls

The controls bar under the masthead adds, all client-side and all persisted in
this browser only:

- **Real / Demo** — Demo swaps every headline figure and deal list for invented
  round-number placeholders on fictional accounts, for screen-sharing or
  walkthroughs. **Real is the default**, and demo mode shows a permanent banner;
  the verification notes and the data-source footer are hidden while it is on,
  because they describe the real run. `?mode=demo` forces it for one visit.
- **Show Tableau** — tints every figure read straight from the Tableau Next SDM
  blue. Daily-target-sheet figures, Salesforce SOQL fields (Stage, MFJ, Org62
  links) and on-page arithmetic (gaps, YoY, velocity) deliberately stay black.
- **Metric Cards** — check/uncheck sections to hide them.
- **(i) on any card header** — freshness and source for that card, plus a
  "why Tableau helps here" note while Show Tableau is on.
- **Click a card header** — collapses it to just the header.

## Data sources

Generated from Tableau Next SDM `Sls_Forecasting_Metrics_Expanded` via
`analyze_data`, with Salesforce SOQL used for record links and
stage/forecast-judgment lookups. See the report footer and each card's
"verification details" for full methodology and caveats.

## Updating the snapshot

Each report is a point-in-time snapshot (see the masthead for the exact
timestamp). To add a new snapshot, replace `index.html` and commit — git
history preserves prior snapshots for comparison over time.

## Reference material

`reference/` holds prior design iterations kept only for UI/UX reference
(not live data sources). See `reference/README.md` for a breakdown of the
notable UI patterns in each one.
