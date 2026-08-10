# Reference: pulse-zine-v16.html

An older, mobile-first "zine" variant of this same Business Pulse report,
kept here purely as a UI/UX reference for features to port into `index.html`.
It is **not** wired to live data (uses hardcoded DEMO/REAL constants) and
should not be treated as a current data source.

## Notable UI elements present here but not in the current `index.html`

- **DEMO / REAL mode toggle** (`#modeSeg`) — a segmented control that swaps
  every `.sw` element's text between a `data-d` (demo) and `data-r` (real)
  value, plus a `.swh`/`.swp` variant for swapping bar heights and track
  widths. Selection persists via `sessionStorage`.
- **"Show Tableau" toggle** (`#tbBtn`) — flips `body[data-tableau]` between
  `on`/`off`, which recolors any `.tbval`/`.tbfill`/`.tbtrk`/`.tbblock`
  element from ink-black to Tableau blue (`--tab: #2F5FED`) to visually flag
  which figures come from the Tableau semantic layer. Also reveals a
  "Why Tableau helps here" section inside the info tooltip.
- **Info/tooltip system** (`.info` circular "i" buttons on each card header) —
  click-to-pin or hover tooltip (`#infoTip`) showing `data-fresh`
  (freshness), `data-src` (source), and `data-tabbenefit` (Tableau benefit
  copy) attributes per card.
- **Metric Cards visibility modal** (`#cardsBtn` → `#cardModalOverlay`) — a
  bottom-sheet modal listing every `[data-key]` card with a checkbox; unchecking
  hides that card (`.hidden-card`) and choice persists via `localStorage`
  (`pulseHiddenCards`).
- **Collapsible card headers** — clicking any card header toggles a
  `.collapsed` state (persisted via `localStorage` key `pulseCollapsedCards`),
  collapsing the card down to just its header. Cards without a natural
  `.hd`/`.ahd` header get one synthesized from `data-title`.
- **Scroll-in card animation** — cards fade/slide in via `IntersectionObserver`
  once ~12% visible, with a staggered `transitionDelay` per card index.
- **Slight per-card rotation** (`.r1`–`.r7` utility classes) for the
  torn-zine/collage aesthetic, reset to `rotate(...) translateY(0)` once
  `.in-view`.
- **"Test against your commit" calculator** (Forecast Stability card) — a
  `$` input + "Set" button that computes gap-to-commit, coverage, and
  linearity live in the browser against the active mode's constants
  (`CONST.real` / `CONST.demo`), rendering a pass/fail "Tracking" verdict
  with a distorted "ransom note" letter styling (`ransom()` helper).
- **Tableau-only cards** (`.tbcard`, e.g. Quota & Attainment, Regional Split,
  Competitive Signal, Pipeline Quality, Coverage vs. 2-Yr History, Deal
  Movement since yesterday/last week, Attrition & NNAOV Risk, Specialist
  Leader Scorecard, Ghost Pipeline, Pipe Gen by Product YoY, High-Risk Stale
  Deals, Q4 Pipeline Readiness) — illustrative cards representing
  Tableau-semantic-layer-only metrics not derivable from Salesforce alone.
- **"Needs attention" triage card** (`.alert`/`.ahd`) — a high-contrast,
  numbered (01–05) severity-triaged list (`.sv.a/.b/.c` = Act now / This week
  / Watch) with heavier border/shadow styling to stand out from regular cards.
- **Only-demo / only-real content blocks** (`.only-demo` / `.only-real`) —
  entire DOM blocks (e.g. different top-10 deal lists) swapped by data mode,
  rather than just text swaps.
