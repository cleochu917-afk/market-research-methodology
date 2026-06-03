---
name: design-investigation
description: Use this skill when designing how to investigate a product or experience problem — producing research questions, a research protocol, a method rationale, and a participant plan with screener. Follows EISR market research and Frame A Problem. Precedes structured insight production.
---

# Design How to Investigate It — SKILL

**Phase position:** Follows Frame A Problem. Precedes Stage 3 (Produce Structured Insight).
**Role perspective:** Experience design owns research questions and phenomenological inquiry. UX owns plan, screener, and method procedure.
**Output:** Two working documents — generative research questions, and protocol + plan + screener.
**Method selection:** Consult `/method-bank/INDEX.md` before beginning. Identify your problem type and route to the recommended method combination. This skill specifies how to produce the documents and what is immutable across all studies. The bank specifies which methods to use. When a study requires a method listed as undocumented in the INDEX, use the INDEX entry as a starting point, apply it in the study, then document it as a bank profile after the study completes — following the contribution protocol in the INDEX.

---

## Core production principle

Before writing any section, ask: who reads this, what decision do they need to make, and what language do they use for that decision?

**Experience designer reads:** what to investigate and why this method over alternatives.
**UX researcher reads:** how to execute the study operationally, step by step.
**Prototyper reads:** what decisions this research will open — a range, not a verdict.
**PM reads:** what cannot be decided without this research, and what changes if findings differ from expectations.

Write each section to its reader. When a section serves multiple readers, name the primary reader and write to them.

---

## Immutable requirement — phenomenological inquiry in Round 1

*Applies to: Type 1 interior experience problems. For Type 2–5 problems, consult the method bank INDEX — this requirement does not apply.*

For any Type 1 study, before any second-round measurement study runs (ESM, A/B testing, usability testing), a phenomenological inquiry must be conducted. This is not a method — it is an analytical process that runs through whatever data source the study collects: netnographic community data, interview transcripts, diary entries. The method is chosen from the bank. The inquiry process below is invariant.

**Why this is immutable:** Second-round studies impose a measurement framework on the phenomenon. If that framework is derived from prior market research assumptions rather than from the lived experience itself, the study measures a researcher construct rather than the phenomenon. The phenomenological inquiry ensures that the framework for Round 2 comes from the data.

**Two conditions that change how the process runs:**
- *If no prior market research exists:* Step 4 (prior research comparison marking) still runs, but all units default to "No prior equivalent" — the comparison is against an empty base. The process is more exploratory; saturation in Step 2 of the stopping rule becomes the primary termination criterion.
- *If the phenomenon has no bodily dimension:* Step 3 (flag embodied units) is skipped. Applicable to cognitive or linguistic phenomena where somatic experience is not the research question.

### The phenomenological inquiry process

**Before each session — bracketing**

Write a methodological note listing the active prior research assumptions you are carrying: which portrait types, which elements of the insight statement, which product directions. Name them explicitly. These are not eliminated — they are the preconceptual horizon against which new findings produce meaning. Naming them is what makes the comparison possible.

**Step 1 — Gestalt read**
Read the whole data unit (thread, transcript, diary period) before extracting anything. Attend to overall shape — tone shifts, what the person returns to, what feels most charged. A unit means something different in the context of the whole than it does in isolation. This step cannot be skipped.

*Output: a sense of the whole before any extraction begins.*

**Step 2 — Delineate units of meaning**
Go through the data identifying discrete units — a phrase, a sentence, a passage that constitutes a distinct moment of meaning. When in doubt, keep separate. Tag each unit with its coverage dimension (not a post type or code category).

*Output: a list of meaning units with coverage dimension tags.*

**Step 3 — Flag embodied units**
Mark any unit describing physical sensation, involuntary body movement, or somatic experience. These are methodologically prioritised — they provide direct access to the bodily layer of the experience that other analytical approaches routinely miss.

*Output: an embodied sub-corpus for priority analysis.*

**Step 4 — Prior research comparison marking**
For each unit mark: Extends prior research / Complicates prior research / No prior equivalent / May revise prior finding. Units marked No prior equivalent are flagged immediately — they constitute the primary analytical output of Round 1. Accumulate them actively.

*Output: a sorted corpus. The "No prior equivalent" pile is what this inquiry exists to produce.*

**Step 5 — Eliminate redundancies**
Consolidate units with the same literal content across sessions. Note: frequency and distribution are not redundant even when content is the same. A unit appearing across multiple communities or participants with increasing emotional intensity is stronger evidence than one appearing once.

*Output: a consolidated unit list with frequency and source distribution noted.*

**Step 6 — Cluster into themes**
Group units sharing a common quality. Do not force clustering. Units that resist grouping are methodologically significant — they often point to structures the prior framework cannot accommodate. Note resistance explicitly in the analytical memo.

*Output: a theme map with outliers explicitly noted.*

**Step 7 — Cross-case comparison**
Ask which themes appear across all data sources — all communities, all participants, all contexts. Themes appearing everywhere are candidates for the shared core the research questions are asking about. Source-specific themes reveal how context shapes the experience.

*Output: a split between shared patterns and source-specific ones.*

**Step 8 — Validity checking**
Return phenomenological descriptions to participants or communities. Ask: does this describe what it feels like? Recognition confirms. Corrections are equally valuable — they surface what the description missed. In netnographic settings: post as a genuine community member with transparent research purpose. In interview settings: present the description at the end of a follow-up session.

*Output: community-validated or participant-corrected descriptions.*

**Step 9 — Composite summary**
Write a description of what the phenomenon looks like from the data — not from the prior research framework. At the end, explicitly compare to the prior research: what is confirmed, what is extended, what needs revision. This comparison is the handoff to Round 2 design.

*Output: the Round 1 primary deliverable. Round 2 instruments are not designed until this exists.*

### Memoing system — four types, maintained throughout

The memo system runs in parallel with all nine steps. It is the discipline that maintains the inquiry across sessions.

- **ON (Observational):** What happened — specific data noted as significant. Source, timestamp, context.
- **TN (Theoretical):** Attempts to derive meaning — what this suggests about the experience structure. Prior research comparison tag attached.
- **MN (Methodological):** The session's bracketing list — active prior research assumptions named at session start. Renewed at the start of each new data source.
- **AM (Analytical):** End-of-session summary — what is emerging, what the data is resisting, what has no prior equivalent. The AM is the mechanism that tracks outstanding coverage gaps between sessions and drives the stopping rule.

### Stopping rule

Data collection closes when all three conditions are met in sequence:

1. All primary coverage dimensions show sufficient variation (minimum 4–5 instances per dimension covering meaningfully different cases). *Coverage dimensions are defined per study in Document 02, Section: data selection — primary, secondary, and quality-check tiers specified there.*
2. Experiential saturation: three consecutive sessions with no new "No prior equivalent" units and no existing clusters gaining new members.
3. Gaps flagged in prior AMs are filled.

Secondary dimensions require sufficient variation, not saturation. Quality-check dimensions require balance only.

---

## Document 01 — Research questions

**Owner:** Experience design
**Reader:** Product team and UX researcher

### What makes a research question work

A research question is open if someone could answer it in a way that surprises you. If the question contains its own analytical framework as a premise, it is a hypothesis disguised as a question.

**Test:** Remove everything after the question mark. Does what remains contain analytical categories or preset options? If yes, rewrite.

Failure: *"What is the temporal and rhythmic structure of food noise?"* — contains the analytical frame.
Working: *"What happens from the moment a craving begins to when it ends or passes?"* — genuinely open.

### Card structure — four elements

**The question** — plain language, non-leading, no analytical categories, no preset options.

**Three side-by-side fields with directional arrows:**
- *What this asks about:* Plain description of the territory. One or two sentences. No frameworks.
- *What we don't know yet:* The specific gap between prior research and this question — what was captured and what was missed.
- *What this opens:* A list of decisions, processes, and prototype choices the finding will inform. Not a verdict. Not a product feature name. Written in the language of the roles who act on it: session architecture, interaction model, copy register, prototype scope. The reader selects what is relevant to where they are.

**Prior research comparison marker** — Extends / May complicate / No prior equivalent / May revise.

**Production trigger** — named role, named decision.

### What does not appear in Document 01

Analytical taxonomy in the questions. Options embedded in the question as prompts. Product feature names in "What this opens." Philosophical citations. Single-outcome verdicts.

---

## Document 02 — Protocol + plan + screener

**Owner:** Experience design (protocol) + UX (plan, screener, procedure)
**Reader:** UX researcher executing the study

### Section: data selection — maximum variation coverage

Derive coverage dimensions from the research questions. For each question ask: what range of data would this question require to produce a credible finding?

**Weighting is mandatory:**
- Primary: foundational questions about what the phenomenon is. Must reach saturation.
- Secondary: contextual and surrounding questions. Sufficient variation required.
- Quality-check: methodological balance only. Not a substantive dimension.

**Two standing rules:**
1. Trigger condition is always primary — what was happening immediately before the experience started. Consistently underinvestigated in prior market research.
2. Communicative function is always a quality check — different communicative styles package the same content differently. They do not independently surface new experiential content.

### Section: method procedure

Written as numbered steps. Each step names what to do, the standard it follows, and where it departs from standard — flagged explicitly with rationale.

### Section: method rationale

Three-column comparison table: research challenge in the centre, our method on the right, alternatives on the left with specific reasons they are less well-suited for this study. "Less well-suited" not "wrong."

### Section: participant criteria and screener

Name the sampling strategy explicitly — maximum variation purposive sampling combined with criterion sampling (Patton, 2002) is standard for this phase.

State quotas per subgroup with the research question each subgroup serves. Tie each screener question to the quota it fills. Include one open-field articulation question when the study requires participants to describe interior experience — flag as non-standard with rationale. Include one foil question — flag it as a foil.

---

## Format standards

Role tags at the top of each document are functional — they tell the reader whether the document is for them. Section labels orient; content explains. Footnotes cite sources, methodology standards, and named departures only.

---

## Common failure modes

**Writing for the wrong reader.** Check the role line before writing each section.

**Questions that contain their own answers.** Apply the test: remove everything after the question mark.

**"What this opens" as a verdict.** A list opens decision space. A single framed outcome closes it.

**Skipping the gestalt read.** Extracting units from posts or transcripts without reading the whole first produces decontextualised data. The gestalt step is non-negotiable.

**Coverage without weighting.** Primary dimensions must reach saturation. Trigger condition is always primary. Communicative function is always a quality check.

**Missing stopping rule.** The AM memo is what makes the stopping rule operational. Without end-of-session memos, gap tracking fails and data collection has no principled endpoint.

**Round 2 designed before Round 1 composite summary exists.** ESM prompts, interview guides, and screeners designed from prior market research assumptions rather than phenomenological findings measure researcher constructs, not the phenomenon.

---

*Skill developed through the vibe eating app research session, June 2026. Phenomenological inquiry process extracted from the food noise study and stated as immutable across all interior experience investigations. Method selection routes to `/method-bank/INDEX.md`.*
