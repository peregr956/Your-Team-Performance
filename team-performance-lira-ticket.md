# Lira Ticket · CORR “Your Team Performance” Module

## TLDR
- Launch the wireframed dashboard inside CORR so customers instantly see how their SOC responds once Critical Start escalates validated alerts.
- Keep the four-slice experience intact: scenario filters → KPI stack → benchmarked charts → coaching copy that states “what to do next.”
- Success = managers can brief leadership in <5 minutes, ≥85% of weeks land inside the peer band, and telemetry shows the module is used in weekly huddles/QBRs.

## Why Now
- SOC managers still stitch MTTR, pickup, and backlog data across tools, so coaching talks feel reactive.
- Existing reports rarely benchmark customers against sector peers, weakening budget or staffing asks.
- The deterministic wireframe already proves the story; customers need it shipping inside CORR with the same brand promise.

## Audience & Jobs To Be Done
- **SOC/security team manager** – narrate “what happened, why, what’s next,” then redirect coaching or surge coverage.
- **Analyst team lead** – pair faster analysts with slower peers, highlight workload fairness, and justify playbook tweaks.
- **Customer security executive / budget owner** – confirm SLA health versus peers before approving headcount or tooling.
- **Critical Start engagement lead** – brief stakeholders on joint MDR outcomes without recreating charts.

## Outcomes & Guardrails
- Managers can retell the last sprint using filters + copy from this module alone.
- ≥70% of weekly huddles/QBRs open this view (tracked via CORR telemetry or export logs).
- KPIs and insights stay deterministic and on-brand so screenshots travel well.
- If the peer-band KPI drops below 85%, the module points to the culprit (analyst, alert type, or day) within two clicks.

## Experience Pillars (per `team-performance-wireframe.html`)
- **Scenario filters** – Timeframe (4/8/12 weeks), analyst, alert type, and alert source selected before data renders; helper text reiterates the scope.
- **KPI stack** – Weekly MTTR, Weeks inside peer band, Median pickup, Alerts per analyst; each shows value, delta vs baseline, icon, and single-line guidance.
- **MTTR vs sector chart** – Solid customer line, dashed median, shaded Q1–Q3 band with ±1σ guardrails; bullet copy prompts managers to flag trend weeks.
- **Day-of-week variability** – Toggle box plot ↔ swarm plot to expose weekend hotspots and recommend staffing or automation shifts.
- **Analyst distribution** – Toggle MTTR spread ↔ workload counts so leaders diagnose whether coaching or coverage matters most.
- **Workload + slow alert storytelling** – Combo bar/dual line ties workload to MTTR and pickup; stacked bars for the ten slowest alert types include pickup + resolution time + alert counts.

## Tone, Copy, and Narrative
- Keep the confident, human, actionable voice from the README; every section reads like a coaching script, not a data dump.
- Insight bullets under each visualization tell users what to investigate next.
- Follow brand rules: Oxford commas, spell out acronyms on first mention, highlight Critical Start’s transparency and 90% analyst retention promise.

## Filters & Interaction Principles
- Filters act globally; nothing renders until a scenario is chosen, preventing stale data flashes.
- Default to the last 12 weeks; quick pivots to 4 or 8 weeks support sprint and quarterly storytelling.
- Analyst filter tightens the Analyst Distribution card while other views still show peer context.
- Day-of-week and analyst toggles remember the last selection in-session to reduce rework.

## Data & Benchmark Expectations
- Weekly medians for MTTR and pickup compared to deterministic sector medians, quartiles, and ±1σ guardrails.
- Alerts-per-analyst index = weekly alerts ÷ count of active analysts so pressure is obvious.
- Weeks-inside-peer-band KPI shows progress vs the ≥85% target and explains the implication when it falls short.
- Slowest alert types view merges pickup + resolution time plus total alert counts to back staffing or playbook requests.

## Accessibility & Brand Commitments
- Use the Critical Start gradients, typography, radii, and iconography exactly as in the wireframe.
- Preserve contrast ratios so cards, text, and chart elements remain legible on gradient panels.
- Filters and toggles must meet keyboard/focus requirements and feel confident when used in demos.

## Dependencies & Assumptions
- `team-performance-wireframe.html` remains the layout and copy source until design QA signs off.
- Telemetry-backed data feeds supply alerts, analysts, alert types/sources, and peer benchmarks validated by SOC leadership.
- Brand, product, and SOC partners approve KPI definitions, thresholds, and copy before handoff; analytics instrumentation captures filter usage, exports, and dwell time.

## Open Questions
- Do we need saved filter presets for recurring leadership briefings?
- Should weekends stay visible by default, or do customers expect a business-day lens?
- What share/export flow inside CORR best fits executives who need snapshots for decks or emails?
