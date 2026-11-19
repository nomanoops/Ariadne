# Distributed Conceptual Grounding Protocol

## Scope and boundary

Use this protocol only after existing **Difficulty Diagnosis** indicates that a learner’s unresolved difficulty may concern a concept’s distributed primary-text role, a necessary prior definition or argument, multiple textual functions of the same term, or an external conceptual context. It applies to Mode 0, Mode 1, and Mode 2 whenever a Guided Primary Text Close Reading has such a hinge.

It strengthens existing Hinge Analysis, Primary Text Selection, Guide Introduction Decision, Specialist Secondary Reading, Question–Evidence Fit (QEF), Bridge Load, and Decomposition–Reintegration. It creates no canonical action status, no parallel operational state, and no automatic change to any project state file.

Do **not** run it because a word is merely unfamiliar, appears technical, or has a likely source discipline. First ask whether the exact current window is sufficient for the local learning task. If it is, use ordinary local parsing, concept-function clarification, or Hinge Analysis instead.

## 1. Trigger and bounded check

Trigger a **Distributed Conceptual Grounding Check** only when one or more of these conditions has evidence:

```text
CURRENT WINDOW LACKS A NECESSARY CONCEPTUAL DETERMINATION
A RELATED USE MAY BE DISTRIBUTED ELSEWHERE IN THE SAME WORK
THE CURRENT MOVE MAY DEPEND ON ANOTHER CHAPTER’S ARGUMENT
A SOURCE DISCIPLINE / THEORY MAY MATTER TO THE LOCAL FUNCTION
THE SAME TERM’S DIFFERENT USES ARE CAUSING CONFUSION
```

The check begins from the existing Difficulty Diagnosis. State the smallest learning need, for example:

```text
What in the current TAU cannot yet be reconstructed?
Is the missing item a definition, an argument, a comparison, a source-domain distinction, or only a useful background?
What evidence would let the learner return to the current TAU?
```

A recoverable prior diagnosis may be reused only when it identifies the same unresolved learning need and has enough evidence to justify this distributed check. A learner’s report that the difficulty recurs is valid learner evidence, but by itself it neither proves a prior diagnosis nor proves a distributed dependency. In a fresh session without a recoverable applicable diagnosis, first complete the minimum Difficulty Diagnosis required by `references/sense-making-priority.md`, then decide whether this protocol is justified. This does not require two full protocols: once that minimum diagnosis establishes a distributed trigger, continue here without repeating it.

Do not use the protocol to turn every vocabulary question into work-wide research.

## 2. Three search domains

Select only the domain(s) necessary to the current learning need:

| Domain | Question | Default evidence task |
|---|---|---|
| **DOMAIN 1 — LOCAL PRIMARY CONTEXT** | Does the current passage and its necessary adjacent context already answer the need? | Verify exact sentence order, referents, local use, and any necessary neighbouring text. |
| **DOMAIN 2 — DISTRIBUTED PRIMARY CONTEXT** | Does another location in the same work provide a necessary definition, argument, or materially different usage? | Deterministic term/variant search → bounded context verification → dependency judgment. |
| **DOMAIN 3 — EXTERNAL CONCEPTUAL CONTEXT** | Is an authorial reference, source-domain meaning, historical borrowing, or scholarly account needed for the current task? | Verify source relation with reliable primary / historical / scholarly material, then distinguish source meaning from philosophical transformation. |

Do not force all three domains. A result in Domain 1 ends the check unless the remaining ambiguity would change the learner’s reconstruction of the current TAU.

## 3. DOMAIN 2 — distributed primary search

### 3.1 Deterministic candidate retrieval

Use available read-only deterministic tools first: searchable local text, local text indexes, or a bounded PDF text-layer / PDFKit probe. Search a planned family of terms rather than relying on one spelling:

```text
base term
morphological variants
translation variants
source-language / transliteration variants when known
nearby technical variants only when textually motivated
```

For example, an English family such as `form / forming / formation` may require translated, inflected, or edition-specific equivalents. Treat a search as candidate retrieval, not conceptual interpretation. It must produce a compact record of query, edition / translation, text status, candidate locations, and limitations.

Classify every candidate separately:

```text
TERM_MATCH
CONTEXT_VERIFIED
CONCEPTUAL_RELATION_SUPPORTED
DEPENDENCY_CONFIRMED
```

- `TERM_MATCH`: a string or defensible variant was found.
- `CONTEXT_VERIFIED`: the exact local passage was inspected and its use recorded.
- `CONCEPTUAL_RELATION_SUPPORTED`: the inspected passages provide evidence for a stated relation between uses.
- `DEPENDENCY_CONFIRMED`: the other locus is necessary for the current TAU’s limited reconstruction, not merely interesting.

Never promote a bare term match to a conceptual relation or dependency.

### 3.2 Search limitations

Record, where applicable:

```text
OCR / damaged text layer
translation or edition divergence
multilingual terminology
transliteration variation
morphological variation
ambiguous or generic term
incomplete local text availability
```

A null result proves only that the specific search did not retrieve a match under those conditions. It does not prove that the work lacks the concept, use, or dependency.

### 3.3 Usage comparison

For every verified non-local use, compare **functions in context**, not dictionary labels. Use one provisional relation label:

```text
SAME_FUNCTION
EXTENSION
TRANSFORMATION
CONTRAST
POSSIBLE_CONNECTION
UNDETERMINED
```

Every relation receives an independent evidence status:

```text
TEXT_VERIFIED
GUIDE_SUPPORTED
PROVISIONAL
```

Use `UNDETERMINED` when the textual relation has not been established. Preserve disagreement or rival scholarly accounts rather than forcing a work-wide unified definition.

### 3.4 Three outcomes: consultation, learner extension, or pathway revision

After verifying only the smallest relevant contexts, distinguish these actions rather than treating every distributed finding as a new reading assignment:

- `LOCAL_EXPLANATORY_CONSULTATION`: the agent consults adjacent primary text, another locus, a guide, specialist work, or reliable background to improve a bounded explanation of the current TAU. If the learner’s assigned reading does not change, this does not by itself require Selection revision, Bridge Load, a new Passage Package, or a canonical-route change. Label the source boundary and return to the current TAU.
- `LEARNER_READING_EXTENSION`: assign a minimal additional source window only when it has clear value for the learner’s understanding. A selected extension requires precise location, a stated return target, Bridge Load, and Question–Evidence Fit; a shared term or interesting connection is not sufficient.
- `PATHWAY_REVISION`: propose Selection revision when a verified `DEFINITION_DEPENDENCY`, `ARGUMENT_DEPENDENCY`, or comparably material relation may alter the existing pathway. Dependency discovery is a trigger for judgment, not an automatic revision: weigh the learning goal, actual textual relation, learner’s present understanding, available explanatory alternatives, and reading cost. A real change to `global next_action` still uses the existing controlled transition.

### 3.5 Dependency classification and minimal selection

Classify the role of a verified locus as exactly one current default:

```text
DEFINITION_DEPENDENCY
ARGUMENT_DEPENDENCY
COMPARATIVE_RELEVANCE
CONCEPTUAL_TRANSFORMATION
BACKGROUND_ONLY
```

Only `DEFINITION_DEPENDENCY` and `ARGUMENT_DEPENDENCY` presumptively justify considering another primary window. Even then, select it only when the `LEARNER_READING_EXTENSION` or `PATHWAY_REVISION` judgment above supports the cost; otherwise use bounded explanation or defer it. `COMPARATIVE_RELEVANCE`, `CONCEPTUAL_TRANSFORMATION`, and `BACKGROUND_ONLY` may inform an explanation, a later optional reading, or a Concept Map record, but do not automatically become learner work.

If distributed primary reading is selected, use the existing **Primary Text Selection Protocol**: document why this window, why now, why not adjacent alternatives, and what is lost if omitted; then apply Bridge Load and QEF. Do not treat a search hit as a Passage Package.

## 4. DOMAIN 3 — external conceptual grounding

First classify the proposed source relation:

```text
TEXTUALLY_EXPLICIT_REFERENCE
HISTORICALLY_DOCUMENTED_BORROWING
STRUCTURAL_ANALOGY
TERMINOLOGICAL_RESEMBLANCE
ORIGIN_UNCERTAIN
```

Do not infer a direct borrowing from verbal similarity. For any needed external grounding, keep three claims separate:

```text
SOURCE-DOMAIN MEANING
PHILOSOPHICAL TRANSFORMATION
ARGUMENTATIVE FUNCTION IN THE CURRENT TAU
```

- A reliable source may establish a source-domain meaning without establishing the philosopher’s transformed use.
- A primary explicit reference may establish contact without establishing a full genealogy.
- A guide or specialist source may support a documented borrowing or interpretation, but its claim remains guide / specialist evidence rather than direct primary warrant.

Use the Guide Introduction Decision and Specialist Secondary Reading procedures only when considering a learner-facing source action. Bounded `AGENT_SOURCE_CONSULTATION` may inform a labeled explanation without entering a learner guide gate. A source-domain explanation may clarify a local task; it never supplies an unprovided primary-text warrant.

## 5. Choose the minimum grounding depth

Choose the least complex adequate response:

| Depth | Use only when | Output boundary |
|---|---|---|
| `BRIEF_GROUNDING` | A small verified distinction is enough to parse the current use. | Give only the distinction, its evidence status, and its return target. |
| `GUIDED_BACKGROUND_READING` | A bounded reliable external passage is needed but is not another primary dependency. | Exact background source/window → learner reconstruction → explicit limit. |
| `DISTRIBUTED_PRIMARY_READING` | A verified Definition or Argument Dependency needs another locus in the same work. | Minimal Passage Package under existing Selection / Bridge Load / QEF controls. |
| `COMPARATIVE_CONCEPT_RECONSTRUCTION` | The difference between verified uses itself matters philosophically. | Compare roles, evidence, limits, and return to the current TAU. |

Do not select a higher depth merely because more background exists.

## 6. Conceptual Distribution Record

Reuse the existing **Concept Map** and **Text Map**. Add a compact record only when this protocol is triggered; it is research-and-teaching evidence, not a state machine and never selects `global next_action`.

```text
concept:
current_locus:
other_primary_loci:
usage_relation:
dependency_type:
evidence_status:
source_domain_background:
current_learning_need:
return_target:
```

Optional compact search-audit fields, when Domain 2 ran:

```text
search_terms / variants:
retrieval_status: TERM_MATCH / CONTEXT_VERIFIED / CONCEPTUAL_RELATION_SUPPORTED / DEPENDENCY_CONFIRMED
edition / translation:
limitations:
```

A Scope Card or `learning-state.md` may contain only the current learner-facing need, selected minimal source window, evidence boundary, and return target. Keep the fuller conceptual map in `maps/text-map.md` or the existing Concept Map; do not mirror it into canonical state.

## 7. Return to the current Parent TAU

Background or distributed reading is repair work, not completion. Return explicitly to the original Parent TAU and ask whether the learner can now state:

1. the current concept’s function in the exact primary window;
2. what the other primary locus or source-domain material contributes;
3. how that contribution helps, without being substituted for the current text;
4. which connections are textually / guide-supported; and
5. which remain hypotheses, contested interpretations, or unresolved gaps.

Only then resume Parent-TAU consolidation or Exit Reconstruction. Completing a background window does not complete the current TAU, erase a hinge, or promote coverage to `RECONSTRUCTED`.

## 8. Performance and non-spoiling

- Ordinary reconstruction does not scan the entire work, reload every map, or synchronize unrelated state.
- Reuse already verified loci before new retrieval.
- Use deterministic retrieval for candidates and inspect only the bounded contexts that could alter the current learning action.
- Do not ask the primary model to page through an entire work simply to locate terms.
- Do not disclose a work-wide conceptual synthesis to the learner merely because an internal Concept Map exists.
- Record failed or limited searches when they matter, so later sessions do not repeat them as if they had never occurred.

## 9. Regression acceptance checks

The patch passes only if it can demonstrate:

1. a sufficient local window does not trigger distributed search;
2. a necessary missing determination can lead to another same-work locus;
3. `TERM_MATCH` does not itself establish conceptual relation;
4. different functions of one term are not forced into a fixed unified definition;
5. merely comparative loci are not automatically assigned;
6. explicit external reference is separated into source meaning and philosophical transformation;
7. uncertain source relation remains uncertain rather than fabricated;
8. a distributed-primary repair uses the smallest necessary Passage Package;
9. distributed reading returns to the originating Parent TAU; and
10. ordinary reconstruction does not trigger whole-work scans or comprehensive state synchronization.
