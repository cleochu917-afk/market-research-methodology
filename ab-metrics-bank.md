# A/B Metrics Bank
## Metric selection by product type and decision type

Every A/B test requires three metric tiers:
- **Primary:** the single metric the test is designed to move. If it does not move, the test did not work.
- **Secondary (2–4):** metrics that explain why the primary moved or didn't. Behavioral signals between the intervention and the primary outcome.
- **Guardrail (1+):** hard thresholds. If a guardrail crosses its threshold, stop the test regardless of what the primary metric shows. A guardrail firing is a finding, not a failure.

*Guardrail logic:* a "bad win" is when the primary metric improves while the guardrail degrades something the product depends on. Standard conversion metrics optimize one number while quietly eroding user trust, experience quality, or retention. Guardrails prevent this. Source: Mixpanel (2025); Tang et al., Microsoft experimentation taxonomy.

Select the combination that matches your product type and the specific decision being resolved. Most tests require 1 primary + 2–3 secondary + 1 guardrail.

---

## Product type: Experiential / emotional wellbeing (applies to food noise product)

The core value is experiential — the product must feel right, not just be used. Standard transactional metrics (conversion rate, revenue per session) are wrong for this product type. Retention is emotional; the person returns because returning felt like something, not because of a streak or a notification.

### Decision type: Onboarding copy or framing

**Primary:** First session initiation rate — did the user complete the onboarding and initiate the first core interaction (vault entry, mode start)?

**Secondary:**
- Session depth — how far into the first interaction did the user go before exiting?
- Post-session affect rating (1–5) — self-reported immediately after first session close. A variant that produces higher initiation but lower affect creates pressure to engage rather than desire to engage — conditional win at best.
- Time to first capture — time elapsed between onboarding completion and first event-contingent capture initiated. Shorter indicates the onboarding successfully established the standing instruction.

**Guardrail:** Exit rate at the first onboarding screen — if a variant produces higher first-screen exit than baseline, the recognition framing has failed before any product value is demonstrated. Threshold: any variant producing >10% higher exit than baseline is stopped.

---

### Decision type: Capture mechanism (vault entry prompt design)

**Primary:** Capture completion rate — the percentage of event-contingent initiations that result in a submitted capture (any option: voice note, photo, sentence, rating only).

**Secondary:**
- Capture richness — character count and presence of sensory or emotional language in the verbatim response. Measured by content analysis of the first 50 captures per variant.
- Option distribution — which of the four capture options participants select. Heavy concentration on "intensity only" indicates the prompt is adding friction, not depth.
- Post-capture continuation — does the participant open a mode or revisit the vault within 60 minutes of capturing? Indicates whether the capture resolved or deepened engagement.

**Guardrail:** Abandonment rate — initiations that were started but not submitted. If a variant produces more abandoned captures than completed ones, the friction cost exceeds the depth benefit. Threshold: abandonment rate exceeding 30%.

---

### Decision type: Session and mode design

**Primary:** Session completion rate — participants who start a mode and reach the natural end rather than abandoning mid-session. Measured per mode separately.

**Secondary:**
- Mode selection distribution — which modes participants choose and whether selection matches the time-of-day peak data from ESM. Mismatch suggests mode entry copy is not matching the context.
- Post-session affect rating (1–5) — a variant with higher completion but lower affect produced compliance without satisfaction.
- Time in session — average session duration by mode. Very short sessions in a mode designed for depth indicate the mode is not holding attention; very long sessions in a mode designed for brevity indicate mismatch.

**Guardrail:** Food consumption within 30 minutes of session end (self-reported at next signal-contingent prompt). If a variant produces above-baseline food consumption immediately after sessions, the redirection mechanism is not working — the session satisfied the measurement without satisfying the experience.

---

### Decision type: Retention and vault return

**Primary:** Vault return rate at 24 hours and 48 hours — did the user return to review a previously logged capture? The vault's value rests on anticipatory pleasure and pattern recognition; if users never return, this value proposition is not operationally supported.

**Secondary:**
- Return depth — how many entries did the user review on return? A single-entry return is different from a sustained browse.
- Return affect rating — self-reported affect immediately after vault browsing. Does returning produce positive emotional signal?
- Days between first capture and first return — shorter intervals indicate higher anticipatory engagement.

**Guardrail:** App uninstall or inactivity >7 days following a session. Any variant that produces higher retention on a secondary metric while correlating with higher uninstall rates is a false win.

---

## Product type: SaaS / B2B task-completion products

### Decision type: Onboarding and activation

**Primary:** Activation rate — percentage of new users who complete a specific milestone action within the first session (completing a task, setting up a core feature, reaching a defined "aha moment").

**Secondary:**
- Time to activation — how long after signup the milestone action was completed
- Feature adoption rate — percentage of users who engage with a secondary feature within 7 days
- Day 7 retention — whether activated users return within the first week

**Guardrail:** Support ticket volume — if a variant activates more users but generates more "how do I do X" tickets, the onboarding is creating false confidence. Threshold: >15% increase in support tickets per activated user.

---

### Decision type: Core workflow

**Primary:** Task completion rate — percentage of users who successfully complete the primary workflow the test targets.

**Secondary:**
- Time on task — average time to complete. Shorter is not always better; for complex tasks, very short completion times may indicate skipping steps.
- Error rate — incorrect inputs or failed submissions
- Feature usage depth — did users engage with related features triggered by the workflow?

**Guardrail:** Data quality or integrity metrics — if a workflow change produces higher completion rates but lower data quality downstream, the test has moved the wrong metric. Threshold: any measurable degradation in downstream data quality.

---

## Product type: Consumer marketplace / e-commerce

### Decision type: Discovery and search

**Primary:** Click-through rate from search results to product pages.

**Secondary:**
- Search refinement rate — did the user modify their search after the initial results?
- Zero-results rate — searches that returned no results
- Add-to-cart rate from search pages

**Guardrail:** Bounce rate from product pages reached via search. A higher CTR that sends users to pages that immediately bounce indicates the search result matched the query but not the intent.

---

### Decision type: Conversion and checkout

**Primary:** Conversion rate — percentage of users who complete a purchase.

**Secondary:**
- Average order value
- Cart abandonment rate by step
- Return visit rate within 7 days

**Guardrail:** Refund and return rate. A conversion-optimized variant that increases impulse purchases can produce higher conversion while degrading satisfaction and increasing operational costs downstream.

---

## Product type: Content / media

### Decision type: Content presentation and discovery

**Primary:** Engagement rate — percentage of users who interact beyond passive consumption (shares, saves, comments, follows prompted by the content).

**Secondary:**
- Time on content — average time spent per content item
- Completion rate — percentage who reach the end of an article, video, or module
- Return visit rate — did the user return within 48 hours?

**Guardrail:** Unsubscribe or mute rate. Content optimized for engagement can increase interaction while increasing notification fatigue. Threshold: any increase in unsubscribe or mute rate that exceeds the engagement gain.

---

## Google HEART framework — applicable across product types

When the specific decision type does not map cleanly to the product type entries above, use HEART as a classification grid to select metrics. Source: Google Ventures; Mixpanel (2026).

| HEART dimension | What to measure | Typical primary metric |
|---|---|---|
| **Happiness** | Satisfaction, perceived value, emotional response | Post-session affect rating, NPS, CSAT |
| **Engagement** | Frequency and depth of interaction | Sessions per week, session completion rate, feature adoption rate |
| **Adoption** | New users reaching a first meaningful interaction | Activation rate, time to first core action |
| **Retention** | Users returning over time | Day 7 / Day 30 retention, vault return rate |
| **Task Success** | Efficiency and accuracy of completing a specific task | Task completion rate, time on task, error rate |

Select one HEART dimension as the primary for each test — the dimension most directly changed by the intervention. Use adjacent HEART dimensions as secondary metrics. The guardrail is typically the HEART dimension the intervention could inadvertently degrade.

---

## Metric selection rules — apply to every test

**One primary metric per test.** Multiple primary metrics produce ambiguous results — you cannot tell which one the intervention actually moved.

**Secondary metrics explain the mechanism.** Ask: what are the behavioral steps between my intervention and the primary outcome? Those steps are the secondary metrics. If secondary metrics do not move when the primary does, the causal mechanism is unclear.

**Guardrail threshold must be specified before the test runs.** A guardrail without a threshold is not a guardrail. "Threshold: any increase >X% relative to baseline" stated in advance. Post-hoc thresholds are rationalisation, not measurement.

**At Stage 3 scale (n=8–12), all findings are Directional at most.** Record direction and effect size. Do not report percentage changes as statistically significant. The synthesis format ends with: Committed / Revise and retest / Escalate to Stage 6.

---

*Bank initiated June 2026 from the vibe eating app research project. First documented entries: experiential/emotional wellbeing product type. HEART framework grounded in Google Ventures (2010); primary/secondary/guardrail taxonomy grounded in Microsoft experimentation taxonomy (Tang et al.) and Mixpanel guardrail metrics standard (2025). Add new product type entries when a study applies a metric combination not yet documented here.*
