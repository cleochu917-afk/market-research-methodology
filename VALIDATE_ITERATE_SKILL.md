---
name: validate-and-iterate
description: Use this skill when setting up instrumentation, running validation tests, collecting qualitative feedback, and operating the continuous discovery loop for a live product. Follows Stage 4+5 (Brand System, Product Specification, Strategic Direction). Produces Stage 6 (Validate) and Stage 7 (Iterate) outputs.
---

# Validate and Iterate — SKILL

**Phase position:** Follows Stage 4+5 terminal documents. The product exists and is in the hands of real users. Stage 6 validates the committed decisions from the Stage 4+5 outcome layer. Stage 7 is the continuous loop with no end point.
**References:** `/method-bank/metrics-setup.md` for the full metric derivation procedure and product type taxonomy.

---

## Core production discipline

**Instrumentation precedes testing.** Define the metric, measurement method, and decision threshold before the first user touches the product. A result without a pre-specified threshold is a data point, not a decision.

**Every committed decision has a metric.** Each item in the Stage 4+5 outcome layer marked Committed or Conditional requires one metric block: metric name · measurement method (specific event names) · supporting metrics · threshold · what happens when threshold is crossed.

**One North Star Metric.** A single behaviour-based metric that, if it moves up, confirms users are getting the core value the product was designed to deliver. Everything else is a supporting metric or a guardrail. See `/method-bank/metrics-setup.md` for how to derive it from Stage 3 findings.

**Three tests before shipping any metric definition:**
1. Is it behaviour-based, not vanity? ("redirected into mode" vs "app opens")
2. Can the product team directly influence it?
3. If it goes up, does core user value go up?

If not — it is the wrong metric.

**The dashboard is a tool, not a report.** The live dashboard is opened daily by the team. If a metric on it has not changed a decision in 30 days, remove it.

**Qualitative feedback explains what quantitative data shows.** The dashboard shows where users drop off. The four feedback methods show why. Both are required — neither replaces the other.

---

## Stage 6 — Validate

### Step 1: Derive the North Star Metric from Stage 3

Before defining any supporting metrics, define the North Star. The procedure is in `/method-bank/metrics-setup.md`. The short version:

1. Identify the product's engagement model (Attention / Transaction / Productivity / Transformation — see metrics bank for definitions)
2. State the core value event — the single action a user takes that proves they received the product's core value
3. The North Star is the rate or frequency of that core value event among active users

For an experiential/wellbeing product like the food noise app: the core value event is "redirected into mode at capture confirmation." The North Star is redirect rate — not app opens, not captures alone.

### Step 2: Build the metric tree

The metric tree shows what inputs drive the North Star. Structure:

```
North Star Metric
├── Input 1 (what must happen for NSM to be possible)
├── Input 2
├── Input 3
└── Guardrail (what NSM improvement must not come at the cost of)
```

Each input metric is an instrumentation target. Each guardrail has a hard threshold.

### Step 3: Define instrumentation blocks

One block per committed product decision from the Stage 4+5 outcome layer. Format:

- **Decision:** exact wording from outcome layer
- **Primary metric:** the single metric this decision's success hinges on
- **Measurement method:** specific event names, calculation
- **Supporting metrics (2–4):** what explains why the primary moved or didn't
- **Guardrail:** what this decision could inadvertently break, with a hard threshold
- **Action threshold:** the value at which a review is triggered
- **Owner:** PM / Design / Eng / Trio
- **Time horizon:** Short (days 1–14) or Long (Month 1+)

### Step 4: Define the success condition

Before Stage 6 begins, state in one line what "working" looks like. Format:

"Product is working if [Metric A] >[threshold] AND [Metric B] >[threshold] AND [North Star] >[threshold]."

All conditions must hold simultaneously. A single metric win with other conditions failing is not product health.

---

### Qualitative feedback — four methods

The feedback methods are selected based on the question type, not scheduled in advance. The question comes from the dashboard.

| Question | Method | Format |
|---|---|---|
| Why did users behave unexpectedly at [step]? | Intercept interview | 5–10 min · in-context · no advance recruitment |
| Did the product actually change the phenomenon? | Group interview (reconvened Stage 3 participants) | 60 min · 4–6 participants · semi-structured |
| Is the product's underlying mechanism coherent? | Expert interview | 45 min · domain expert · phenomenon knowledge |
| What would fix [specific friction point]? | Co-creation session | 90 min · full product trio present · not delegated |

**Intercept interviews:** approach current or recent users in the contexts where the phenomenon occurs. 2–3 questions maximum, all anchored to the most recent session. Capture exact vocabulary — not paraphrase. Any word not in the Stage 3 vocabulary logs is a finding.

**Group interviews:** reconvene Stage 3 research participants who have been using the live product for at least 2 weeks. Three phases: individual account first (15 min), then shared comparison (25 min), then forward projection (20 min). The before/after comparison is the strongest signal for whether the product addresses the phenomenon. Only possible because Stage 3 produced a baseline.

**Expert interviews:** show the live product to domain experts. Ask: "Does this intervention make sense given what you know about this phenomenon?" and "What failure mode would you predict?" Any testable claim about the mechanism becomes an A/B test hypothesis.

**Co-creation sessions:** the product trio (PM, designer, engineer) runs the session — not a researcher intermediary. Show the friction point. Let participants interact with it and propose solutions. The team listens and records. Commit to one direction based on what emerged before the session closes.

---

### A/B test tracker — minimal format

One row per test. The result column contains the number. The decision column contains the action. Interpretation goes in the learning log, not the tracker.

| # | What was tested | Primary metric | Sample size | Result | Significance | Decision |
|---|---|---|---|---|---|---|

**Decision values:** Committed (ship, update relevant document) · Revise + retest (state revised hypothesis and timeline) · Drop (question answered by other evidence — document why).

**Minimum sample size:** 200 per variant for most consumer product metrics. Less produces confidence intervals too wide to act on.

---

### Validation decision record

At the end of Stage 6, record:

1. **Confidence tier upgrades:** which Stage 3 Directional findings are now Validated (or downgraded) based on live product data. Downgrades are as important as upgrades.

2. **Pivot or persevere:** Persevere (enter Stage 7 continuous loop) · Partial pivot (specific documents updated, affected flows redesigned) · Structural pivot (core mechanism is not producing the intended effect — return to Stage 3 convergence with live data as input).

---

## Stage 7 — Iterate

Stage 7 has no end point. It is a standing operating cadence, not a project.

### Live dashboard

**Metric hierarchy:**
- **North Star Metric** — reviewed weekly, acted on monthly
- **Input metrics** — reviewed weekly, acted on when threshold crossed
- **Guardrail metrics** — reviewed daily, acted on immediately if threshold crossed
- **Diagnostic metrics** — reviewed when a threshold is crossed elsewhere, not monitored continuously

**Removal rule:** if a metric has not changed a decision in 30 days, remove it from the dashboard.

**Three metric categories every product dashboard requires:**

*Behaviour metrics* — what users do: activation rate, retention (Day 1, 7, 30), core action frequency.
*Experience metrics* — where the experience breaks: drop-off by step, session completion, post-session affect, feature usage.
*Outcome metrics* — does the product change anything: the North Star Metric and 1–2 downstream outcomes tied to the product's core value proposition. These are the hardest to measure and the most important. Never omit them.

### Signal detection + auto-update

Continuous discovery in an AI-augmented system is not a calendar-driven cadence — it is an event-driven signal detection layer. When a signal crosses its threshold, an update is triggered. The system does not wait for a weekly review.

**Four signal types:**

- **Metric signal:** a dashboard metric crosses its pre-specified action threshold for 48+ consecutive hours. Guardrail metrics fire immediately on first crossing — no 48-hour condition.
- **Experiment signal:** an A/B test result reaches statistical significance (p <0.05) with minimum sample size met.
- **Qualitative signal:** a feedback session produces a finding marked → design review by the session facilitator. Trigger is the marking, not the session end.
- **Anomaly signal:** the same unexpected behaviour is observed in 3+ independent users within a 14-day rolling window. Single observations are logged only — patterns trigger review.

**Propagation rules — signal type to documents updated:**

| Signal | Documents updated |
|---|---|
| Metric | Product Specification (flow or constraint) · Stage 6 instrumentation · Learning log |
| Experiment | Brand System or Product Specification (the document containing the resolved decision) · A/B tracker (decision column) · Stage 3 convergence output layer (confidence tier) |
| Qualitative | Stage 3 journey map · Strategic Direction · A/B backlog (new hypothesis if generated) |
| Anomaly | Stage 3 journey map (new behaviour entry) · Product Specification open questions · Strategic Direction insight bridge (if new unaddressed need) |

**Four conditions requiring human review before any update is committed:**
1. Signal contradicts a Validated (not just Directional) Stage 3 finding
2. Redirect rate below threshold for 14+ consecutive days — structural pivot decision required
3. Anomaly with no prior hypothesis — schedule 3 user calls before any document update
4. All Phase 1 success conditions met — Phase 2 promotion requires human sign-off

### Learning log

Three entry types — one entry per week minimum:

**Pattern:** a behaviour or signal appearing consistently. State: the pattern, the evidence, whether it was predicted. If not predicted — flag for document update review.

**Failure:** a feature, flow, or assumption not working as designed. State: what was expected, what happened, the specific decision it requires. Every failure entry ends with: → test hypothesis / → design review / → escalate.

**Unexpected:** something the team did not anticipate. Log first. Do not explain immediately. "What are the 3 users who show this behaviour doing?" — schedule calls before any design decision is made.

### Document update protocol

Stage 7 is the layer that makes the system AI-augmentable. When a signal crosses a threshold, specific prior documents update. The update is recorded with: date, triggering signal, documents changed, changed by.

**Update trigger types and the documents they affect:**

| Trigger | Documents updated |
|---|---|
| A/B test committed result | Brand System (copy updated) · Product Specification (interaction constraint updated) · Confidence tier table (Stage 6) |
| Dashboard metric crosses threshold | Product Specification (relevant flow or constraint) · Stage 6 instrumentation (threshold revised if needed) |
| Group interview confirms/contradicts Stage 3 finding | Stage 3 journey map · Stage 3 convergence output layer (confidence tiers) · Strategic Direction Section 03 (product decisions) |
| Learning log → design review | Product Specification (open questions) · Stage 6 learning log |
| Phase 2 promotion | Product Specification (MVP scope block) · Stage 6 instrumentation (new metric blocks for Phase 2 features) |
| Structural pivot | Return to Stage 3 convergence. All documents from Stage 4+5 forward are on hold pending revised synthesis. |

---

## Common failure modes

**Instrumentation defined after testing starts.** Post-hoc thresholds are rationalisation. Define them before the product ships.

**North Star is a vanity metric.** "App opens" or "downloads" do not tell you whether the product delivered its core value. A behaviour-based metric tied to the core value event is required.

**Dashboard has too many metrics.** A team monitoring 20 metrics monitors none of them effectively. Start with 6–8. Remove any that have not changed a decision in 30 days.

**Qualitative feedback delegated away from the product trio.** The people building the product must hear users directly. A researcher report is not a substitute. At least one weekly touchpoint must involve the full trio without intermediary.

**Unexpected learning log entries explained immediately.** The impulse to explain an unexpected signal before understanding it produces premature hypotheses. Log it first. Schedule calls. Understand before deciding.

**Documents not updated when signals cross thresholds.** The document update protocol is not optional. If the Product Specification still says ≤2 taps when live data shows users need 3, the spec is wrong and the engineering team is working from an incorrect brief.

**Structural pivot treated as failure.** A structural pivot triggered by Stage 6 data means the research methodology worked — a false assumption was caught before growth investment. It is not a failure. It is the system functioning correctly.

---

*Skill developed through the vibe eating app research session, June 2026. Metric derivation procedure in `/method-bank/metrics-setup.md`. North Star framework grounded in Amplitude product engagement model taxonomy (2023). HEART framework: Google research team (2010). Continuous discovery cadence: Torres (2021). Metric tree structure: Reforge growth framework.*
