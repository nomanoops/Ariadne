# Research State, Handoff and Reconciliation

This reference owns the durable learning record for the exploration. It is written in
plain Markdown; no canonical JSON, transition engine or validator ships with the core.
Where the text says "record", it means a learner-visible Markdown record, not a
simulated state transition.

## 1. What the record contains

Update `research-state.md` after each substantive learning round:

- Current phase
- Current horizon
- Known knowns
- Known unknowns
- Unknown knowns
- Newly discovered unknown unknowns
- Map status
- Primary text reading status
- Secondary literature status
- Surprise / Horizon Shift Log
- Candidate Problems
- Next Actions

Never change without explicit learner confirmation:

- Active Research Question
- 核心 Thesis
- 重大研究方向变化

Learner-level detail (what was read, what was reconstructed, what failed, which hint was
used, which bridge is still open) belongs in `learning-state.md`. The research record holds
orientation, not a transcript.

## 2. Session handoff

A session boundary never by itself closes, resets or re-diagnoses an Exploration phase.
At a pause or handoff, preserve only the learner-specific context needed to resume without
fabrication or repetition:

- **Most recent substantive user reconstruction** and its evidence / calibration status;
- **pending calibration / residual gap**;
- **current unresolved learning need**, including any live hinge or deferred-context trigger;
- **next concrete learning action**, with support-fading level, last hint / answer mode,
  harvest disposition and do-not-repeat items when applicable.

Mode 0 records this detail first in `learning-state.md`; `research-state.md` is used only
when high-level research context is actually implicated.

## 3. Historical learning-state reconciliation

When an audit finds a conflict among session evidence, learner records, Scope Cards,
Markdown mirrors and the written plan, stop new reading and reconcile before advancing.
First submit a node-by-node evidence table and a minimal repair plan for learner review; do
not write project records until the learner approves the plan.

1. Classify each Passage Package separately as `CONFIRMED`, `PENDING_CALIBRATION`,
   `AGENT_INSPECTED_ONLY` or `UNKNOWN`. Require a learner reconstruction plus confirmed
   calibration for `CONFIRMED`; a Scope Card, an agent text inspection, a completed
   selection action or an agent summary alone never establishes learner completion.
2. Keep three layers distinct: epistemic status (what the learner reconstructed and
   confirmed), operational status (the actual next action and node), and planning evidence
   (Scope Card selection and agent-side inspection). A consistent-looking mirror does not
   settle the other two layers.
3. Recover the smallest available primary evidence before proposing a repair: user
   reconstruction, calibration exchange, explicit exit evidence, then durable learner
   records. Preserve the original evidence and state the uncertainty when only partial
   evidence survives.
4. Never backfill historical completion by inventing a completed node or receipt. Record
   recovered history as reconciliation evidence instead. If the record cannot faithfully
   encode a pending historical node, retain that limitation explicitly rather than
   manufacturing a completed one.
5. Repair Markdown mirrors and Scope Cards only where the exact field is demonstrably stale
   or internally inconsistent. Do not overwrite a field merely because its name sounds
   learner-facing; first determine its record role. Preserve historical timestamps and raw
   reconstructions, and label superseded current-state lines rather than rewriting history.
6. After approved repairs, independently compare the written plan, the current Markdown
   mirrors, the Scope Card window fields and the reconciliation ledger. Agreement is
   structural; it does not prove that learner evidence, calibration or historical coverage
   is complete.
7. Reassess Card Harvest only after reconciliation: separate confirmed-but-unharvested
   understanding, existing candidates, pending-calibration material, and material that
   remains too open to harvest. Do not create, revise, commit or promote cards as part of
   reconciliation unless the learner separately authorizes that action.

## 4. Field-level checks before resuming

For each package named in the plan, confirm:

| Field | Check |
|---|---|
| Package window | exact start / end sentences, not only a page number |
| Reading mode | `PRIMARY_FIRST`, `GUIDE_ORIENTED_ENTRY` or `COMMENTARY_ASSISTED`, with reason |
| Learner reconstruction | present, in the learner's words, with calibration status |
| Required bridges | each bridge identified, entered, and not replaced by an agent summary |
| Open hinges | recorded as open; not silently converted into conclusions |
| Deferred context | item plus a concrete trigger |
| Next action | one concrete action, not a phase name |

If a field cannot be checked, write `UNVERIFIED` with the reason. Do not fill it by
inference from a summary.

## 5. Resume gate

After approved reconciliation or ordinary session resumption:

1. Re-read the written plan, the last learner reconstruction and the open hinges.
2. Confirm that the next action follows from the recorded evidence and does not repeat an
   established diagnosis.
3. Confirm that no canonical-sounding claim ("package complete", "thesis adopted") is being
   made in the records when the learner evidence does not support it.
4. Resume from the recorded next action; ask the learner only about a material internal
   conflict that the records cannot resolve.

A note, a completed reading, or an agent inspection is not learner completion. The record
must keep that distinction visible across sessions.
