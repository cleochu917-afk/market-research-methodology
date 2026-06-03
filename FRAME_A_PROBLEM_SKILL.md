# Frame A Problem — SKILL
## Standardised methodology for problem framing in product development

**Phase position:** Follows EISR market research. Precedes product brief and design sprint.
**Role perspective:** Creative strategy / product / experience design / content design — alternating as specified per document
**Output:** Three working documents for the product team's decision-making phase
**Not the same as:** PRD, design brief, project charter, stakeholder presentation

---

## Ground rules (active for entire session)

These two rules apply from the moment Frame A Problem begins and govern every output produced.

**Ground Rule 1 — Role transparency**
Every document and substantive output must open with a role line:
*Speaking as: [role] → To: [audience]*

Roles: Creative Strategy / Product / Experience Design / Content Design / Branding
Audience: Product team / Content designer / Experience designer / External audience

If a document draws on multiple roles simultaneously, name both: *Speaking as: Product + Experience Design → To: Product team*

This is a document element, not a conversational convention. It must appear in the rendered HTML output, not only in accompanying text.

**Ground Rule 2 — Active pushback**
Push back when:
- Sequencing skips something that would make the output stronger
- A framing is borrowed from one professional context but applied incorrectly to another
- A command assumes a decision that hasn't been made yet
- Something has been missed that will create problems downstream

Pushback format: direct and specific. Not "are you sure?" but "I'd push back on X because Y — here's what I think we should do instead."

---

## What this stage produces

Three documents. Each comes from a distinct professional tradition. Each serves a different function. They are not interchangeable and should not be merged.

```
Document 01 — Reframed research question
Document 02 — Constraints
Document 03 — Founding content brief
```

All three are rendered as a single HTML file with tab navigation. Each document is one page — prose, not slide deck, not bullet list. The three are working documents for the product team's decision-making phase, not handoff documents for the full team.

---

## Document 01 — Reframed research question

**Professional lineage:** IPA Creative Brief structure, adapted for internal product use
**Speaking as:** Creative Strategy → To: Product team
**Function:** Moves from the business question (what to build) to the behavioural/systems question (what the product is actually replacing or serving). Makes every subsequent product decision feel grounded rather than arbitrary.

### Structure (mandatory, in this order)

**The reframe** — a single question in a left-bordered box. Not a paragraph, not a list. One sentence or two at most. The reframe must move from category-level thinking to psychological/structural thinking. Test: could this reframe apply to a competitor's product? If yes, it's not specific enough.

**Key tension** — a dark inverted panel, serif italic. States the central contradiction the research surfaces — the thing that makes the problem harder than it looks and makes the obvious solution wrong. One paragraph. Must contain the word "but" or its equivalent — tension requires two sides.

**What this means** — three to four implications, each addressed to a named role. Format: arrow → **Role name:** implication statement. Each implication must be a direct consequence of the reframe and tension above it — not general product advice, not restated research findings.

### Conflation rules
Roles in "what this means" may be conflated where their implications derive from the same underlying argument. Experience design and creative strategy are frequently conflatable because both derive from the brand/experience positioning. Content design and product are usually distinct. Do not conflate more than two roles in a single implication — three-way conflations produce unfocused statements.

### What does NOT appear in Document 01
- Background section explaining the business question
- Methodology explanation
- Research citations
- Process scaffolding of any kind

The document starts with the reframe. Everything before the reframe is the process used to arrive at it — that process is not the deliverable.

---

## Document 02 — Constraints document

**Professional lineage:** GDS Alpha constraints format (UK Government Digital Service Service Standard)
**Speaking as:** Product + Experience Design → To: Product team
**Function:** Names what the product will not do and why, as explicit decisions rather than risks or preferences. Prevents scope creep, misaligned features, and wasted sprint cycles. Each constraint is a reference point when a decision is challenged.

### Constraint types (mandatory tagging)

**Cannot** — technical or ethical reality. Something the product is structurally unable to do given platform capabilities, user behaviour patterns, or ethical obligations. Grounded in evidence, not preference.

**Should not** — product identity decision. Something the product could technically do but that would alter what the product fundamentally is, not just what it offers. Grounded in the research question and portrait psychology.

**Will not** — founding commitment. A categorical exclusion that applies to all surfaces, all versions, all future iterations. Non-negotiable. Usually grounded in the language harvest or the core insight statement.

The distinction between these three types is the document's primary analytical value. Mixing them produces a document that reads as a wishlist rather than a decision record.

### Entry structure (per constraint)

Each constraint entry has:
1. Type tag (Cannot / Should not / Will not) — colour-coded pill
2. Title — a plain declarative statement of what is excluded, specific enough to be unambiguous
3. Body (expandable) — the grounding rationale. Must contain: the specific evidence or logic that makes this a constraint, not just a preference; and what it means for the product if this constraint is violated
4. Source citation — which phase of the EISR research or which role package established this

**Accordion interaction:** constraints are collapsed by default, expandable on click. This keeps the document scannable at the title level while preserving full rationale on demand.

### What does NOT appear in Document 02
- Risk register framing ("likelihood / impact" matrices)
- SWOT analysis
- Aspirational statements about what the product will do
- Constraints without grounding rationale
- More than 8–10 constraints (beyond this, constraints become noise)

---

## Document 03 — Founding content brief

**Professional lineage:** Sarah Richards / GDS content design discipline; Content Design 3.0 (UX Content Collective)
**Speaking as:** Content Design → To: Content designer (visible to UX and experience design)
**Function:** Establishes what content, aesthetic, and motion problems to solve first, before any copy is written. A founding brief — written pre-build, not as a retrospective audit.

### What "founding" means
This brief is written before the product has any content. It is not triaging existing content problems — it is anticipating them and prioritising them before they exist. The language is therefore forward-looking and directive, not retrospective and corrective.

### Priority matrix — the 2×2 axis

**Implementation rule:** Always build as SVG with absolutely-positioned node cards. Never use CSS grid, flexbox, or quadrant div containers for a 2×2 matrix. These collapse under dynamic content. The SVG approach:

```
- SVG canvas: fixed viewBox (recommended: 700x480)
- Axis lines drawn as SVG <line> elements with arrowheads as <polygon>
- Centre dashed dividers drawn as SVG <line stroke-dasharray>
- Quadrant labels as SVG <text> in a pale background colour
- Priority nodes as absolutely-positioned HTML divs over the SVG
- Node position set by left%/top% against the container dimensions
- Container must be position:relative; SVG must be position:absolute, pointer-events:none
```

**Positioning nodes:** Each node must have a genuinely distinct position on both axes — no clustering in a single quadrant. If all items initially appear to belong in the same quadrant, re-examine the engineering cost estimates to find the real differentiation. Minute differences in scale are legitimate and should be represented.

**Axis labels:** y-axis = User Impact (HIGH top, LOW bottom); x-axis = Eng. Cost (LOW left, HIGH right). Ghost quadrant labels (DO FIRST / SCHEDULE / QUICK WINS / DEFER) in pale background colour — present but not dominant.

### Expanded priority cards

When a node is clicked, its full card expands below the axis. Multiple cards can be open simultaneously, stacking in selection order. Cards collapse on second click or via a close button.

**Card structure (mandatory, in this order):**

1. Header — priority number, title, impact tag, cost tag, close button
2. Description — what this priority is and why it ranks here. This is the original priority rationale. It is NOT replaced by the three signals — it is the context that makes them readable.
3. Three-column body — Content / Aesthetics / Motion

**Non-redundancy rule:** Information that appears in a priority card's signals must not also appear as a standalone section above the matrix. The matrix and its expanded cards are the document. Standalone sections above the matrix duplicate information and create a two-tier document.

### The three signals — Content / Aesthetics / Motion

Each signal column contains:
- A specific recommendation for that dimension at that priority
- A source note at the bottom

**Source note format:**
- Direct source (verbatim from research): prefix with ↳
- Inferred from research: prefix with ⟳ and state the inference reasoning explicitly

**What each signal covers:**

*Content* — the specific copy approach, verbatim language to use, register, length constraints for this priority surface. Must reference actual phrases from the language harvest where applicable.

*Aesthetics* — design and brand direction for this surface: visual temperature, typographic register, spatial approach, what to avoid. Not a general brand guide — specific to this priority surface.

*Motion* — UX motion and interaction triggers specific to this priority: what animates, when, at what pace, what the motion communicates emotionally. Sourced from portrait psychology and analogous inspiration where direct research evidence is thin.

### What does NOT appear in Document 03
- User language table as a standalone section (language appears inside Content signals)
- Hard constraints list as a standalone section (constraints appear in Content signals and reference Document 02)
- Content purpose section explaining what the document does
- Content system note as a trailing section
- Any section that could be removed without losing information specific to a priority

---

## Rendering standards (all three documents)

### Typography
- Display / headings: Cormorant Garamond (serif) — signals editorial, considered register
- Body / UI: Epilogue — clean, functional, not generic
- Never: Inter, Roboto, Arial, system-ui for display purposes

### Colour system
- Background: #FAF8F4 (warm off-white — not clinical white)
- Ink: #0F0E0C
- Secondary ink: #3A3830
- Tertiary / labels: #7A7568
- Rule lines: #E2DDD5
- Accent for constraint type-cannot: #FCEEE9 / #8C2A0A
- Accent for constraint type-should-not: #EEF3EE / #1D5C38
- Accent for constraint type-will-not: #EBE9F5 / #2E2870

### Document shell
- Single HTML file, tab navigation between three documents
- Sticky nav bar at top, border-bottom only on active tab
- Max content width: 860px centred
- Padding: 3rem on document panels
- Footnote line at bottom of each document: 11px italic, sources only

### Ghost elements and patching discipline
**Critical rule:** After two rounds of patching the same section, do a full section rewrite rather than a third patch. Iterative patching on already-patched HTML creates ghost elements — old HTML surviving alongside new HTML and rendering unexpectedly. Symptoms: duplicate sections appearing, content appearing in wrong document panel, elements rendering outside their intended container.

Prevention:
- After each significant edit, verify with string search that old section markers are absent
- For the 2×2 matrix specifically: verify that `.quadrant.q-`, `.axis-outer`, `.axis-label-x`, and `.p-card` (as distinct from `.p-node`) are absent from the final file
- If any of these are found, do a full section rewrite — do not patch further

---

## Sequencing and dependency

Frame A Problem follows EISR research and depends on it directly. The three documents draw from:
- EISR Phase 6 (language harvest) → Document 03 content signals
- EISR Phase 7 (consumer insight statement) → Document 01 reframe and tension
- EISR Phase 8 (white space analysis) → Document 02 constraints
- EISR Phase 2 (portrait psychology) → Document 01 implications, Document 02 should-not constraints
- EISR Phase 9 (analogous inspiration) → Document 03 aesthetics and motion signals

Frame A Problem must be complete before:
- Product brief (needs the reframe and constraints as inputs)
- Design sprint (needs the content brief as a founding document)
- Engineering scoping (needs the constraints document)

---

## Quality tests

**Document 01 passes if:**
- The reframe cannot be applied to any competitor's product unchanged
- Each implication in "what this means" would change a decision if removed
- No process scaffolding is visible in the rendered document

**Document 02 passes if:**
- Every constraint is tagged by type and the type distinction is defensible
- Every constraint has a grounding rationale, not just an assertion
- Reading the titles alone gives a complete picture of what the product will not do
- Constraints numbered 1–8 all feel like genuine decisions, not preferences

**Document 03 passes if:**
- The axis is a true 2×2 with no clustered nodes
- Clicking a node reveals: description first, then three signals
- No information appears both in a standalone section and inside a card
- Every Content signal references at least one verbatim phrase from the language harvest
- Every inferred Aesthetics or Motion signal states why the inference was made

---

## Common failure modes

**Document 01: reframe that restates the problem**
Signs: the reframe sounds like "how do we make a better food tracking app?" Fix: the reframe must name the psychological or structural mechanism, not the product category. Ask: what is this behaviour actually serving?

**Document 01: implications that are general product advice**
Signs: any implication could apply to a competitor's product unchanged. Fix: every implication must be a direct consequence of the specific tension named above it.

**Document 02: constraints that are preferences**
Signs: a "should not" constraint would not actually change any decision if removed. Fix: apply the decision test — if this constraint were absent, would the team build something different? If not, it's not a constraint.

**Document 02: mixing constraint types**
Signs: a technical reality is tagged "will not" or a founding commitment is tagged "cannot." Fix: re-examine the type taxonomy. Cannot = structural impossibility or ethical boundary. Should not = identity decision. Will not = categorical founding commitment.

**Document 03: signals replacing description**
Signs: clicking a priority card reveals three columns but no explanation of what the priority is or why it ranks where it does. Fix: the description paragraph is mandatory and sits above the three columns. Signals answer "how." Description answers "what and why."

**Document 03: standalone sections duplicating card content**
Signs: user language or hard constraints appear both as sections above the matrix and inside card signals. Fix: remove standalone sections. All priority-specific content lives inside the cards.

**Document 03: CSS grid or flexbox 2×2**
Signs: the matrix renders as stacked rows rather than a proper axis when content height varies. Fix: rebuild as SVG with absolutely-positioned HTML nodes. This is the only implementation that holds regardless of card content height.

---

*Frame A Problem skill developed through the vibe eating app product development session, June 2026. Produced in conjunction with EISR — Experiential Insight Synthesis Research. Both skills function as a connected methodology: EISR generates the research inputs; Frame A Problem converts them into product team working documents.*
