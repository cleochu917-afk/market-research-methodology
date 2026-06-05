[PRODUCE_STRUCTURED_INSIGHTS_SKILL (1).md](https://github.com/user-attachments/files/28642381/PRODUCE_STRUCTURED_INSIGHTS_SKILL.1.md)
---
name: produce-structured-insights
description: Use this skill when producing structured insights from fieldwork — running active data collection, synthesising evidence into named insights, and producing the terminal outputs that feed Stage 4. Follows Stage 2 Design How to Investigate It. Precedes Stage 4 Translate Insight into Decisions.
---

# Produce Structured Insights — SKILL

**Phase position:** Follows Stage 2 (Design How to Investigate It). The Stage 2 composite summary and participant screener must exist before Stage 3 begins. Precedes Stage 4 — Translate Insight into Decisions.
**Role perspective:** UX owns fieldwork execution and participant logistics. Experience design owns qualitative synthesis and insight production. Full team owns convergence sprint and terminal outputs.
**Output:** Three working files — fieldwork (participant selection, EMA design, instruments, IDI guide, rapid prototyping), synthesis (cultural analysis, QES log, affinity diagram, quantitative integration, journey map, usability report), convergence (sprint, rapid prototype backlog review, terminal outputs).
**A/B metrics:** Consult `/method-bank/ab-metrics-bank.md` before designing any rapid prototype test. Metric selection depends on product type and the decision being resolved.

---

## Core production principles

**Write to enable decisions, not demonstrate thinking.** Every sentence must answer: what does this mean for action? If a sentence does not change a decision, remove or compress it.

**Plain language first.** Replace abstract phrasing with observable behaviour. Not "experiential tension" — say "users feel X and respond by doing Y." One idea per sentence.

**Action-oriented outputs.** Phrase findings as implications: not "users struggle with X" but "this means the product must X." Every insight leads to: *therefore we should / must / should avoid.*

**Tie claims to data.** "Across IDIs and event captures..." "Observed in 6/8 participants..." Avoid unsupported generalisations — remove "generally", "often", "usually." Use specific signals.

**Confident but not over-claimed.** Use "suggests", "indicates", "points toward." With small samples: signal direction, not certainty. A/B results at Stage 3 scale (n=8–12) are always Directional at most.

**Only include content that guides production.** No explanatory prose defending methodology. No definitions of canon concepts. No footnote citations. No meta-language about what a stage ensures or allows. Content is in the document only if it changes a production decision.

**Vocabulary:** prefer pattern, behaviour, moment, context, trigger, response, outcome. Avoid: phenomenological, ontological, structural tension (unless defined), theoretical frame.

**Stay at one level per section.** Behaviour level, experience level, or system level — do not jump between them in the same paragraph.

**Lead with conclusion.** Weak: "Users experience anticipatory tension around food." Strong: "Users experience anticipatory tension before acting on cravings, which means the product must provide an immediate outlet at that moment rather than after the fact."

---

## File 1 — Active fieldwork

### Participant selection (Tab 01 — do this first)

**Two-stage criteria.** Stage 1 criteria are specified now. Stage 2 criteria are derived from the Stage 2 composite summary after it exists — not before.

**Stage 1 — specify now:**
- Minimum threshold: phenomenon must be present at sufficient frequency for the capture protocol to produce adequate data (e.g. 3–4 food noise events per day minimum)
- Welfare exclusions: clinical severity conditions that make the protocol inappropriate (e.g. active eating disorder diagnosis)
- Medication/confound exclusions: conditions that would suppress or alter the phenomenon being measured
- Capture capacity: willingness and ability to self-initiate a capture within 30 minutes of onset

**Stage 2 criteria derivation — derive from composite summary using three questions:**
1. Which findings are thin? (Portrait types, contexts, or registers where Stage 2 data was insufficient — over-recruit to fill these gaps)
2. Which findings have no prior equivalent? (These are the highest-priority for Stage 3 — recruit participants who can confirm, extend, or show the limits of these findings)
3. Which portrait boundaries dissolved? (Recruit to the boundary condition, not to represent a type)

**Sample size:** 8–12 participants completing the full protocol. Saturation, not number, determines adequacy.

**Extreme and mainstream balance:** Minimum 2 extreme-case participants (highest intensity, most unusual pattern, most contradictory data). Minimum 4 mainstream participants (most common portrait profiles from Stage 2). Do not moderate all participants identically — extreme cases need more probing time on their specific dimension.

**Primary pool:** Stage 2 ESM completers at 70%+ compliance — longitudinal continuity produces a richer analytical base. If unavailable, recruit fresh participants using Stage 2 criteria as the baseline screener.

---

### EMA design (Tab 02)

**Minimum viable study — if time is constrained, run only these two:**
- Event-contingent capture: 7-day self-initiated protocol. Irreducible core — without it, Stage 3 adds nothing to Stage 2.
- IDIs: 60-minute sessions anchored to participant captures, Phases 1, 2, and 4 only.

Everything else (signal-contingent ESM, four instruments, usability testing) adds depth, coverage, and quantitative signal. Drop in this order if time-constrained: instruments first, then signal-contingent ESM, then usability testing. Fewer methods means lower confidence tiers — not shortcuts in the analysis. The full analytical procedure runs regardless of which methods were used.

**Protocol 1 — Signal-contingent (Secondary):**
- 5 signals per day, semi-random within known peak windows, minimum 2-hour gap between signals
- Fixed items: phenomenon present Y/N, intensity 1–5, current activity, location, elapsed time since last meal
- Variable probe: one rotating question per session, designed from Stage 2 composite summary — not from prior market research assumptions
- 30-minute confirmation window: captures initiated more than 30 minutes after onset are flagged retrospective and excluded from moment-capture analysis

**Protocol 2 — Event-contingent (Primary):**
- Participants self-initiate immediately when the phenomenon hits
- 30-minute confirmation window: first question confirms the event occurred within 30 minutes
- Four capture options (participant chooses the least friction one — frictionless by design, depth comes in the IDI not the capture):
  - 30-second voice note (most analytically rich — captures embodied and emotional language before editing)
  - Photo of environment (captures trigger context that interview recall cannot reconstruct)
  - Intensity + one sentence completion ("Right now it feels like ___")
  - Intensity only (fallback — minimum data, temporally valid)
- Training before study begins: 15-minute onboarding call using participant's own Stage 2 diary entries as examples of the target moment

**Documentation format — event-contingent capture log:**
One row per capture. Fields: Capture ID (participant + day + sequential number) · Type (voice/photo/sentence/rating) · Verbatim (exact transcript — never paraphrase at this stage) · Intensity · Proximity confirmed (Y/N — N entries excluded from moment-capture analysis) · Trigger context (what the participant was doing immediately before) · Researcher first response (written before comparing to other entries) · Tension flag (does this contradict another entry, prior market research, or the Stage 2 composite summary?)

---

### Instruments (Tab 03)

**Instruments are selected per study, not fixed.** The four instruments documented in the fieldwork file (collage, attention map, card sort, environment walkthrough) are the selection made for this specific study. A different research question requires a different selection. See `/method-bank/fieldwork-instruments.md` for the full bank and `/method-bank/INDEX.md` for the selection framework.

**Selection procedure — run before specifying any instrument:**

Four categories. One suitability question per category. If yes — at least one instrument from that category is required.

| Category | Suitability question | Produces |
|---|---|---|
| **SAY** | Does the research question require how participants consciously position themselves — stated values, vocabulary, self-report? | Conscious attitudes, participant vocabulary, self-positioning |
| **DO** | Does it require actual behaviour in context or temporal/spatial distribution of the phenomenon? | Behaviour in situ, environmental affordances, temporal pattern |
| **MAKE** | Is the phenomenon pre-verbal, somatic, or identity-adjacent — below the threshold of easy articulation? | Tacit knowledge externalised in non-verbal form |
| **ENACT** | Is the phenomenon situational or decision-dependent — occurring only under specific conditions? | Edge cases, contextual breakdowns, embodied responses |

*SAY and MAKE are not interchangeable. SAY reaches what participants can articulate. MAKE reaches what they cannot. If the phenomenon has both dimensions, both categories are required.*

*ENACT instruments produce directional, not evidential data. Always pair with event-contingent capture for real-time evidence. Roleplaying and bodystorming run within IDI Phase 3 — they are not standalone sent instruments.*

**For each selected instrument, document:**
Prompt (exact wording sent to participant) · What it produces (one sentence) · Documentation format (fields captured, verbatim requirement) · Which synthesis output it feeds · Timing within the study period.

**Primary instruments must run.** Secondary instruments add depth — drop before trimming IDI phases if time-constrained. Fewer instruments means lower confidence tiers on the findings they would have produced — not shortcuts in analysis.

**IDI documentation format — complete within 2 hours of session close:**
Transcript (verbatim — include [pause Xs], [incomplete], [laughs]) · researcher post-session note (written before reading transcript: what surprised you, what the participant corrected) · member check result (what description was presented in Phase 4, participant response: recognition/partial/correction, and the specific correction if made — corrections enter the QES log as tension flags) · capture-to-IDI links (what each IDI probe added that the raw capture could not show).

---

### IDI guide (Tab 04)

Before the session: select 4–5 specific captures for analytical interest — unexpected language, clear trigger context, or contradiction with signal data. Review all instrument outputs. Identify whether this participant is an extreme or mainstream case for the question you most need to probe.

**Phase 1 — Opening (5 min, Primary):**
Ask about the study experience, not the phenomenon directly. What did they want to capture but couldn't?

**Phase 2 — Capture walkthrough (25 min, Primary):**
Present each selected capture. Anchor every question to the specific capture.
- "Take me back to this moment. What was happening right before it started?"
- "Where did you feel it — was it in your body somewhere?"
- "You rated this a [X] — what would a [X+1] feel like? A [X-1]?"
- [For voice notes with unexpected language]: "You said '[phrase]' — tell me more about that word."
- [For photos]: "What in this image is connected to the [phenomenon]? What isn't?"

*Probe the trigger condition at every capture: "What were you doing right before it started?" This is the dimension most likely to surface findings the prior research did not reach.*

**Phase 3 — Instrument depth (20 min, Secondary — skip if time-constrained):**
Use collage and card sort as prompts. Probe tensions between instruments and captures.
- "You put [word] in 'feels true' — when did that become true for you?"
- "In your attention map you showed it starting at [X], but in your captures it seemed to start earlier — what's the difference?"
- "If [phenomenon] went away completely — what would be missing?"

**Phase 4 — Validation and close (10 min, Primary):**
Present one or two descriptions of the experience from the Stage 2 composite summary. Ask whether they fit.
- "Does this describe what it's like for you? What fits, what doesn't?"
- "Is there anything about your experience we haven't touched on?"

**Moderation principles — apply at every phase:**
- Pursue the unexpected. Follow it before returning to the guide.
- Work in the participant's vocabulary. If they use a different word for the experience, use it back.
- Probe the body at every emotional or cognitive description: "When you feel that — where do you feel it?"
- Do not fill pauses. Wait at least 5 seconds before rephrasing.

---

### Rapid prototyping (Tab 05)

A rapid prototype comparison exposes a small number of participants to two variants and collects observational data on which variant produced the better behavioural signal. This is not an A/B test — there is no live product, no real user base, and no statistical significance. Output is a directional finding, not a test result. Real A/B tests run in Stage 6 against a live product.

**Source of high-risk decisions:**
- Stage 1 Constraints document ("Will not / Should not" entries made on research assumptions)
- Stage 1 Founding Content Brief priority matrix (P1 and P2 impact assumptions)
- Stage 3 design principles where evidence is insufficient to indicate direction without a comparison

**Feasibility test — run first (days 1–3):**
Single primary: event-contingent capture compliance (captures initiated per participant per day). If median daily captures fall below the minimum threshold, diagnose the failure mode before proceeding — all subsequent comparisons are invalid without a functioning capture mechanism.

**Observation criteria — one set per comparison:**
Each comparison resolves a different decision. Select observation criteria from `/method-bank/ab-metrics-bank.md` matched to the specific decision. Every comparison requires: one primary criterion, 2–4 secondary criteria explaining why the primary moved or didn't, one guardrail with a hard threshold. Two primary criteria produces an unresolvable result — one primary only.

**Observation log — record without interpretation:**
- Primary criterion observation per variant (exact — no rounding)
- Direction (variant B produced more of the target behaviour / less / no meaningful difference)
- Effect size (substantial / moderate / minimal / noise)
- Participant count contributing to this observation
- Secondary criteria per variant
- Guardrail per variant — flag if threshold crossed

**Synthesis format — written after observation closes:**
Variant [B/A] showed more of the target behaviour than [A/B] on [primary criterion] by [difference], suggesting [what the behavioural difference means]. [Secondary criterion finding] supports/contradicts/qualifies this. This [confirms/complicates/revises] the hypothesis that [original decision]. Directional finding: [Committed / Revise and retest / Escalate to Stage 6 for real A/B test against live product].

The directional finding is mandatory. If observation is insufficient, state what additional evidence would reduce uncertainty and at what stage to seek it.

---

## File 2 — Synthesis

**Sequence of work: Cultural analysis → QES → Affinity → Usability → Quantitative integration → Journey map.** Cultural analysis runs first — it establishes the coding framework before any evidence is logged. Journey map runs last — it draws from all prior outputs. Do not reorder.

---

### Tab 01 — Cultural analysis + coding

**Source documents:** QES evidence log (primary) · raw transcripts (reference only — verify verbatim when unit meaning is ambiguous) · Stage 2 composite summary (bracketing reference at selective coding).

**Four stages in order — do not begin the next until the current is complete across the full corpus:**

**Stage 1 — Open coding (Primary):**
Label every distinct moment in the evidence log with 1–4 words, as close to the data as possible. No prior frameworks at this stage. A single entry may have multiple codes. 50–100+ codes across the full corpus is typical.
*Failure mode: using prior market research category names as open codes. This imports the prior framework before the data has been read on its own terms.*

**Stage 2 — Axial coding (Primary):**
Group open codes that share a relationship. Look for: codes that are causes of each other, conditions for each other, or consequences of each other. Name each cluster with a descriptive sentence — not a single word. A sentence forces an analytical position; a single word hides it.
*Inter-coder reliability check — run after clusters have stabilised (60–70% of corpus reviewed) and before selective coding begins: primary researcher codes 100% of data, second person independently reviews a 20% random sample, assigns each unit to the clusters given the definitions but not the primary researcher's placements. 70%+ agreement: proceed. Below 70%: cluster definitions are ambiguous — revise before proceeding.*

**Stage 3 — Selective coding (Primary):**
Identify the core category — the cluster that most other clusters relate to. All other clusters are antecedents, conditions, consequences, or modifiers of the core. Explicitly compare the emerging core category to the prior market research insight statement: does the data confirm, extend, or contradict it? Name contradictions explicitly — a contradiction between Stage 2 and Stage 3 is itself a finding.

**Stage 4 — Working theory (Secondary):**
2–3 paragraphs. Internal document. Describes the core category and its structure. Compares explicitly to the prior market research insight statement: what is confirmed, extended, or revised. Not a report — the working document that all subsequent Stage 3 outputs are derived from.

**Bias mitigation — three mechanisms:**
- *Reflexivity log:* end of each session, separate from the AM memo. Prompts: "What am I finding easiest to see? What might I be reluctant to see?"
- *Negative case analysis:* for each cluster, search for contradicting data. Document: "I looked for contradicting evidence and found: [result]." Undocumented search did not happen.
- *Member checking:* return findings to participants for correction. Corrections enter the QES log as tension flags.

---

### Tab 02 — Qualitative evidence synthesis (QES)

**Source documents:** All fieldwork documentation logs — event-contingent capture log, IDI session output, collage output log, food attention map log, environment walkthrough log. Open all before beginning. Signal-contingent ESM data and card sort log feed quantitative integration directly, not QES.

**Before beginning — priority flags:**
Read all fieldwork documentation before logging any entry. Flag and prioritise these four signal types — the hardest to recover once abstraction begins:
- **[B] Embodied language** — physical sensation, body movement, somatic description
- **[V] Participant vocabulary** — words the participant uses that differ from the research team's vocabulary; log verbatim
- **[!] Moments of surprise** — anything the team did not anticipate; log immediately and mark for priority analysis
- **[…] Silences and hesitations** — pauses [pause Xs], incomplete sentences, moments where the participant reached for language and did not find it

**Evidence log — one row per unit:**
Capture ID · Type · Verbatim (never paraphrase) · Trigger context · Researcher first response (untheorised — written before comparing to other entries) · MR comparison marker (Extends / Complicates / No prior equivalent / May revise) · Tension flag

*MR comparison marker is mandatory for every entry. "No prior equivalent" entries are the primary analytical output — accumulate them actively.*

---

### Tab 03 — Affinity diagram + insight statements

**Source documents:** Open codes from cultural analysis Stage 1 (one sticky note per coded unit) · QES evidence log (verbatim anchors per sticky note) · collage images (visual reference pinned near relevant clusters).

**Construction:**
Lay all notes on the board before clustering. Read each one — gestalt before grouping. Cluster by shared experiential quality, not topic. Name each cluster with a full sentence: "Bodily onset precedes cognitive awareness" not "Agency." Notes that resist any cluster are flagged — investigate these first.

**Insight statement format:**
[Specific participant group] [experiences a specific structural feature] because [mechanism revealed by fieldwork], which means [design implication — the decision this changes].

Every insight card must include:
- **Confidence tier:** Validated (3+ independent sources, 2+ method types, 5+ participants) · Directional (2 sources, 3–4 participants) · Exploratory (1 source or 1–2 participants)
- **Source trail:** specific affinity cluster + specific QES entry IDs
- **MR comparison marker:** Confirms / Extends / Complicates / No prior equivalent

*Decision test: if this insight is removed from the synthesis, does any design decision change? If no — it is an observation. Demote to evidence base; do not include in terminal outputs.*

---

### Tab 04 — Usability test report

**Source documents:** Usability testing of analogous products — one task, one interaction, one metric per product. Not a full product evaluation. Uses Stage 3 fieldwork participants — they contextualise observations against their own experience of the phenomenon.

**Test procedure:**
- Moderated remote sessions, 45 minutes, 2–3 products per session
- One task per product testing the specific functional overlap with the product under development
- Think-aloud throughout — participant narrates experience as they complete each task
- Do not lead: no validation, no help during tasks. Ask "what are you thinking right now?" if stuck — never show them what to do. The stuck moment is the data.

**Severity table — sorted highest to lowest:**
Issue # · Severity (1 cosmetic / 2 minor / 3 major / 4 critical) · Issue description · Participant frequency (X/Y) · Product tested · Design implication for this product

*Issues observed by multiple participants carry more weight than single-participant observations.*

---

### Tab 05 — Quantitative integration

**Source documents:** ESM temporal density data (signal-contingent + event-contingent protocols) · Values card sort distribution · Usability severity ratings.

Integrate after qualitative synthesis is complete. The quantitative layer corroborates and pins specific constructs — it does not lead the analysis.

**Three sources → three decision records:**

**Source 1 — ESM temporal density and affect data:**
Plot food noise frequency by hour (heat map or line chart). Does it cluster at specific times? Does Stage 3 event-contingent data confirm or revise Stage 2 signal-contingent findings? Cross-tabulate activity × location × intensity.
*Constructs pinned: default notification timing · widget proactive display logic · which mode to surface at which time of day.*

**Source 2 — Values card sort distribution:**
Percentage per word in "feels true / partly true / doesn't fit." Top three claimed words cross-referenced with voice note content.
*Constructs pinned: onboarding copy register · words that belong in the product's language system · words to exclude from all copy surfaces.*

**Source 3 — Usability severity ratings:**
Issues by severity per product. Which products produced the highest concentration of severity 3–4 issues.
*Constructs pinned: interaction patterns to adopt or avoid · IA and flow decisions.*

**Decision record format — one per construct:**
Named construct · Evidence trail (specific source IDs) · Decision direction · Status: **Committed** (adopt into specification) / **Conditional** (directional, confirm in Stage 6) / **Escalate** (insufficient evidence at this scale).

*All Stage 3 quantitative findings are Directional or Exploratory at most — sample sizes are too small for statistical significance. Decision records signal direction, not certainty.*

---

### Tab 06 — User journey map

**Source documents:** Affinity clusters (stage boundaries, pain points) · Cultural analysis working theory (emotional arc shape) · Food attention map logs (temporal arc) · Environment walkthrough logs (touchpoints, trigger context) · IDI transcripts (behaviour descriptions in participant vocabulary) · ESM temporal density (validates stage timing).

**The journey starts before the product exists.** Stage 1 is the person's daily reality — no product. The product enters at Stage 3 at the earliest.

**Five stages:**
1. Phenomenon erupts — daily life, no product. What does the person actually do with the craving?
2. Searching — the person actively looks for something different. What do they search for, what do they avoid?
3. Psychological contract — deciding whether to trust the product. What makes them stay or exit in the first session?
4. Real-time encounter — the product's moment of truth. Does it work in the actual context of the phenomenon?
5. Resolution — what the person does after. Do they return, share, abandon?

**Five rows:**
- *User behaviour:* 2–3 specific behaviours per stage in participant vocabulary verbatim. From IDI Phase 2 transcripts and event-contingent captures.
- *Emotional arc:* a single continuous curve across all five stages. Not described in cells — drawn as a line showing the psychological trajectory. Derive arc shape from cultural analysis working theory. Replace the placeholder dashed curve with a solid line when each stage's emotional state is confirmed.
- *Touchpoints:* every surface the person touches at each stage — including pre-product surfaces in Stages 1 and 2. From environment walkthrough logs and IDI accounts.
- *Pain points:* minimum 2 per stage. Must include pain that exists before the product exists (Stages 1–2). Use QES tension-flagged units and affinity cluster names — these are the most evidence-grounded descriptions of failure.
- *Opportunity points:* populate last — after pain points are confirmed. Each opportunity addresses a named pain point. Tag each: [Quick Win] [Strategic Bet] [Service SOP] [Material VI] [Strategy Rule].

**Do not pre-fill the map with assumptions from prior market research.** Every cell is populated from Stage 3 fieldwork evidence. A cell without evidence is a placeholder with a source label, not a hypothesis.

---

## File 3 — Convergence sprint

**Sequence:** Synthesis output (read first) → Sprint structure → A/B test backlog review → Terminal outputs.

---

### Tab 00 — Synthesis output (read this first)

Before producing this tab, read File 2 in full. This tab shows what the research produced — core insights, key tensions, design principles, opportunity spaces. The rest of the convergence file shows how those outputs were produced.

**Core insights:** 3–5 insight statements classified by confidence tier. Each insight in the format: [who] [structural feature] because [mechanism], which means [design implication] → therefore [action direction].

**Key tensions:** 2–4 named tensions the product must hold simultaneously. A tension names two things the data holds as simultaneously true that cannot be resolved by choosing one side. Format: Tension name · both sides stated · what the product must do to hold both.

**Design principles:** statements about how the product must behave — specific enough to make a decision, clear enough to be violated. Format: "The product must [specific behaviour] because [fieldwork finding], not [what to avoid]."

**Opportunity spaces:** named gaps between what participants need and what currently exists. Format: "[Specific population] currently has no way to [specific need revealed by fieldwork] — they resort to [current workaround] which [cost of workaround]. This is a territory the product can address."

---

### Tab 01 — Convergence sprint structure

**Confidence classification — apply to all findings before the sprint begins:**
- **Validated:** 3+ independent sources from 2+ method types · 5+ participants · pattern holds across portrait types. Act on directly. Grounds a design principle or system model element.
- **Directional:** 2 independent sources from different method types · 3–4 participants. Act with caution. Flag for Stage 6 confirmation before committing engineering resources.
- **Exploratory:** 1 source or 1–2 participants. Do not act on alone. Include in A/B backlog or note as hypothesis for Stage 6.

*A/B results at Stage 3 scale are always Directional at most — they indicate which direction to pursue, not how large the effect is.*

**Researcher bias mitigation — active throughout:**
At sprint opening, read the reflexivity log before reviewing any synthesis output. For each insight in Phase 3b, state: "I looked for data that would disprove this and found: [result]." An undocumented negative case search did not happen.

**Sprint phases — each produces a required artefact. If a phase does not produce its artefact, it has not been completed:**

**Phase 1 — Raw material review:**
Lay out all raw fieldwork material before touching any synthesis output — event-contingent captures, IDI transcripts, instrument outputs, signal-contingent ESM data. Read each one. Flag any raw material that contradicts a synthesis output. This is the check on the synthesis, not a re-reading of it.
*Artefact: flagged contradictions list.*

**Phase 2 — Cross-source clustering:**
For each insight statement, map which sources support it, which are silent, and which contradict it. Convergence across method types (netnography + ESM + IDI) is stronger evidence than convergence within one method type.

Triangulation thresholds:
- **Strong convergence:** 3+ independent sources from 2+ method types → grounds a design principle
- **Moderate convergence:** 2 sources from different method types → sufficient for an insight statement, flag for Stage 6 confirmation
- **Weak convergence:** 1 source → observation only, include in A/B backlog if high-risk
- **Contradicted:** tension card mandatory, do not suppress
*Artefact: source map per insight (supported / silent / divergent).*

**Phase 3 — Tension mapping:**
List every contradiction. For each: is this a real contradiction (same person, same context, incompatible) or a contextual difference (same person, different situations — itself a finding)?
*Artefact: named tension list with both sides held simultaneously.*

**Phase 3b — Insight generation:**
Apply to each cluster:
1. Name the structural feature — what does this cluster reveal? State as a claim, not a description. *"If I removed the weakest supporting source, would I still believe it?"*
2. Apply the confidence tier — how many independent sources support it?
3. State the design implication — which role, which decision? *"If a designer did not know this, what specifically would they build wrong?"*
4. Compare to prior market research — confirms / extends / complicates / no prior equivalent. If it revises the insight statement, update Stage 1 Document 01 before Stage 4 begins.
5. Write in full format: [who] [structural feature] because [mechanism], which means [design implication].
*Test: read aloud. If a team member responds "we already knew that" without the fieldwork evidence — it is an observation.*
*Artefact: prioritised insight list — insights that change decisions at the top, observations below.*

**Phase 4 — Decision test:**
For each insight, ask: if removed, does any design decision change? If no — demote to observation. Keep for context; do not let it carry the weight of an insight in the terminal outputs.
*Artefact: final insight list with demoted observations separated.*

---

### Tab 02 — A/B test backlog review

Review each candidate test from the fieldwork file against synthesis findings. Three possible statuses:
- **Run:** synthesis did not reduce uncertainty enough. Hypothesis still well-grounded. Execute in Stage 6.
- **Revise:** synthesis revealed the hypothesis was based on an incorrect assumption. Rewrite before Stage 6.
- **Drop:** synthesis produced sufficient directional signal on this question. The finding from synthesis feeds Stage 4 directly.

For each test reviewed, record the status with the synthesis finding that drove the decision.

---

### Tab 03 — Terminal outputs

Three formats. Every insight from the synthesis must attach to one of these three before Stage 3 closes. If it does not fit any format, it is still an observation.

**Design principles — format:**
"[The product] must [specific behavioural requirement] because [specific fieldwork finding], not [what to avoid]."
- Specific enough that a designer can use it to resolve a specific decision
- Clear enough that a specific design choice could violate it
- Every principle links to at least one Validated or Directional insight

**Opportunity spaces — format:**
"[Specific population] currently has no way to [specific need revealed by fieldwork] — they resort to [current workaround] which [cost of workaround]. This is a territory the product can address."
- Not a feature idea — a named gap in the market
- Grounded in a specific pain point from the journey map

**System model:**
A single-page diagram of how the behaviour works — what triggers it, what shapes it, what resolves it. Every element traces to at least one QES evidence entry. Not a product flow. Structure: trigger → onset → intensification → coping attempt → resolution / continuation, with modifying variables named. Pin this to the start of every Stage 4 session.

---

## Common failure modes

**Filling the journey map with prior assumptions.** Every cell must come from Stage 3 fieldwork. A cell without evidence is a placeholder, not a hypothesis dressed as data.

**Producing insights without a source trail.** An insight with no traceable evidence trail is a hypothesis. Every insight card requires specific QES entry IDs.

**Designing Round 2 instruments before Round 1 composite summary exists.** ESM prompts and screeners designed from prior market research measure researcher constructs, not the phenomenon.

**Coding before bracketing.** If the session-opening methodological note is not written, the codes will import prior market research categories without the researcher knowing.

**Skipping the gestalt read.** Reading posts or transcripts in fragments produces decontextualised units. The gestalt step cannot be skipped.

**Affinity clustering by topic.** Two entries about different topics that share the same experiential structure belong in the same cluster. Clustering by topic produces categories, not findings.

**Missing the tension flag.** Contradictions between entries, between methods, or between Stage 2 and Stage 3 are findings. A corpus with no tension flags has not been read carefully enough.

**Not reading the reflexivity log before the sprint.** The sprint's external-challenge function only works if the researcher surfaces their interpretive lens before applying it to the conclusions.

**Insight that does not change a decision.** The decision test is mandatory. Remove insights that survive the test with "we already knew that" — they are observations restating prior assumptions.

**A/B test with no guardrail metric.** A test without a guardrail can produce a metric win while silently degrading the experience the product depends on. Consult `/method-bank/ab-metrics-bank.md`.

---

*Skill developed through the vibe eating app research session, June 2026. Language standards, content inclusion criteria, and production principles encoded from the iterative editing process applied to the food noise study Stage 3 documents. A/B metrics bank in `/method-bank/ab-metrics-bank.md`. Method selection in `/method-bank/INDEX.md`.*
