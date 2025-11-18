# Lira Ticket · CORR “Your Team Performance” Dashboard

## TLDR
- Ship the existing wireframed dashboard inside CORR so customers can see how their SOC reacts once Critical Start escalates a validated alert.
- Anchor the flow in four slices: scenario filters → KPI cards → benchmarked charts → coaching copy that calls out the next action.
- We are done when managers brief leadership in <5 minutes, ≥85% of weeks land in the peer band, and telemetry shows the view in weekly huddles/QBRs.

## Goals & Success Signals
- Give SOC managers a single screen to tell “what happened, why, what’s next” without exporting data.
- Prove ≥70% of recurring coaching cadences touch this module (usage, exports, shares).
- Keep copy and benchmarks deterministic so screenshots feel trustworthy and on-brand.
- When the peer-band KPI drops, the experience surfaces the likely driver within two interactions.

## Users & Jobs
- **SOC/security team manager** – run huddles, coach analysts, justify shifts in staffing or workflow.
- **Analyst team lead** – pair faster analysts with slower peers, balance workload, tune playbooks.
- **Customer security executive / budget owner** – see SLA health versus peers before approving spend.
- **Critical Start engagement lead** – brief joint outcomes without rebuilding charts elsewhere.

## Experience Snapshot (see `team-performance-wireframe.html`)
- **Scenario filters** — Timeframe (4/8/12 weeks), analyst, alert type, alert source; helper text reminds users the entire story respects those choices.
- **KPI stack** — Weekly MTTR, Weeks inside peer band, Median pickup, Alerts per analyst; each shows value, delta vs baseline, icon, and short guidance.
- **Benchmark views** — MTTR vs peer band (line + shaded guardrails), day-of-week volatility (box↔swarm toggle), analyst distribution (MTTR spread↔workload), workload vs MTTR/pickup combo, slowest alert types stacked bars.
- **Narrative cues** — Under every chart, bullets suggest the coaching move (e.g., surge coverage, automation, pairing analysts).

## Tone & Storytelling
- Confident, human, actionable voice; feels like a coaching script instead of a data dump.
- Use Oxford commas, spell out acronyms on first mention, reinforce Critical Start’s transparency and 90% analyst retention proof points.
- Copy should always tie metrics to staffing, workflow, or automation decisions.

## Data & Benchmark Expectations
- Show weekly medians for MTTR and pickup next to deterministic peer medians, quartiles, and ±1σ guardrails.
- Alerts-per-analyst index reflects weekly alerts divided by active analysts so pressure is obvious.
- Weeks-inside-peer-band KPI highlights progress toward the ≥85% target and suggests where to investigate when below target.
- Slowest alert types view combines pickup + resolution time plus alert counts to support playbook or staffing asks.

## Brand & Accessibility Guardrails
- Mirror the gradients, typography, iconography, and card styling in the wireframe and brand kit.
- Maintain contrast so text, cards, and chart elements stay legible on gradient panels.
- Filters and toggles must feel effortless on keyboard and touch; no jitter or clipped focus rings in CORR.

## Scope Guardrails & Assumptions
- `team-performance-wireframe.html` remains the reference for layout, copy, and microcopy until design QA closes.
- Data sources supply alerts, analysts, alert types/sources, and sector benchmarks validated by SOC leadership.
- Stakeholders (brand, product, SOC) sign off on KPI definitions and narrative copy before release.
- Analytics capture filter usage, exports, and dwell time to validate adoption targets.

## Open Questions
- Do SOC leaders need saved filter presets for recurring briefings?
- Should weekends stay visible by default, or do customers expect a business-day lens?
- What export/share path inside CORR best serves execs who need drop-in visuals for decks?
