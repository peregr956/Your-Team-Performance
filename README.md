# Your Team Performance Dashboard

## Background
- Critical Start, headquartered in Plano, Texas, delivers Managed Detection and Response (MDR) and Incident Response (IR) services through CORR, its single-pane collaboration platform.
- The Your Team Performance dashboard lives inside CORR and exposes how a customer’s SOC or security team performs after Critical Start’s 24/7/365 SOC escalates a validated alert.
- MDR is a collaborative workflow: the faster a customer investigates, contains, and closes, the more effective Critical Start can be in minimizing breach risk. This module exists to make those shared touchpoints measurable.

## Audience & Use Cases
- Primary users: SOC/security team managers at Critical Start customer organizations who need coaching-level insight into their analysts.
- Secondary users: customer executives, Critical Start engagement managers, and practice leaders who brief stakeholders on joint MDR outcomes.
- Core use cases:
  - Weekly operational huddles focused on MTTR, pickup speed, backlog pressure, and analyst variance.
  - Monthly/quarterly reviews that benchmark the customer against sector peers to justify staffing, automation, or workflow investments.

## Goals & KPIs
- Show operational metrics (weekly MTTR, time to analyst pickup, alerts per analyst, analyst variance, day-of-week volatility, slowest alert types) alongside sector medians, quartiles, and ±1σ bands.
- Provide configurable filters (timeframe, analyst, alert type, alert source) so every narrative can be scoped before data renders.
- Highlight actionable copy that tells managers what to investigate next, not just what happened.
- Preserve room for strategic KPIs (e.g., percent of weeks meeting SLA targets) when they reinforce coaching or budget conversations.

## Deliverables in This Repo
- `team-performance-wireframe.html`: high-fidelity React + Tailwind prototype with seeded deterministic data, KPI cards, chart components (line + band, box-and-whisker, swarm, stacked bars), and filter interactions.
- `brand/` folder: Critical Start brand system (overview, voice, headline inspiration, visual identity, persona, iconography, boilerplate). Each Markdown file can be shared independently with designers, writers, or partners.
- `brand/README.md`: map of the brand assets plus usage notes (Oxford commas, spell out acronyms on first mention, “Cybersecurity” as one word).

## Prototype Capabilities
- Scenario filter bar scopes the entire experience by timeframe (last 4/8/12 weeks), analyst, alert type, and alert source before any KPI or chart renders.
- KPI stack tracks Weekly MTTR, Weeks inside the peer band (target ≥ 85%), Median time to analyst pickup, and Alerts per analyst with trend tags versus rolling baselines.
- Insight copy under each visualization reinforces Critical Start’s tone—confident, human, actionable—so dashboards double as coaching scripts.
- Brand shell, cards, toggles, and icons match the guidance in `brand/` (gradients, radii, typography, Oxford commas) so designers can lift the UI directly into CORR.

## Chart Inventory & Coaching Prompts
- `LineBandChart`: compares your MTTR line to the shaded sector Q1–Q3 band plus ±1σ guardrails and a dashed sector median for escalation narratives.
- `DowChartContent`: toggles between box-and-whisker and swarm plots to expose day-of-week volatility, alert spread, and weekend hotspots.
- `AnalystBreakdownContent`: flips between MTTR IQR bars and workload counts to connect coaching conversations to actual alert volumes per analyst.
- `ComboBarDualLine`: overlays workload-per-analyst bars with MTTR and pickup lines to flag whether backlog sits in queue acceptance or investigation.
- `SlowTypesChart`: stacks pickup (light) and MTTR (dark) for the ten slowest alert types, including counts, so playbook or staffing requests have data.

## Data Model & Implementation Notes
- `createDashboardData` seeds 12 weeks of alerts (seed `1337`) with analyst names, alert types, sources, pickup times, MTTR, and sector benchmarks for deterministic demos.
- `useTimeframeSlices` applies all filters before computing medians, quartiles, workload, alerts-per-analyst index, and the share of weeks inside the peer band.
- Box, swarm, workload, and slow-type views rely on reusable helpers (`buildDayOfWeekStats`, `buildAnalystStats`, `buildAlertTypeStats`) that translate 1:1 to API responses.
- Open `team-performance-wireframe.html` directly in a browser or serve it locally (`npx serve team-performance-wireframe.html`)—React, Tailwind, and data generation are inlined.
- When wiring to production, replace the synthetic dataset with telemetry-backed APIs, keep medians deterministic per sprint, and preserve copy blocks verbatim for brand compliance.

## Brand & Product Constraints
- Treat the brand guidance as non-negotiable: follow the defined palette, gradients, typography, iconography, tonal cues, and copy rules.
- UI copy must feel confident, human, and actionable—tie every insight back to Critical Start’s promises (contractual SLAs, SOC transparency, analyst retention, continuous improvement).
- Visualizations should remain legible against gradients and tinted panels while passing accessibility guidelines (contrast, focus, keyboard targets).

## Workflow & Implementation Notes
1. Open `team-performance-wireframe.html` in a browser to review the current layout, seeded metrics, and interactions.
2. Validate the KPI definitions, targets, and peer benchmarks with Critical Start product, SOC leadership, and customer success teams.
3. When moving into CORR’s production codebase, confirm component-library parity (spacing, radii, typography) and available charting libraries so the design remains faithful.
4. Plan telemetry/analytics to observe how customers use each module, which filters they rely on, and where follow-up coaching occurs.

## Next Steps
- Run a brand and accessibility audit of the prototype before handoff.
- Align with engineering on data contracts (APIs feeding MTTR, pickup, workload, analyst stats, and sector benchmarks).
- Schedule usability testing with SOC managers to ensure the dashboard supports both operational and strategic decision cycles.