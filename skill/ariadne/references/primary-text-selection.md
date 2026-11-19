# Primary Text Selection Protocol

## Scope

This protocol determines **WHAT should be read** when constructing a new Passage Package or revising a Package / Pathway selection. It does not replace Work Orientation, Corpus Scope / materialization, Bridge Load Check, Question–Evidence Fit, Guided Text Entry, Difficulty-First repair, or learner-facing support fading.

Run it on entering a new major work, a work-part with its own architecture, or an important chapter **only when that scope needs a new Package or a pathway revision**. Maintain the resulting map proportionately as the pathway moves. Do **not** re-run this protocol during ordinary learner reconstruction of an already-selected Package: that reconstruction uses the existing reading and evidence checks and updates coverage only. Re-open selection only when a defined revision trigger is met. It is a selection and coverage protocol, not a demand to map an entire book before any reading.

## 1. Macro Text Mapping

Before choosing a first Passage Package in the relevant scope, build or extend a bounded argument map. Each **Textual Argument Unit (TAU)** records:

| Field | Requirement |
|---|---|
| Textual Argument Unit (TAU) | A text-bounded move, question, or transition; not merely a famous theme. |
| Primary Text Location | Exact work / part / chapter / section and available page or locator range. |
| Main Philosophical Question | The question this TAU inherits or introduces. |
| Argumentative Function | e.g. problem-setting, model reconstruction, distinction, criticism, positive proposal, bridge, limitation, reply, application. |
| Relation to Other TAUs | prerequisite, develops, contrasts with, limits, or makes the next TAU intelligible. |
| Evidence Status | `TEXT_VERIFIED`, `GUIDE_SUPPORTED`, or `PROVISIONAL`. |

Evidence-status discipline:

- `TEXT_VERIFIED`: the Agent has inspected the cited primary text and the stated function is warranted by its wording and immediate argumentative context.
- `GUIDE_SUPPORTED`: an authoritative guide supports a provisional structural segmentation or relation, but the relevant primary locus has not yet been directly inspected enough to classify it `TEXT_VERIFIED`. Record the guide, exact pages, and its claim separately.
- `PROVISIONAL`: a hypothesis, table-of-contents lead, sparse locating information, or unverified model knowledge. It may guide further locating, but cannot by itself authorize an Anchor, Required Bridge, claim about an author’s structure, or a learner-facing reconstruction question.

Do not represent model familiarity with a work, a famous quotation, or a guide’s interpretation as a verified primary-text structure. Guides may check whether units are plausibly delimited and flag pressure points, but P (primary), G (guide), and A (Agent synthesis) remain separate.

Expand the map only as far as the current selection requires. On a new chapter, map its local TAUs and their explicit incoming/outgoing relation; do not fabricate a whole-book map. When later inspection revises a TAU boundary or relation, preserve the prior status in the audit note and correct the map.

## 2. Candidate Passage Evaluation

After mapping, identify the smallest continuous primary windows that could carry the current TAU. Evaluate candidates qualitatively, never through an unverified fixed weighted score.

### Required gates

A candidate may be selected for a learner-facing Passage Package only if all applicable gates pass:

1. **Structural evidence:** its TAU and relation to the current pathway are `TEXT_VERIFIED`, or are explicitly `GUIDE_SUPPORTED` while direct primary inspection is pending and the action is limited to `Locate`, not a substantive reconstruction.
2. **Argumentative necessity:** it either supplies an indispensable question, inferential move, positive account, limitation, or transition, or it is explicitly marked deferrable with a concrete reconsider trigger.
3. **Learner readiness:** Bridge Load / prerequisite probe confirms that the learner can enter it, or a smaller required bridge has been selected first.
4. **Evidence sufficiency:** the exact proposed window passes Question–Evidence Fit for the actual question. Assertion, example, and conclusion do not automatically supply a warrant.
5. **Source adequacy:** the applicable Corpus Scope / materialization rules pass; a guide or specialist source is added only when its role is currently necessary.

Only after the gates pass, compare candidates by:

- **Argumentative Necessity:** What indispensable work does this window do?
- **Structural Position:** Does it give the required incoming problem and outgoing move, rather than merely a memorable result?
- **Interpretive Importance:** Does a verified guide or specialist source identify a genuine hinge, ambiguity, or disputed locus? This cannot override primary structure.
- **Learner Readiness:** Is it the next intelligible transition for this learner? Use the existing Bridge Load Check; do not re-score it here.
- **Evidence Sufficiency:** Can the exact contiguous window support the assigned question without importing the answer?

For every actual selection, keep a compact internal Selection Record that can answer:

```text
Why this passage?
Why now?
Why not the adjacent alternatives?
What would be lost if skipped?
Primary evidence inspected:
Guide evidence, if any:
Uncertainty / revision trigger:
```

This record normally belongs in the relevant Text Map, Corpus Scope Card, or a selection audit artifact. Do not expose the full audit to the learner by default.

### Intervening-unit discipline

Do not treat pages or subsections that sit between a completed TAU and a candidate TAU as a required bridge merely because they are adjacent in the book. Inspect the intermediate unit and classify its local contribution:

- make it an `ESSENTIAL_BRIDGE` only when it supplies a term, warrant, contrast, or transition without which the target question is unreadable;
- otherwise mark it `DEFERRED` or `CONDITIONAL_BRIDGE`, stating what the current package safely relies on instead and the concrete trigger that would require return;
- a later TAU’s explicit restart from an already reconstructed structure can support deferral, but chapter order or topical resemblance cannot.

Record this comparison in the Selection Record’s “Why not the adjacent alternatives?” field. This preserves a continuous learner-facing window while preventing completeness-driven expansion and makes any skipped methodological, empirical, or contextual detour auditable.

### User-nominated entry ranges

Treat a learner's proposed starting section as a provisional Anchor rather than proof that it is self-sufficient. Before assigning it, inspect the nearest incoming and outgoing TAUs.

- Add the smallest preceding window as a Required Bridge when the anchor depends on an undefined term, contrast, example, or inferential move.
- Add the smallest following window as an Exit Bridge when it gives the first positive clarification of a term or contrast that the anchor states only negatively; otherwise the learner may retain a merely privative reconstruction.
- State the route as `Orientation → Required Bridge(s) → Anchor → Exit Reconstruction`, with one exact reason for every added window.
- Verify both edges against the contiguous source before labelling material as outside the window or as a `next-window preview`: a framing, classification, or qualification sentence may stand immediately before a subsection heading while still belong to the assigned range. Heading boundaries alone do not establish evidential boundaries.
- Do not widen backward for completeness, and do not replace an omitted bridge with Agent summary; use bounded primary reading and learner reconstruction, because a summary can hide the transition whose necessity is under assessment.

### Self-objection and qualification boundary

When an Anchor opens with an authorial self-objection, qualification, or apparent withdrawal, do not select only the opening pressure. Inspect the continuous text until its first explicit local disposition of the challenged claim:

- **resolved:** the text answers or replaces the objection;
- **limited:** the text restricts the claim’s scope, status, or standpoint;
- **retained as a problem:** the text neither affirms nor abandons the claim, but specifies what further analysis would be required.

Record the route as `Pressure → Qualification / Reply → Exit status`. Ask the learner to reconstruct this sequence rather than to decide from the opening paragraph whether the author simply rejects the earlier claim. Stop at the first explicit local disposition; do not annex a following chapter’s new positive account unless it is necessary to make that disposition intelligible. This prevents two opposite errors: treating a provisional self-critique as a final abandonment, and extending a bounded package merely to obtain a later theory.

## 3. Deadline-Aware Passage Pathway Planning

When the learner gives an explicit reading deadline, perform this planning check while constructing or revising the Passage Pathway, before issuing any Reading Action. Record only what the deadline changes:

```text
Required primary target:
Available time:
Essential primary dependencies:
Companion guide cost:
Deferrable context:
Minimum viable understanding:
```

Classify each candidate window or support item as exactly one of:

```text
CORE_REQUIRED
ESSENTIAL_BRIDGE
CONDITIONAL_BRIDGE
COMPANION_CONTEXT
DEFERRED
```

- `CORE_REQUIRED`: the user’s named primary target and any continuous text needed to reconstruct its local argument.
- `ESSENTIAL_BRIDGE`: a primary window whose omission would make the Core target’s decisive term, contrast, inference, or transition unreadable. It cannot be replaced by a guide, Agent summary, or contextual label.
- `CONDITIONAL_BRIDGE`: a bounded primary window with a stated activation trigger; do not pre-read it merely for theoretical completeness.
- `COMPANION_CONTEXT`: a bounded guide or orientation source that passes the existing Companion Reading gate. State its contribution, reading cost, and return-to-primary target; reject it if that contribution is too small for its cost.
- `DEFERRED`: relevant but non-blocking material. Record the Context Debt, risk, and repayment trigger when its omission may later matter.

Do not expand a deadline-bounded pathway merely for theoretical completeness. Conversely, do not omit an Essential Bridge merely because a guide can describe it. The plan may propose sequence and classifications, but **No formal Reading Action is issued by a regression or planning check.**

## 4. Argument Coverage Record

Maintain a lightweight coverage record for mapped TAUs. Its purpose is to detect structural omissions, not to make every TAU a required reading task.

```text
Coverage status: PENDING | READ | RECONSTRUCTED | DEFERRED | SKIPPED_WITH_REASON
Agent inspection: not inspected | inspected
Learner contact: unread | read | reconstructed
Reason / evidence:
Reconsider trigger:
```

Meanings:

- `READ`: the learner has read the designated primary window; it does not imply reconstruction.
- `RECONSTRUCTED`: the learner has reconstructed the unit’s local argument with the required evidence check.
- `DEFERRED`: not selected now; record why and the condition that would make it necessary.
- `SKIPPED_WITH_REASON`: deliberately excluded for this pathway; record what the present pathway can safely do without it and what would be lost if its exclusion becomes unsafe.
- `PENDING`: not yet inspected or selected enough to classify.

Never conflate:

```text
Agent inspected the text
≠ learner read the text
≠ learner reconstructed the argument.
```

Before marking an important local TAU or a pathway segment sufficiently covered, audit—only where applicable—whether it omits:

- necessary problem-setting;
- a live competing interpretation or rival model;
- a core inferential step;
- the positive account after a critique;
- an important stated limitation, qualification, or reply.

These are audit dimensions, not a fixed form that every philosophical text must possess. A negative result must be explicit: e.g. “no rival model stated in this unit,” “positive account belongs to a later mapped unit,” or “limitation remains `PENDING`.”

## 5. Integration and Correction

The controlling sequence is:

```text
Text Mapping
→ Candidate Selection
→ Bridge Load
→ Question–Evidence Fit
→ Reading Action
→ Argument Coverage Update
```

Responsibilities remain distinct:

- This protocol: **WHAT** to read, why this TAU, and what is covered or intentionally deferred.
- Bridge Load / prerequisite probe: **WHEN** the learner can enter it.
- Guided Text Entry / reading modes / question openness: **HOW** the learner reads it.
- Question–Evidence Fit and Difficulty-First diagnostics: whether the assigned window and question remain valid once reading begins.

Run this protocol at Package construction or Package / Pathway revision, not as a repeated step in ordinary learner reconstruction. Ordinary reconstruction follows the already-selected package and updates coverage; it reopens selection only if a revision trigger below is met.

Do not create a parallel scoring engine, duplicate existing checks, or treat a guide as a substitute for either the primary window or learner reconstruction.

Re-open selection only as a Package / Pathway revision if primary inspection reveals a mistaken TAU boundary; a guide identifies a consequential nearby bridge or limitation; Question–Evidence Fit fails; the learner signals a pathway gap; coverage exposes that an omitted TAU is actually required; or Distributed Conceptual Grounding verifies a Definition or Argument Dependency whose goal-relative value, learner need, alternatives, and reading cost justify a route change. Correct the map and Selection Record first, then re-run the existing downstream checks. Do not treat ordinary reconstruction, a term match, or Agent-only local consultation by itself as a reason to re-run selection.

## 6. Pedagogical Non-Spoiling

The Agent may maintain an internal map and audit record, but learner-facing output normally includes only:

- the current location;
- the minimum structural locator needed to make it intelligible;
- the exact continuous reading range;
- one question that the window supports.

Do not give an un-read later unit’s full argument, a whole-work argument summary, or a guide’s answer before the learner’s primary encounter. The learner may request the complete map or selection audit at any time; then show evidence status and P/G/A provenance rather than concealing uncertainty.

## 7. Completion Criterion

A selected Passage Package is selection-ready only when its Textual Argument Unit (TAU) is mapped with stated evidence status, its Selection Record answers the four audit questions, applicable gates pass, its exact window is set, and its current coverage state is recorded. This protocol does not mark the TAU learner-complete; only actual learner reading and reconstruction can do that.

## 8. Retrospective Read-Only Selection Audit

Use this mode when the user asks whether an already-running primary-text pathway selected the right work, chapter, entry point, bridge, or order. It is a **selection review**, not ordinary learner reconstruction and not a license to repair the project automatically.

### 7.1 Freeze the audit boundary

1. Copy the user’s non-negotiable limits into the audit header: for example, no Skill edit, no state change, no learner-record change, no new reading action, or no canonical-next-action change.
2. Read the canonical state and relevant mirrors only to establish a snapshot. Do not invoke state transitions, backfill coverage, change a completed node, or normalize stale mirrors during the audit.
3. If a report artifact is permitted, write only that report. Keep all proposed repairs explicitly prospective.

### 7.2 Reconstruct history before judging it

Read the smallest artifact set that can establish: project questions; original selected windows; current state; maps; scope cards; learner reconstructions; source matrix; and decision records where available.

Record three distinct statuses for every material claim:

```text
AGENT_INSPECTED
LEARNER_READ
LEARNER_RECONSTRUCTED
```

Never infer a Parent TAU reconstruction from completed micro-nodes. Preserve a local accomplishment as an accomplishment even when the audit finds a missing structural bridge.

Do not retrofit a historical selection rationale from a later audit conclusion — if no contemporaneous comparison or rationale is found, report it as undocumented rather than treating an inferred rationale as history.

### 7.3 Build a bounded comparative map

1. Map the selected work-part and only the genuinely plausible alternatives. Inspect exact primary windows sufficient to identify each TAU’s question, local function, incoming/outgoing relation, and relevance to the project questions.
2. Include incoming architecture when the historical selection entered in the middle of a chapter; a memorable local passage may otherwise lack its problem-setting or transition.
3. Mark every relation as `TEXT_VERIFIED`, `GUIDE_SUPPORTED`, or `PROVISIONAL`. Keep P (primary), G (guide), A (Agent synthesis), and learner reconstruction separate.
4. Treat distributed retrieval as candidate generation. Classify each result as `TERM_MATCH`, `CONTEXT_VERIFIED`, `CONCEPTUAL_RELATION_SUPPORTED`, or `DEPENDENCY_CONFIRMED`; only the last two can support a relation, and only a confirmed definition or argument dependency presumptively justifies a required bridge.

Do not turn chapter order, topical resemblance, a term match, or prior time invested into a textual dependency.

### 7.4 Compare paths qualitatively

For each actual or proposed route, answer:

```text
Why this passage?
Why now?
Why not adjacent alternatives?
What would be lost if skipped?
```

Assess argumentative necessity, structural position, interpretive importance, learner readiness, evidence sufficiency, bridge load, and fragmentation risk without inventing weighted scores. Distinguish:

```text
TEXTUAL ARGUMENT DEPENDENCY
PEDAGOGICAL PREREQUISITE
```

A pedagogically useful bridge does not establish that the author’s argument strictly depends on it.

### 7.5 Diagnose the current pathway without rewriting it

Separate at least these possibilities:

- selection/entry-point error;
- omitted structural bridge;
- distributed conceptual grounding need;
- Question–Evidence mismatch or genuine textual limit;
- decomposition/reintegration failure.

Do not collapse them into a single “the learner did not understand” diagnosis. In particular, a sequence of locally supported sentence checks can still fail to produce Parent-TAU reconstruction.

### 7.6 Report contract and future proposal

A retrospective audit report should include:

1. Historical Path Reconstruction;
2. Comparative TAU Map;
3. Path comparison;
4. Existing learner coverage and its limits;
5. Missing dependencies / DGC record;
6. Pedagogical assessment;
7. Prospective path recommendation;
8. Recommended Next Action **Proposal**;
9. Evidence and uncertainty register.

Use one conclusion label: `CURRENT_PATH_VALID`, `CURRENT_PATH_VALID_WITH_MISSING_BRIDGES`, `PATH_REVISION_RECOMMENDED`, or `INSUFFICIENT_EVIDENCE`.

A next-action proposal must state the target, exact verified window (or explicitly say that bounded primary mapping must occur first), Parent TAU, why-now rationale, prerequisite status, expected philosophical operation, and reintegration target. It is not a Reading Action. End by restating what was not changed and wait for user authorization before any implementation.
