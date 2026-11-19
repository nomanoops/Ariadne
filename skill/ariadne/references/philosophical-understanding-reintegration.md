# Philosophical Understanding & Reintegration Protocol

## Scope and boundary

Use this protocol whenever a learner reports broad difficulty in a **Guided Primary Text Close Reading**, or when a Parent **Textual Argument Unit (TAU)** is being consolidated or exited. It applies in Mode 0, Mode 1, and Mode 2 whenever that close-reading practice actually occurs. Mode changes corpus/entry governance; it does not relax these controls.

This protocol strengthens existing Difficulty-First Hinge Analysis, Support Fading, Question–Evidence Fit (QEF), Passage Package Exit Reconstruction, and TAU Coverage. It creates no canonical action status, no parallel workflow state machine, and no automatic change to any project state file.

Run it only at the needed granularity:

- **ordinary reconstruction:** reuse the selected package, current TAU, and current evidence; perform the required local calibration and state the question’s cognitive demand without rebuilding maps;
- **difficulty trigger:** perform a focused diagnosis and select one remediation route;
- **TAU consolidation / Package or Pathway revision:** restore relations, update coverage, and use an existing controlled transition only if the actual global action changes.

Do not rerun the Primary Text Selection Protocol during ordinary reconstruction. It remains limited to Package construction or Package / Pathway revision.

## 1. Difficulty diagnosis before decomposition

A broad learner signal—e.g. “these pages basically make no sense,” “I do not know what this passage is saying,” or “I know each sentence but not what they mean together”—does **not** default to sentence-by-sentence decomposition.

First form a bounded internal diagnosis from the learner’s prior answers, the current text, and the current Scope Card. Classify one or more of:

```text
LANGUAGE / TRANSLATION
CONCEPT_FUNCTION
BACKGROUND / EMPIRICAL_BRIDGE
INFERENCE / WARRANT
ARGUMENT_STRUCTURE
TEXTUAL_GAP
```

Use the smallest action that follows from the diagnosis:

| Diagnosis | Default remediation, subject to evidence |
|---|---|
| `LANGUAGE / TRANSLATION` | local parsing or translation control |
| `CONCEPT_FUNCTION` | concept clarification tied to its local textual role |
| `BACKGROUND / EMPIRICAL_BRIDGE` | minimal empirical bridge or required primary bridge |
| `INFERENCE / WARRANT` | existing Hinge Analysis, argument mapping, or bounded primary extension |
| `ARGUMENT_STRUCTURE` | local argument mapping, Parent-TAU consolidation, or passage decomposition if actually needed |
| `TEXTUAL_GAP` | primary extension; earlier bridge; guide close reading; bounded secondary support; or explicit unresolved limitation |

Several diagnoses may coexist. Ask the learner one minimal clarification question only when the unresolved classification would lead to materially different teaching actions. Do not interrogate merely to fill a form.

Decomposition is permissible only when it addresses the diagnosed difficulty. It is never the default translation of “I do not understand.”

## 2. Question–Evidence Fit plus Cognitive Demand

Keep QEF statuses unchanged:

```text
SUPPORTED | PARTIALLY_SUPPORTED | NOT_SUPPORTED
```

For question-type-sensitive completion semantics, bounded source consultation, and working interpretations, follow `sense-making-priority.md`. Direct textual reconstruction still requires exact-window support; interpretive sense-making may use explicitly labeled P/G/B/A/WI material without completing the TAU.

For every Reading Question, also state the principal **Cognitive Demand**—the operation the learner is being asked to perform:

```text
TEXT_LOCATION
PARAPHRASE
EVIDENCE_BOUNDARY
CONCEPT_FUNCTION
RELATIONAL_EXPLANATION
INFERENTIAL_RECONSTRUCTION
ARGUMENT_INTEGRATION
TRANSFER / APPLICATION
```

These are instructional-operation labels, not canonical state values or a ranking of question quality.

- `TEXT_LOCATION`, `PARAPHRASE`, and `EVIDENCE_BOUNDARY` can be necessary local scaffolds.
- A successful low-demand answer does not itself establish that a Parent TAU is understood or reconstructed.
- A higher-demand question is not automatically better. Demand must match the exact evidence, learner readiness, and current pedagogical task.
- `SUPPORTED` means the text can answer the question; it does not mean the question tests philosophical understanding sufficiently for a TAU exit.

Record the demand compactly in the existing Scope Card or learning-state question record. Do not create a new data object.

## 3. Decomposition–Reintegration

**Decomposition is a remediation technique, not a substitute for reconstruction.**

If a Parent TAU is split into micro-nodes, retain the Parent TAU in existing Scope Card / learning-state fields. For every micro-node, record only:

```text
Parent TAU:
Current pedagogical role:
What this node establishes:
What remains unresolved:
Return / reintegration target:
Cognitive demand:
```

Use existing Passage Roles (`Entry / Orientation`, `Bridge`, `Anchor`, `Counterexample / Pressure`, `Consolidation / Retrieval`) rather than a new node taxonomy.

Schedule a consolidation attempt when one or more of these applies:

1. an important conceptual transition has been traversed;
2. a local argumentative relation has been established;
3. enough evidence is present to attempt Parent-TAU reconstruction;
4. a sequence of extraction-only tasks risks fragmenting the learner’s understanding;
5. the learner asks for an overall explanation;
6. the same concept cluster repeatedly generates difficulty.

A micro-node count may warn of fragmentation but must not mechanically determine consolidation. Textual structure and the diagnosed obstacle decide.

Until consolidation, local completion means only that node’s designated operation was successfully performed. It does not complete the Parent TAU or discharge its Context Debt.

## 4. Parent TAU exit reconstruction

Keep two facts distinct:

```text
LOCAL NODE COMPLETED
≠ PARENT TAU RECONSTRUCTED
```

A Parent TAU may involve one or more of these operations, as the text actually requires:

```text
CONCEPT INTRODUCTION
CONCEPTUAL DISTINCTION
RELATIONAL ORGANIZATION
INFERENTIAL ARGUMENT
CRITICAL RESPONSE
QUALIFICATION
THEORETICAL TRANSITION
```

They are optional operation-types, not a fixed premise–conclusion template.

A TAU Exit Reconstruction must, where applicable, show that the learner can:

1. state the philosophical problem the TAU handles;
2. explain the function of its central concept(s) or proposition(s);
3. reconstruct the key relation the text actually establishes;
4. distinguish textual argument from assertion or mechanism the text has not established;
5. identify a material unresolved question or textual gap; and
6. locate the TAU’s relation to an adjacent TAU when that relation is needed for the current pathway.

Do not demand a warrant the primary text does not provide. It is permissible to record both:

```text
TAU adequately reconstructed for its limited operation
+ specific unresolved textual gap
```

Only an exit reconstruction appropriate to the TAU’s actual operation may update Parent-TAU coverage to `RECONSTRUCTED`. If the learner has read the required windows but has not completed that exit, use the existing coverage distinction (`READ`, `DEFERRED`, or `PENDING` as appropriate). Local-node completion never auto-promotes coverage.

## 5. Unresolved hinge management

Use the existing Hinge Analysis, but classify a repeated or consequential hinge by its pedagogical disposition:

```text
RESOLVABLE_IN_CURRENT_WINDOW
REQUIRES_PRIMARY_EXTENSION
REQUIRES_EARLIER_BRIDGE
REQUIRES_GUIDE
GENUINELY_UNRESOLVED_IN_AVAILABLE_TEXT
NON_BLOCKING_FOR_CURRENT_TAU
```

If a hinge is necessary to the TAU’s stated operation, do not declare the Parent TAU reconstructed until it is resolved or the exit explicitly limits the achieved understanding and records the unresolved textual gap.

If it is non-blocking, learning may proceed. Record what the current TAU can safely establish, what remains open, and the trigger for revisiting it. Do not turn every unanswered question into a blocker.

Guide use has three distinct routes. A `COMPANION` guide may be proactively selected when its bounded, non-duplicative contribution improves the learner’s primary encounter; it does not require a prior learner failure, but it remains primary-anchored and cannot pre-complete the learner’s core interpretation. For `REMEDIAL`, follow the applicable primary repair before assigning a bounded guide action for a recorded difficulty. `AGENT_SOURCE_CONSULTATION` may inform the agent’s explanation or a labeled Working Interpretation without becoming learner guide reading, requiring a learner-facing Guide Reading Action, or creating a Passage Package. In all three routes, a guide may clarify a hinge but cannot manufacture a primary warrant. The detailed learner-facing decision aid is `guide-introduction.md`.

## 6. Context restoration at consolidation

At a suitable Parent-TAU consolidation or exit, restore three relations without spoiling unread text:

```text
LOCAL: What philosophical operation did this text actually perform?
STRUCTURAL: How does this TAU relate to the current chapter or adjacent TAUs?
PROJECT: What does it contribute to the learner’s current inquiry, and what does it not yet establish?
```

Do not force every sentence to answer the project’s central question. A TAU may be necessary preparation only. For example, a local reading of one concept must not be presented in advance as a completed ontology of the whole domain.

## 7. Record and performance discipline

Reuse existing Scope Card and learning-state structures. Do not build a new complete audit object or mirror every pedagogical field into canonical state.

- **Normal reconstruction:** reuse current passage context and Parent TAU; label cognitive demand only as needed; update the local record / coverage evidence.
- **Difficulty trigger:** run focused diagnosis, choose one evidence-bound remediation, and record only the diagnostic result and return target.
- **TAU exit or actual pathway revision:** run reintegration, update coverage, and make a controlled operational transition only if the real global action changes.

Do not, on every learner turn, rebuild the TAU map, re-evaluate all candidate passages, reload the Literature Matrix, run corpus construction, or synchronize unrelated Markdown mirrors.

## 8. Regression acceptance checks

The patch passes only if the workflow can demonstrate all of the following:

1. broad difficulty signal → diagnosis before decomposition;
2. supported but extractive question → cannot alone complete a Parent TAU;
3. micro-node completion → does not imply Parent-TAU reconstruction;
4. decomposition → retains Parent TAU and reintegration target;
5. repeated unresolved hinge → remediation or explicit bounded deferral;
6. non-blocking textual gap → does not unnecessarily block learning;
7. TAU exit → matches the text’s actual philosophical operation;
8. consolidation → restores local / structural / project context without forced connection;
9. ordinary reconstruction → does not rerun Text Selection;
10. historical completed nodes → remain preserved without fabricated mastery;
11. Mode 1 guided close reading → uses equivalent TAU / exit controls; and
12. QEF-supported but cognitively insufficient question → prompts further appropriate teaching rather than automatic success.
