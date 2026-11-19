# Rule Authority Audits and Minimal Refactors

Use this reference only when the user asks to audit, reconcile, or minimally refactor the learning workflow itself. It does not govern ordinary learner-facing teaching.

## Procedure

1. **Freeze scope and protect state.** Restate the permitted files and whether the task is read-only or allows Skill/reference edits. Unless explicitly authorized, do not modify project state, Scope Cards, learning records, canonical routes, or research commitments.
2. **Read live authorities before judging them.** Inspect the current main Skill, every actually loaded reference named by the task, the workflow controller’s routing rules, and any tests the host project maintains. Any host-maintained static contract tests check packaging, boundaries and text invariants, not teaching behaviour; no tests are bundled in this release. Run available tests against the candidate, and never present a string-level pass as behavioural evidence. Treat prior audits as leads, never as the live specification.
3. **Make a rollback manifest before edits.** Copy each candidate file to one timestamped backup directory and record its SHA-256. Include tests (where they exist) and cross-skill controller files when they may change.
4. **Map authority clause-by-clause.** For each material rule, identify its owner, trigger, mandatory wording, dependencies, and type: `CORE`, `GUARDRAIL`, `HEURISTIC`, or `REDUNDANT/CONFLICTING`. Diagnose whether a procedural rule has become a universal gate without a learning-goal, text, or learner justification.
5. **Consolidate rather than merely delete.** Give a detailed operational procedure one authoritative reference. In the main dispatcher retain only: applicability, non-negotiable invariant, and pointer. Preserve the underlying failure prevention while removing duplicated criteria.
6. **Separate three kinds of source use.** Distinguish Agent-side consultation, learner-facing supplemental reading, and a pathway revision. Agent consultation alone does not create a reading assignment, rerun text selection, or change canonical routing. A real route change still uses the existing controlled transition.
7. **Treat pedagogical strategies as defeasible.** Keep source authenticity, provenance, learner-evidence, and state-integrity rules as guardrails. Make sequencing, guide use, decomposition, background, and orientation conditional on their actual pedagogical value; do not convert the replacement coordination rule into a new approval chain.
8. **Test behavior, not only strings.** First add or revise small contract tests that express the intended authority boundary. Replace obsolete literal-string tests with semantic assertions only after confirming the live rule already preserves the intended meaning. Then run realistic learner-facing replays and label them separately from actual outcomes.
9. **Check sources when a replay invokes them.** For primary-text or guide claims, inspect the real accessible source window. If a PDF needs extraction, use an available local parser such as `pypdf` and report the inspected pages and evidential limit. Do not treat project review notes as a substitute for source inspection.
10. **Verify closure.** Run whatever suite and routing/link checks the host project provides; compare changed files to the backup; report character/hot-path impact; verify project-state files were not written. Label evidence as `STATIC RULE PASS`, `SIMULATED BEHAVIOR PASS`, `SOURCE-CHECK EXECUTED`, or `ACTUAL LEARNER OUTCOME UNTESTED`.

## Pitfalls

- Read the current file before patching it; prior reports and line numbers drift after refactors and can move the wrong authority.
- Preserve the invariant while relocating detail; otherwise a deletion can silently remove the safeguard against treating Agent explanation, local completion, or prompted recognition as independent understanding.
- Do not force every source consultation through learner-reading gates; doing so turns ordinary sense-making into administrative routing and suppresses useful bounded explanation.
- Do not let a verified dependency auto-reroute the learner; dependency evidence establishes a reason to judge revision, not that revision is always proportionate.
- Do not make Work Orientation a default pre-course; its independent activity must answer a foreseeable entry risk, while direct verified primary entry remains legitimate when the local question is sufficiently situated.
- Do not call a replay an outcome; simulated compliance tests a policy’s decision shape, whereas learning requires subsequent learner evidence.
