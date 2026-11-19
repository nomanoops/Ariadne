# Guide Introduction Decision Procedure

Use this procedure as decision support when considering a learner-facing `GUIDE_ORIENTATION_READING`, `GUIDE_ORIENTED_ENTRY`, `GUIDE_CLOSE_READING`, or `COMMENTARY_ASSISTED`. It is not a universal approval gate for all secondary-source use, adds no guide mode, does not make guides default background material, and does not alter the existing Guide Reading Action. It is a pedagogical/audit record, not a new operational state machine. It governs learner reading only: bounded `AGENT_SOURCE_CONSULTATION` is handled by `references/sense-making-priority.md` and must not be recorded as learner guide reading.

The main Skill's cross-protocol evidence discipline remains binding here: distinguish `P — Primary textual support`, `G — Guide interpretation`, and `A — Agent synthesis`; G cannot be presented as a direct primary-text statement, and A cannot be presented as scholarly consensus.

## 1. Primary Sufficiency Check

Assess the exact primary window and its exact current question as `SUPPORTED`, `PARTIALLY_SUPPORTED`, or `NOT_SUPPORTED`.

- `SUPPORTED → default PRIMARY_FIRST.` A bounded `COMPANION` evaluation remains allowed when a guide has a recorded structural, historical, problem-field, interpretive, or secondary-literacy contribution that is worth its reading cost; it does not require a prior learner failure or proof that primary-only reading is insufficient.
- `PARTIALLY_SUPPORTED`: classify the gap before selecting any **REMEDIAL** guide: question too broad; adjacent primary warrant missing; earlier bridge missing; package overload; local parsing / hinge difficulty; or external context dependency.
- `NOT_SUPPORTED`: first seek adjacent primary text, an earlier primary bridge, or an alternative primary orientation window. A required primary bridge must be assigned before a guide; a guide cannot substitute for it.

## 2. Guide Purpose and Trigger Classification

Record one guide purpose before selecting a learner-facing guide:

```text
Guide purpose: `REMEDIAL` | `COMPANION`
```

- `REMEDIAL` resolves an already recorded local understanding difficulty. It uses one of: `STRUCTURAL_LOCATION`, `HISTORICAL_OR_POLEMICAL_DEPENDENCY`, `PRIMARY_HINGE_REMAINS_OPAQUE_AFTER_PARSE`, `CONSEQUENTIAL_INTERPRETIVE_DISAGREEMENT`, or `SECONDARY_READING_AS_EXPLICIT_LEARNING_GOAL`.
- `COMPANION` proactively improves a named primary encounter through an authoritative guide’s structural location, historical context, problem field, bounded interpretive perspective, or explicit secondary-reading objective. It does not require a prior learner failure and does not require primary-only reading to be inadequate.

Guide availability, Agent desire to explain more, and generic background usefulness cannot by themselves select a guide. `BRIDGE_OVERLOAD`, `QUESTION_EVIDENCE_MISMATCH`, ordinary syntax difficulty, and ordinary local parsing difficulty remain primary-text problems unless a distinct recorded `REMEDIAL` or `COMPANION` basis survives the applicable repair.

## 3. Primary-Repair Priority

For `REMEDIAL`, use this default order before guide selection:

```text
narrow question
→ extend adjacent primary
→ locate earlier primary bridge
→ decompose overloaded package
→ local parsing / hinge micro-check
→ only then assess guide
```

If any step resolves the necessary question, record `Guide decision: DEFERRED` and its reason. A guide cannot repair a `BRIDGE_OVERLOAD`; only smaller primary windows plus user reconstruction can do that.

For `COMPANION`, do not require the learner first to fail or prove primary-only insufficiency. Instead, verify that the primary target and any Essential Bridge remain assigned; then justify why the proposed guide contribution is non-duplicative, worth its reading cost, exact and bounded, and pedagogically non-spoiling. If the contribution is duplicative, too small for its cost, or spoils the primary encounter, record `Guide decision: DEFERRED` with the reason.

## 4. Guide Role / Mode Selection

Reuse the least intrusive existing route; `REMEDIAL` and `COMPANION` are guide purposes, not reading modes.

| Purpose / recorded basis | Allowed route and limit |
|---|---|
| `COMPANION` structural location, historical/polemical context, problem field, or bounded entry perspective | `GUIDE_ORIENTED_ENTRY` with `GUIDE_ORIENTATION`; do not pre-explain the specific passage-level answer. |
| `REMEDIAL` `STRUCTURAL_LOCATION` | `GUIDE_ORIENTED_ENTRY`; guide supplies only chapter / argument location. |
| `REMEDIAL` `HISTORICAL_OR_POLEMICAL_DEPENDENCY` | `GUIDE_ORIENTED_ENTRY` or bounded `GUIDE_ORIENTATION`; do not pre-explain substantive doctrine. |
| `REMEDIAL` `PRIMARY_HINGE_REMAINS_OPAQUE_AFTER_PARSE` | `GUIDE_CLOSE_READING` or bounded `COMMENTARY_ASSISTED`. |
| `REMEDIAL` `CONSEQUENTIAL_INTERPRETIVE_DISAGREEMENT` | `GUIDE_CLOSE_READING` plus Interpretive Contrast / FIDD as needed. |
| `REMEDIAL` or `COMPANION` `SECONDARY_READING_AS_EXPLICIT_LEARNING_GOAL` | `GUIDE_CLOSE_READING`. |

Every selected route remains primary-anchored and retains the existing Guide Reading Action where `GUIDE_CLOSE_READING` is required. A guide cannot replace the named primary target or any Essential Bridge.

## 5. Return-to-Primary Target and Scope Card Record

Before issuing a guide action, record the exact primary window, hinge, reconstruction, or comparison to which the learner returns. Work-level guides may establish only problem field, method, architecture, or entry motivation; they cannot answer a later passage question. Passage-level guides remain local and cannot become a whole-work background lecture.

When guide use is triggered, record in the Scope Card — or in the same plain scope note where the project keeps no corpus record:

```text
Guide purpose:
Guide trigger category:
Primary sufficiency:
Primary remediation attempted:
Why primary remains insufficient:             # required for REMEDIAL when applicable
Companion contribution to learning:           # required for COMPANION
Why this contribution is worth its reading cost:  # required for COMPANION
Exact guide window:
Guide's scholarly role:
Non-spoiling boundary:
Guide mode:
Return-to-primary target:
```

The learner must personally read the exact guide window for every learner-facing `REMEDIAL` or `COMPANION` guide action. A source consulted only by the agent is `AGENT_SOURCE_CONSULTATION`, not learner guide reading.

When no guide is triggered, record:

```text
Guide decision: DEFERRED | NOT_NEEDED
Reason:
```

## Work Orientation guide rule

`PRIMARY_ORIENTATION_READING` has priority only when an authorial window performs the **same** selected orientation work. A bounded `COMPANION` `GUIDE_ORIENTATION_READING` may proactively supply a non-duplicative structural, historical, problem-field, methodological, or formal coordinate when that coordinate is materially relevant to the stated learning objective—even if the first primary passage is comprehensible without it.

A Work-Level `COMPANION` decision must record:

```text
Selected coordinate and its objective-relative relevance:
Exact guide section/pages:
Incremental value over the available primary window and learner knowledge:
Why the contribution is non-spoiling:
P/G/A provenance boundary:
One learner reconstruction question:
Return-to-primary target:
```

Do not treat logical necessity for the first Passage Package as the sole relevance test. Classify remaining context as:

```text
REQUIRED_FOR_WORK_ORIENTATION
HELPFUL_BUT_DEFERRABLE
NOT_NEEDED_NOW
```

`REQUIRED_FOR_WORK_ORIENTATION` includes both immediate ingress needs and coordinates without which the current learning objective would misdescribe the work or omit a material work feature. A merely helpful but deferrable context cannot trigger a guide. A guide remains bounded: it does not make a full biography, intellectual history, secondary-literature survey, or guide accompaniment for every Passage Package mandatory.

The learner must read the exact `COMPANION` window and reconstruct its contribution. An Agent's paraphrase or a guide consulted only by the agent is not learner-facing orientation completion. Only if a guide action becomes the next action does the learner's own plan record it. These pedagogical fields never select an action themselves.
