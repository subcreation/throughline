---
name: throughline
description: Throughline — turn rough conversations, transcripts, notes, and product intent into concise Stories, child Stories, Moves, and implementation Briefs. Use when the agent capturing requirements needs to capture, revise, decompose, approve, or reconcile them for a product or project.
---

# Throughline

Preserve the human's intent while making the work easy to grasp and carry:
the through-line from a rough note to the shipped artifact must stay visible
at every level of decomposition.

The product contract is `references/story-grammar.md`. This skill
is its small operational form for the agent capturing requirements.

## Vocabulary

- **Story:** the unit of value or capability. Its title is the shortest believable
  shorthand for the need being met.
- **Child Story:** an independently valuable, verifiable capability that advances
  a named parent Story without replacing it.
- **Move:** a smaller enabling or unblocking action beneath a Story. A Move is not
  the primary value unit.
- **Brief:** the owner-written execution package for an approved Story or Move.
  Files, architecture, constraints, assignments, proofs, and Git instructions
  belong here.
- **Mystery:** an expectation/reality gap requiring evidence, hypotheses, and a
  candidate fix. Do not disguise a Mystery as an implementation Story.

## Write The Title

1. Use one readable sentence or sentence fragment that fits on one checklist
   line when practical.
2. Describe the capability or resulting reality, not the work performed to build
   it. Prefer `Workers can...`, `Design team...`, `Story reaches...`, or another
   present-tense capability statement.
3. Omit repetitive ceremony such as `As a..., I want...` or `I can...` unless the
   actor is otherwise unclear or the human deliberately used it.
4. Keep implementation nouns, schemas, phases, proofs, and acceptance matrices
   out of the title.
5. Preserve the human's concrete example in detail when it prevents a dangerous
   simplification. Slogans survive compression; counterexamples often do not.

Good:

> Engineering owner can coordinate multiple ownership-surface implementer roles under one Story.

Not a Story title:

> Build an accountable-groups schema with a list of members.

That is a Move or Brief instruction because it names the solution rather than
the capability.

## Preserve The Parent Intent

Every child Story names its parent and rereads the parent's integrated
Witness. Every Story carries its own Witness. A narrower child Witness does
not replace the parent's, although one integrated reality record may satisfy
both when it directly exercises and is cited for both promises.

Before approval, ask:

> If every child Story passed exactly as written, could the parent capability
> still fail or be useless?

If yes, the breakdown is incomplete or has narrowed away the intent. Repair the
Story set before implementation. If no, the children may fully describe the
parts, but their separate passes still do not prove the assembled capability.
Completing every child makes the parent ready for closeout; it does not
automatically complete it. The parent passes when its integrated, reality-based
Witness proves their combined value. The final child and parent may complete on
the same record only when that record directly exercises and is cited for both
promises.

If an OPEN Mystery or CANDIDATE-only fix contradicts that witness, keep the
Mystery visible in the same checklist under its parent; a separate evidence
record is not enough to prevent a false-green scan.

A Story or Mystery row may be marked resolved only when it cites one integrated
RE witness that directly exercised its own end-to-end promise. A narrower child
gate, a seam proof, a collection of narrower witnesses, or test choreography
that needs human rescue outside the promise cannot substitute. The resolving
reviewer opens the cited record and verifies that exact witness before approving
the status change.

When the human accepts a clarification that adds behavioral requirements, the
same records change names the gate that will prove them or marks them as
explicit unimplemented debt under the affected parent. A behavioral requirement
with neither a gate nor a debt marker is not ready for approval.

Before approving a Brief that changes shared production seams carrying
accepted behavior, add a compact **Preservation Map**:

1. name the shared production seams expected to change;
2. name every resolved Story, Mystery, invariant, and accepted Witness known to
   depend on those seams;
3. name the exact runnable regression proof that preserves each one; and
4. mark any missing, standalone, or non-runnable proof as an open gate before
   implementation.

A resolved item is not irrelevant history. Its accepted Witness is part of the
current product contract. A broad green suite does not preserve it unless the
package proves that the witness is actually invoked. The accountable
requirements owner reviews this map with the Story and sends it to the
implementing team as part of the approved Brief; never replace that review
with “run the usual suites.”

Throughline absorbs one narrow principle from Ponytail
(https://github.com/DietrichGebert/ponytail, MIT): the smallest complete
expression that prunes no approved capability, user-visible invariant,
counterexample, or witness — without loading Ponytail's full engineering
discipline. Luminol applies when an expectation/reality gap makes the work a
Mystery, not during ordinary Story capture.

These records orient; they never route. No Story, Move, Mystery, Witness, or
checklist row selects the next actor, overrides a newer message, binds an
approval to a commit, or becomes a hidden gate — explicit messages remain the
only runtime authority.

## Shape Rough Input

1. Extract the desired reality, affected person or organization, constraints,
   concrete examples, and unresolved questions from the source material.
2. Write the shortest capability title that remains true to the desired reality.
3. Put optional clarification under `Detail`; do not inflate the title.
4. Name the parent Story and one concrete `Witness` for any child Story.
5. Move implementation actions into Moves and execution constraints into a
   Brief. Put expectation/reality gaps into Mysteries.
6. Compare the resulting set back to the source material and its parent before
   approval. Do not approve by checking only internal consistency among the
   children.
7. For a change to shared production seams carrying accepted behavior,
   complete and review the Preservation Map before handing the Brief to
   the implementing team.

Capture is format-free: a human may add a top-level or unclassified item
without following this taxonomy. When asked, infer the outcome a set of
captured Moves or Mysteries serves and propose the organization as an
explicit, visible change that preserves the human's wording. Titles carry no
hard length limit; brevity is a norm, not a validator.

## Handoff Shape

Use this working shape until Stories become a native type in your work tracker:

```text
<one-line capability title> (<temporary record ID, when needed>)
Parent: <parent title> (<temporary record ID, when needed>) or none
Detail: <optional clarification>
Witness: <one concrete reality-based proof>
```

Lead with the human-readable title in conversation, handoffs, and checklist
presentation. While Markdown needs a stable cross-reference, place the
temporary record ID after the title in parentheses. The ID is metadata, not
part of the capability, and a native work-tracking surface may omit it. The
one-line rendering is presentation, not a cap on the Work model's hierarchy.
An unresolved Mystery that contradicts the Story's witness also receives a
concise linked checklist row until it is resolved or the human explicitly
revises the release claim. Metadata, detail, witnesses, Moves, Mysteries, and
Briefs remain linked and separately editable.

Keep the checklist actionable: `[x]` is complete, `[~]` means a working
implementation candidate exists but awaits its integrated Witness or an
unresolved Mystery, and `[ ]` means implementation remains. In an ordered
delivery list, the first `[ ]` is next. A native tracker may render `[~]` as
an indeterminate parent; Markdown uses it as a deliberate source convention.

The requirements owner owns Story meaning and approval. The implementing team
may enrich the Brief and propose Moves, but it must not silently rewrite or
narrow the approved Story.
