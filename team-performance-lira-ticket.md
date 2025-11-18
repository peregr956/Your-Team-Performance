# Lira Ticket: CORR Your Team Performance Dashboard

## TLDR
- Productize the “Your Team Performance” dashboard inside CORR so customers see how their SOC responds after Critical Start escalates validated alerts, matching the README narrative.
- Deliver scenario filters, coaching-ready KPIs, and benchmarked charts from `team-performance-wireframe.html`, preserving tone, copy, and brand shell.
- Serve SOC/security team managers first, ensuring they can run weekly coaching huddles and executive briefings without stitching data from other tools.
- Consider the module done when experiences mirror the wireframe, filters feel trustworthy, and adoption proves users rely on it for staffing, workflow, and SLA decisions.

## Problem & Opportunity
- Managers lack a single-pane story that connects pickup speed, MTTR, and backlog after Critical Start’s SOC hands off an alert.
- Current reporting seldom compares customer performance to sector peers, making it hard to justify coaching or investment.
- Without scoped filters, narratives stay generic and cannot identify which analysts, alert types, or sources drive delays.
- Turning the deterministic wireframe into a CORR module anchors conversations in human, actionable insights instead of raw metrics.

## Who We Serve & Key Jobs
- **SOC/security team manager**: coach analysts, spotlight bottlenecks, and walk leadership through “what happened, why, what’s next.”
- **Analyst team lead**: pair faster analysts with slower peers, plan surge coverage, and align playbooks with observed workload.
- **Customer security executive / budget owner**: benchmark MTTR and SLA adherence before approving staffing, automation, or tooling.
- **Critical Start engagement manager or practice leader**: brief stakeholders on joint MDR outcomes and prioritize follow-up sessions.

## Desired Outcomes & Success Measures
- Managers can explain the last sprint’s performance in under five minutes using filters, KPIs, and insight copy.
- ≥85% of monitored weeks stay inside the peer performance band, or the module clearly flags why not with narrative prompts.
- At least 70% of weekly huddles or QBRs reference this module (measured via CORR telemetry or export tracking).
- Users share or export the dashboard confidently because copy, visuals, and benchmarks stay deterministic and on-brand.

## Experience Overview (reference `team-performance-wireframe.html`)
- **Scenario filters first** — Timeframe (4/8/12 weeks), analyst, alert type, and alert source must be selected before any KPI or chart renders; helper text reminds users the filters scope the entire story.
- **KPI stack** — Four cards (Weekly MTTR, Weeks inside peer band, Median time to analyst pickup, Alerts per analyst) show value, trend tag vs baseline, icon, and subcopy explaining action.
- **MTTR vs sector benchmarks** — Solid customer line against shaded Q1–Q3 peer band with ±1σ guardrails and dashed sector median; bullets prompt managers to highlight trend weeks and drill into filters.
- **Day-of-week variability** — Toggle between box-and-whisker and swarm plots to expose volatility, weekend hotspots, and recommended actions from the insight list.
- **Analyst performance distribution** — Toggle between MTTR spread and alerts-per-analyst counts to pair workload with coaching cues.
- **Workload & slow alert storytelling** — Combo bar + dual line links workload per analyst with MTTR/pickup trends; slowest alert types chart stacks pickup and resolution times with counts so playbook or staffing asks feel justified.

## Content & Narrative Requirements
- Maintain the confident, human, actionable tone from the README and prototype; every module section should read like a coaching script.
- Keep insight bullet lists under each visualization so the dashboard states what to investigate next, not only what happened.
- Follow brand copy rules (Oxford commas, spell out acronyms on first mention, reinforce Critical Start promises like 90% analyst retention).
- Tie every call-to-action to staffing, workflow, or automation decisions so business stakeholders hear a clear “so what.”

## Filters & Interaction Behaviors
- Filters apply globally before KPIs render, preventing momentary flashes of stale or irrelevant data.
- Default timeframe is the last 12 weeks, with quick pivots to 4 or 8 weeks for sprint or quarterly storytelling.
- Analyst selection narrows analyst-specific views while the rest of the module still references sector benchmarks for context.
- Day-of-week and analyst toggles remember the last selection during a session to reduce friction across multiple conversations.

## Data & Benchmark Requirements
- Display weekly medians for MTTR and pickup alongside deterministic peer medians, quartiles, and ±1σ guardrails.
- Calculate alerts-per-analyst index using the count of active analysts per week so workload pressure is obvious.
- Surface the Weeks inside peer band KPI with its ≥85% target and explain what falling short implies.
- Slowest alert types view combines pickup and resolution duration plus alert counts, enabling concrete staffing or playbook decisions.

## Accessibility & Brand Commitments
- Apply Critical Start gradients, typography, iconography, and card treatments exactly as in the wireframe and brand kit.
- Preserve contrast ratios for cards, text, and chart elements so the module remains legible against gradient backdrops.
- Ensure filter controls and toggles meet focus, keyboard, and hit-area standards for accessibility.
- Reinforce Critical Start’s transparency and retention promises whenever performance narratives mention trust or coverage.

## Dependencies & Assumptions
- `team-performance-wireframe.html` remains the canonical reference for layout, copy blocks, and microcopy until design QA completes.
- Telemetry-backed data sources provide alerts, analyst metadata, alert types, sources, and sector benchmarks validated by SOC leadership.
- Brand, product, and SOC stakeholders sign off on KPI definitions, thresholds, and narrative copy before handoff.
- Analytics instrumentation will capture filter usage, exports, and dwell time to guide future iterations.

## Open Questions & Follow-Ups
- Do we need saved filter presets for recurring leadership briefings, or is manual selection acceptable for launch?
- Should weekend behavior remain visible by default, or do customers expect business-day-only narratives?
- What share/export mechanism inside CORR best supports executives who need snapshots for decks or emails?
- How will we capture qualitative feedback from SOC managers during early access to confirm the module’s coaching utility?
