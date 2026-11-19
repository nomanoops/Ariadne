# Specialist Secondary Literature Close Reading

Use this protocol only for a bounded specialist source whose argument must be understood for the current task. It is not an excuse to begin literature reading, to replace primary reconstruction, or to turn a specialist article into an introductory lecture. The learner's project decides the project-level source role and next action; this reference decides whether and how a learner-facing secondary passage is entered.

## 1. Purpose and necessity gate

Before assigning a specialist window, record exactly one purpose:

```text
ORIENTATION
CONCEPT_CLARIFICATION
INTERPRETIVE_SUPPORT
INTERPRETIVE_DISPUTE
ARGUMENT_RECONSTRUCTION
SOURCE_CHAINING
COUNTEREVIDENCE
```

Then ask, in order: whether the **current question can be resolved from the primary text**; whether **a guide can resolve the gap**; whether a **genuine interpretive or research gap** remains; whether this specialist source addresses that gap; and whether its argument—not merely bibliographic awareness—is necessary now. If any earlier route suffices, otherwise record `DEFER`. A specialist source must not be close-read merely because it is important, local, or available.

`GUIDE` serves orientation, structure, entry, and bounded conceptual neighborhood. `SPECIALIST SECONDARY` serves an interpretive argument, specific dispute, textual warrant, scholarly intervention, or counterevidence. Do not use a specialist paper as an introductory guide unless the Scope Card records its exact section as a bounded `ORIENTATION` role.

## 2. Secondary Passage Package

For an allowed source, create a **Secondary Passage Package**. It is a learner-facing audit record, not a new operational state machine:

```text
Source:
Source role:
Reading purpose:
Exact section/pages:
Target primary issue:
Author's main claim:
Immediate argumentative target:
Evidence used:
Warrant / inferential move:
Primary text relied upon:
Interpretive commitment:
Rival / alternative:
Known limitation:
Question–Evidence Fit:
User reconstruction question:
Return-to-primary target:
```

Where a Literature Matrix exists, the Scope Card uses the stable Matrix `source_id` and, when specialist use is actual, records `specialist_decision`: status, specialist source ID, purpose, exact window, primary anchor, dispute status, user-read status, and exit status. These fields never authorize an action; only a decided global next action reaches canonical operational state through the existing transition layer.

## 3. Reading sequence and user reconstruction

Use this sequence without giving a detailed whole-paper summary first:

```text
1. Locate Argument
2. Exact Secondary Window
3. User Reconstruction
4. Claim–Evidence–Warrant Check
5. Primary Anchor Check
6. Interpretive Commitment Check
7. Rival / Limitation Check
8. Calibration
9. Return to Primary / Research Map
```

At Locate Argument, give only why the section matters, what claim to look for, which primary issue it bears on, and exact pages. The user must then reconstruct: (1) the author’s claim, (2) target or problem, (3) evidence, (4) warrant from evidence to claim, and (5) the author’s own interpretive move. Repeating a conclusion is not completion.

For every important argument, record `CLAIM → EVIDENCE → WARRANT`; add `ASSUMPTION`, `TARGET`, `OBJECTION`, or `RESPONSE` only when they carry the local inference. Run Question–Evidence Fit against the exact secondary window. If the question is too strong for it, narrow it or minimally extend the secondary window; do not repair a secondary mismatch with a longer Agent summary.

## 4. Evidence, anchor, and commitment checks

Use this evidence taxonomy:

```text
S1 — Secondary author quotation/paraphrase of primary
S2 — Secondary author's textual inference
S3 — Historical/contextual evidence
S4 — Conceptual reconstruction
S5 — Comparative inference
S6 — Agent synthesis
```

Keep these distinct from `P — Primary textual support`, `G — Guide interpretation`, and `A — Agent synthesis`. A secondary interpretation is never automatically a primary textual fact.

For any interpretation of a philosopher, perform a Primary Anchor Check: exact primary locus supplied; quotation accuracy; adequate context; whether the interpretation is stronger than the text; and whether the primary supports, strongly implies, or does not establish the claim. If a significant claim lacks a usable anchor, mark `UNANCHORED_INTERPRETIVE_CLAIM`. It is not automatically rejected, but cannot be promoted as primary-supported.

Then ask what acceptance of the interpretation commits us to: a concept boundary, chronology, relation between texts, methodological assumption, influence attribution, or strong/weak primary reading. Record it in the Debate Map, Literature Matrix, or a candidate gap as appropriate—not as a user-confirmed research claim.

## 5. Rival, difficulty, and FIDD integration

If a specialist materially changes a primary claim, hinge, concept boundary, text relation, or research consequence, trigger Interpretive Contrast / FIDD rather than silently adopting it. Compare Reading A, Reading B, primary evidence, what differs, research consequence, and current status. FIDD is:

```text
Frame disagreement
→ Identify interpretive hinge
→ Direct textual evidence
→ Determine research consequence
```

Conclude only `DEFER`, `LIVE_DISPUTE`, `PROVISIONAL_PREFERENCE`, or `REQUIRES_MORE_EVIDENCE`; no final interpretive conclusion without the existing Human Gate.

Diagnose difficulty as `ARGUMENT_STRUCTURE_GAP`, `PRIMARY_REFERENCE_GAP`, `TERMINOLOGY_GAP`, `HISTORICAL_CONTEXT_GAP`, `INFERENCE_GAP`, or `RIVAL_POSITION_GAP`. Apply the least sufficient support:

```text
Point → Argument Map Hint → Evidence Locator → Contrast → Limited Reveal
```

Limited Reveal addresses only the local inferential hinge and is followed by user reconstruction. It does not become a longer paper summary.

## 6. Exit, records, and Card Harvest boundary

A secondary reading completes only when the user can state the author’s claim, evidence, warrant, interpretive move, primary anchor, strongest consequential limitation/rival, and why it matters to the current research. Then return to the named primary window or Research Map; do not continue into a new source by default.

It may produce a literature-map, concept-matrix, debate-map, candidate-gap, counterevidence, or argument-evidence candidate update. It cannot automatically produce an Active Research Question, thesis, or final interpretive commitment. Card Harvest may propose L/E/P candidates only with provenance separated among source-author claim, user-confirmed understanding, and Agent synthesis; a paper summary never automatically becomes a permanent note.
