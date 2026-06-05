---
name: translate-and-materialise
description: Use this skill when producing the three final output documents from prior research and synthesis: Brand System, Product Specification, and Strategic Direction. These are the documents teams build from. No separate Stage 4/Stage 5 distinction — decisions are embedded within each document as sections. Follows Stage 3 (Produce Structured Insights). These three documents are the handoff to engineering, execution, and leadership.
---

# Translate and Materialise — SKILL

**Phase position:** Follows Stage 3 convergence outputs (design principles, opportunity spaces, system model, insight statements, tensions). These Stage 3 outputs are source material — they do not appear again as separate deliverables. They are embedded sections within the three documents below.
**Output:** Three documents produced in parallel — Brand System (Content + Brand Voice track), Product Specification (UX Design track), Strategic Direction (Experience Design track).
**Reference:** `/method-bank/ab-metrics-bank.md` for metric selection when writing prototype specifications. `/method-bank/INDEX.md` — Production calibration references section for HMW scoping and concept direction distinctness calibration.

---

## Core production discipline

**Every key decision must pass three tests before it ships:**
1. Can an engineer build this without asking a question?
2. Can two designers implement this and produce the same result?
3. Does this eliminate at least one alternative approach?

If not — it is still too loose. Rewrite it.

**Output templates, not instructions.** The documents define what a finished output must look like — number of items, structure of each item, allowed formats, validation criteria, removal criteria. The difference:

- Instructional (wrong): "proof points must be verifiable"
- Output-defined (correct): "3–5 proof points, each formatted as: [claim] — Source: [Stage 3 finding or data reference]. Removal criterion: any proof point without a source citation is deleted before presentation, not rewritten."

**Decisions replace insights.** Stage 3 insight language ("the act/resist binary is the structural gap") does not appear in these documents. It has been translated into a specific product decision: "third option = redirect into mode, triggered at capture confirmation. No flow presents eating or suppression as the resolution path." If a decision statement still reads as analysis, translate it further.

**Specificity standard:**

| Too loose | Correct |
|---|---|
| "capture must be fast" | "user enters capture state within 1 tap from any entry point, no required text input" |
| "onboarding should use recognition" | "first two onboarding screens contain only recognition statements — no product benefit language, no CTA" |
| "audio optional" | "no flow may require audio to complete a session" |
| "product should reduce friction" | "maximum 2 taps from onset to submitted capture, no exceptions" |
| "timing needs optimisation" | "notification default set to [ESM temporal peak ± 30 min], adjustable, validated in Stage 6" |

**Interaction flows use monospace notation with hard constraints beneath.** Not prose descriptions. Format:

```
Step 1 → Step 2 → [decision: Y/N] → Step 3a / Step 3b → end state
```
Every hard constraint listed beneath the flow: tap count, time limits, states that must never occur, error paths.

**Quality statements must be observable.** "Understood", "Received", "Safe" — a designer can look at a completed screen and verify whether this quality is present. "Positive experience" or "feels good" are not observable and are not acceptable as quality statements.

**Required / Recommended tiers on every section.** Required: the document fails its purpose without this section. Recommended: standard practice, adaptable to time constraints. Teams know what to produce under pressure.

**MVP phase labelling on all flows and sections.** Phase 1 = MVP. Phase 2 = Core product. Phase 3 = Optional depth. Every flow and wireframe section labelled against phases.

---

## Shared outcome layer — produced before all three documents

Before opening any of the three documents, produce a shared outcome layer: the specific product decisions, the specific rules-out, and the specific open questions from Stage 3. This layer lives visibly before the three documents and every document references it rather than restating the research.

**Column 1 — Product decisions:** Each stated as a behaviour constraint, not an insight. Format: "[feature/interaction] will/will not [specific behaviour]." Confidence tier (Committed / Conditional) attached to each. A Conditional decision is directional — it must be validated in Stage 6 before hardcoding.

**Column 2 — Rules out:** What is now off the table because of the decisions in Column 1. Named precisely enough that the team stops debating them. Not "negative space" — explicit eliminations.

**Column 3 — Still open:** Decisions the research was not large enough to resolve. Each states what additional evidence would resolve it and at which stage.

**Test:** a stakeholder reads the outcome layer and understands what changed without opening any of the three documents.

---

## Document 1 — Brand System

**Audience:** writers, designers, content designers, AI systems. Anyone producing copy for the product.
**Function:** the complete working reference. Every writer opens this before writing a single word. Specific enough that any team member can produce on-brand content without requiring editorial oversight.
**Sources:** Stage 3 participant vocabulary logs · IDI language harvest · card sort logs (claimed and rejected words) · collage voice transcripts · Stage 3 identity tensions · Stage 1 constraints.

### Section 01 — Brand voice foundation (Required)

**Output:** 3–4 voice attributes. More than 4 creates inconsistency — writers must hold too many constraints simultaneously. Each attribute is one complete block:

- **Name:** 2–3 words. Not a generic value ("bold", "human"). Specific to this product's positioning. Grounded in participant vocabulary where possible.
- **Tier:** Primary (exactly one — overrides all others when conflict arises) or Secondary (2–3). **Tiebreaker rule:** when attributes conflict and the channel guide does not specify, ask "does this copy make the person feel understood before it asks anything of them?" This is always the final test.
- **Definition:** Exactly one sentence. Validation test: two writers read this and independently produce copy for the same surface — outputs must be recognisably similar. If not, rewrite.
- **This / not that:** Exactly two contrasts, each a complete sentence. The "not that" must be something a competent writer could plausibly produce — if no one would do it anyway, it does not count as a constraint.
- **Fieldwork source:** One Stage 3 QES entry ID or insight statement number. Not an argument — the evidence.
- **Live example:** One sentence of actual product copy on a named surface. Must be copy that would ship. If you cannot write this example, the attribute is not specific enough.

**Failure criterion:** an attribute that cannot produce a live example is not defined specifically enough. Rewrite before the document ships.

### Section 02 — Messaging hierarchy (Required)

**Output:** all four levels complete. Each level has a validation criterion — not just a format.

- **Brand Purpose:** 1 sentence. Validation: survives "but why does that matter?" three times without becoming circular.
- **Brand Promise:** 1 sentence, falsifiable. Validation: if the product ships with a bug directly violating this promise, the team agrees it must be fixed before launch. If they would not agree, it is not a promise.
- **Value propositions:** one per Stage 3 portrait type or key context. Format: [portrait/context] + [specific need from fieldwork] + [what the product provides] = one sentence. Failure criterion: uses any word not found in Stage 3 participant vocabulary logs.
- **Proof points:** exactly 3–5 items. Format per item: [claim] — Source: [Stage 3 finding / ESM data / analogous product evidence]. Removal criterion: any proof point without a source citation is deleted, not rewritten.

### Section 03 — Channel and context guide (Required)

**Output:** a table. One row per surface. All surfaces in the content model must have an entry before the document ships. Columns:

Surface name (exact name from UX spec IA) · Character limit · Lead attribute (Primary or Secondary) · Copy must do (functional job, one sentence) · Copy must NOT do (most common failure mode, grounded in usability severity table where possible)

**Minimum surfaces:** onboarding screens 1–2 · vault entry prompt · mode entry copy · in-session copy · push notification · error state · community prompt · app store description.

**Validation:** every row's "must NOT do" is specific enough that a writer knows immediately whether they have violated it. "Don't be generic" fails — "do not include any product benefit language on onboarding screens 1–2" passes.

### Section 04 — Do/don't examples (Required)

**Output:** minimum 2 example sets per voice attribute, minimum 1 per surface from Section 03. Each example set:

- Surface (linked to Section 03 row)
- Attribute demonstrated
- Do version: correct copy
- Don't version: same underlying content, written wrongly — not a different message
- Why the don't fails: one sentence, citing the specific attribute it violates and the consequence for the reader

**Failure criterion:** if the don't version requires more than one sentence to explain what is wrong, the attribute in Section 01 is not specific enough.

### Section 05 — Copy range production (Recommended)

**Output:** one complete piece of copy per required format, each traceable to a voice attribute and a surface specification. Required formats: OOH poster (≤8 words) · push notification (title ≤40 chars / body ≤90 chars) · onboarding headline (≤12 words) · vault entry prompt (≤20 words) · TikTok hook (≤5 seconds spoken) · email subject (≤50 chars) · in-session mode copy (≤30 words) · app store description (≤80 words).

**Test:** any piece of copy that could belong to any wellness product fails the system test. Every piece must be specific to this product's position.

### Section 06 — Naming and terminology (Recommended)

**Output:** one entry per product-specific noun. Format per entry: Term · Definition (1 sentence) · Correct usage (in a sentence) · Incorrect usage (most common mistake) · Why this term (one sentence, grounded in participant vocabulary where possible).

Include: every mode name · "vault" or chosen product term · "capture" · the chosen product term for the phenomenon · "session." Also include every word from the Stage 3 card sort "doesn't fit" column that could plausibly appear in copy — document explicitly why it is excluded.

### Section 07 — AI register analysis (Recommended)

**Output:** one entry per voice attribute. Format: attribute name · register scale (e.g. formality 1–5, target value and acceptable range) · system prompt instruction that produces on-attribute copy · one prompt-output pair showing the attribute active · one pair showing the failure mode when the parameter is absent · failure mode description (specific — not "sounds generic").

**Test:** paste the system prompt into an LLM and verify output matches the attribute. If it does not, the attribute definition is not specific enough to be machine-operable.

---

## Document 2 — Product Specification

**Audience:** engineers and product team. The document they build from.
**Function:** every structural, interaction, and content decision — from IA to annotated wireframes to handoff notes. An engineer should not need to ask a design question after reading this.
**Sources:** Stage 3 design principles · system model · consumer journey map · usability severity table · quantitative integration decision records · Stage 1 Frame a Problem · Stage 1 constraints doc.

### MVP scope block — immediately after Section 01, before IA (Required)

Three columns: Phase 1 MVP (what gets built first — the irreducible core), Phase 2 Core product (the product as designed), Phase 3 Optional depth (features contingent on Stage 6 validation). Every section and flow that follows is read against these phases. Phase labels appear on every flow and wireframe section.

### Section 01 — Scope and design principles (Required)

**Output:** problem statement (1 paragraph, sourced from Stage 1 Frame a Problem — the research reframe, not the original brief) + design principles list.

Design principles are hard filters — every design decision in sections 02–07 must be traceable to one. For each principle: the confidence tier (Validated/Directional) + the specific constraint it places on the spec — what it rules out, not just what it requires. Followed immediately by the MVP scope block.

### Section 02 — Information architecture (Required)

**Output:** app map diagram. Every screen, mode, and state in the product — parent-child relationships, navigation hierarchy, mode hierarchy. Format: hierarchical diagram with root → L1 screens → L2 screens/states → modal overlays.

Every IA decision annotated with its rationale. Dashed/placeholder nodes mark screens whose structure is agreed but content not yet specified — must be resolved before wireframing begins.

**Hard rule:** this section must be agreed before wireframing begins. Everything downstream depends on this structure.

### Section 03 — User flow diagrams (Required)

**Output:** five required flows specified as interaction sequences. Not prose descriptions. Format per flow:

```
Step → Step → [decision: Y/N] → branch A / branch B → end state
```
Beneath each flow: hard constraints (tap counts, time limits, states that must never occur, error paths). Each flow labelled with its MVP phase.

**5 required flows** (all Phase 1 unless noted):
1. First session (download → onboarding → first vault entry) — Phase 1
2. Event-contingent capture (onset → capture → optional mode entry) — Phase 1, critical path
3. Mode session (mode entry → in-session → session close → affect prompt) — Phase 1 (1 mode), Phase 2 (full suite)
4. Vault return (app open → browse → action) — Phase 1
5. Notification re-entry (notification → deeplink → capture state → home) — Phase 1

**Validation:** every hard constraint stated precisely enough that an engineer can write an acceptance test from it. "Capture must be fast" is not a hard constraint. "Maximum 2 taps from onset to submitted capture" is.

### Section 04 — Annotated wireframes (Required)

**Output:** per-screen structural blueprints, low to mid fidelity. No colour, no final typography, no imagery. Format per screen:

Screen code (immutable — maps to IA, never changes after assignment) · Screen name (exact name from IA, consistent with Brand System naming glossary) · Layout at 375px mobile-first · Content hierarchy annotated · Interaction annotations (what each element does on tap) · Design principle citation (which Stage 3 principle this layout satisfies) · Phase label (Phase 1/2/3).

**Hard rule:** greyscale only — a wireframe that could not be understood without colour is over-specified at this stage. Colour, final typography, and imagery are not included.

### Section 05 — Interaction states (Required)

**Output:** one entry per interactive element covering all states: Default · Focus/hover · Active/pressed · Loading · Success · Error (with error message copy sourced from Brand System Section 03) · Empty · Disabled.

Error and empty states are the most commonly underdocumented. Every screen that can be empty must show what it looks like empty. Every action that can fail must show the failure state with copy.

### Section 06 — Accessibility and constraints (Required)

**Output:** specific compliance requirements plus product-specific constraints. Minimum: touch targets (44×44px minimum) · colour contrast (WCAG AA — 4.5:1 normal text, 3:1 large text) · screen reader labels (every interactive element) · text scaling (layout holds at 200%) · audio-independent interaction (all modes complete without audio — grounded in the shared-space fieldwork finding) · haptic specifications (pattern named for any haptic used as a primary signal).

**Audio-independent is a hard product requirement, not an accessibility note.** The fieldwork finding that primary use context is a shared office or home environment means audio failure cannot break a session. Specify this separately from WCAG compliance.

### Section 07 — Engineering handoff (Required)

**Output:** component inventory (every reusable element named consistently with IA and Brand System glossary) · dependency chain (which screens depend on which data or states — this is the build sequence) · open questions (each with owner and resolution date — an undocumented open question becomes an undocumented engineering assumption) · build priority (linked to Stage 3 A/B backlog items with "Escalate to Stage 6" status — those flows are tested first) · version history.

---

## Document 3 — Strategic Direction

**Audience:** design team and leadership. Not just creative-facing — this document must resolve product debates and commit the team to specific directions.
**Function:** the creative and product brief all other tracks work from. Defines what the product experience must produce AND what decisions that commits the team to. The "commits us to / rules out / still open" structure is the most important part of this document.
**Sources:** Stage 3 convergence output layer · tensions · opportunity spaces · emotional arc · system model · Stage 1 constraints.

### Section 01 — Insight-to-concept bridge (Required)

**Output:** one bridge card per core insight from Stage 3 convergence output layer. Each card:

- Insight: "We discovered that [user type] does X because [motivation], which means [design implication]" — confidence tier attached
- HMW statement derived from "which means" — scoped correctly (see scope test below)

**HMW scope test:** broad enough to invite multiple concept directions, narrow enough to rule out irrelevant ones. If two directions produce identical responses, the statement is too narrow. If any direction could respond to it, the statement is too broad.

### Section 02 — Concept directions × 3 (Required)

**Output:** three genuinely distinct directions — different answers to the same question, not variations of the same answer. If two directions differ only in surface treatment, collapse them and develop a genuinely different third.

Format per direction: Name (specific — "The vessel" not "Direction A") · Core idea (1 sentence — what this direction fundamentally proposes about the product's relationship with the user) · HMW response (how it answers each HMW statement) · Tension position (which Stage 3 tension it leans into and how — a direction that avoids all tensions is not a direction, it is a compromise) · Experiential quality (1 sentence — what it would feel like to use, not functional features) · Differentiator (single most compelling advantage) · Biggest risk (single most significant constraint — a direction with no risk is not specific enough).

Rejected territories are documented here and carry the same portfolio weight as the selected direction.

### Section 03 — Selected direction with product decisions (Required)

**Output:** selected direction card + rejected direction cards + product decisions block.

**Selected direction card:** Name · Extended description (3–4 sentences: what it is, what it commits to, what it gives up) · Why selected (citing Stage 3 design principles by number — not "the team preferred it") · What it requires (constraints on the Product Specification, the Brand System, and the prototype).

**Product decisions block — three distinct sections, each required:**
- *Commits us to:* 2–3 specific behaviour constraints in format "[feature/interaction] will/will not [specific behaviour]." Stated precisely enough that the team stops debating them.
- *Rules out:* 1–2 approaches now off the table. Named specifically — not "the other direction."
- *Still open — feed to Stage 6:* 1–2 questions this direction does not resolve. States what additional evidence would resolve each one.

**Rejected direction cards:** one per rejected direction — what it got right (one sentence) and why it was not selected (one sentence, specific constraint or risk, not "the other direction was better").

### Section 04 — Experience principles (Required)

**Output:** a table. One row per consumer journey stage (from Stage 3 journey map — all five stages). Columns:

Stage name · Target emotional state (from Stage 3 emotional arc — populated after fieldwork) · Must produce (observable — a designer can verify this on a completed screen) · Must not produce (grounded in the Stage 3 pain point for this stage) · Quality statement (one word or short phrase — the design team's internal test for every decision at this stage)

**Validation criterion:** each "must produce" statement must be observable. "A sense of being seen before being offered anything" is observable. "A positive experience" is not. If you cannot verify it on a completed screen, rewrite it.

**Precedence rule:** experience principles constrain the Product Specification, not the other way around. If an interaction decision in the Product Specification conflicts with an experience principle, the experience principle takes precedence.

### Section 05 — Creative platform (Recommended)

**Output:** campaign line · platform rationale (why this line, what tension it holds, why it is durable) · channel executions (one direction per channel: product, TikTok/social, press/PR) · 12-month execution range (4–6 territories the platform sustains — brief descriptions) · rejected lines (2–3 with one sentence each on what they got right and why rejected).

**D&AD standard:** evidence of divergent creative thinking before convergence. Rejected territories shown briefly to prove range. A platform that only works in one execution is a campaign, not a platform. Test: could a different creative team produce each 12-month territory from the campaign line alone?

### Section 06 — Prototype specification (Recommended)

**Output:** scope (which flows — linked to Stage 3 A/B backlog "Escalate to Stage 6" items) · fidelity level per section (Low/Mid/High with rationale — default is Mid; High only where copy register or visual design is the variable being tested) · must demonstrate (specific decisions the prototype tests, not "what the product looks like") · must not include (out of scope — every additional screen of fidelity is time that could be a second iteration) · test protocol (which participants, which tasks, what constitutes a successful test).

---

## Common failure modes

**Insight language surviving into the documents.** "The act/resist binary is the structural gap" belongs in Stage 3. If it appears in any of these three documents, translate it to a specific decision before the document ships.

**Instructions instead of output templates.** "Proof points should be verifiable" is an instruction. "3–5 proof points, format: [claim] — Source: [citation], removal criterion: delete if unsourced" is an output template. Every section must define the finished output, not describe how to produce it.

**Quality statements that are not observable.** "Feels welcoming" cannot be verified on a completed screen. "The person reads the first screen without being asked for anything" can be. Test every quality statement.

**Flow descriptions without hard constraints.** A flow written as prose will produce different implementations from different engineers. Every flow must have a monospace notation and numbered hard constraints beneath it.

**Strategic Direction that is only creative-facing.** The "commits us to / rules out / still open" block is mandatory, not optional. Without it, the strategic direction tells leadership what was chosen but not what the choice means for the product. Leadership must be able to read Section 03 and know what to approve and what to stop debating.

**Outcome layer that restates analysis.** "The act/resist binary is the structural gap" in the outcome layer is analysis. "Third option = redirect into mode, triggered at capture confirmation" is a decision. If the outcome layer still reads as Stage 3 synthesis, the translation has not been completed.

**Missing MVP phase labels.** Every section and flow must be labelled Phase 1/2/3. Teams discover phasing in engineering and scramble. The phasing must be visible before a single screen is built.

---

*Skill developed through the vibe eating app research session, June 2026. Production discipline encoded from the iterative editing process applied to the Stage 4+5 documents. Three specificity tests (engineer/designer/eliminates-alternative) derived from the editing discipline enforced throughout. Brand System section structure grounded in industry brand guidelines standard (Brand Vision, 2026; Frontify, 2025; Helms Workshop, 2025). Product Specification structure grounded in UX spec industry standard. Creative platform standard grounded in D&AD professional award criterion.*
