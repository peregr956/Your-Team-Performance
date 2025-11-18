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