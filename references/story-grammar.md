# Story Grammar

Date: 2026-07-22
Status: canonical Story grammar for requirements work; a Markdown stand-in
until Stories become native records in a work tracker

This grammar carries two kinds of authority, and this document keeps them
distinct. The Story/Move/Release/Brief vocabulary and the title discipline are
**recovered from an earlier planning grammar**. Parent links, Witnesses, and
Mystery-as-record are **a later synthesis**, adopted while building Current, an
open-source multi-agent harness (coming soon) (see "Provenance" below). The
operational form used by the agent capturing requirements is the Throughline
skill, [`SKILL.md`](../SKILL.md).

## The model

- **Story:** the unit of value or capability. Its title is the shortest
  believable shorthand for the need being met.
- **Parent Story:** a high-level capability whose purpose must remain visible
  while lower-level work proceeds.
- **Child Story:** an independently valuable and verifiable capability that
  advances a named parent without replacing it.
- **Move:** a smaller enabling or unblocking action beneath a Story.
- **Brief:** the accountable owner's execution package for an approved Story or
  Move. Architecture, files, constraints, assignments, proofs, and Git
  instructions belong here.
- **Mystery:** an expectation/reality gap requiring evidence, hypotheses,
  falsifiers, and a candidate fix. A Mystery is not an implementation Story.
- **Release:** a coherent usable or shippable grouping of Stories.

## The title

A Story title:

1. Fits on one readable checklist line when practical.
2. Describes the capability or resulting reality, not the work performed to
   build it.
3. Uses present-tense capability language and only names an actor when the actor
   matters.
4. Omits `As a`, `I want`, and `I can` ceremony unless those words add meaning.
5. Keeps schemas, phases, proofs, file names, and implementation choices out.
6. Leaves optional context in Detail rather than padding the title.

Canonical example:

> Engineering owner can coordinate multiple ownership-surface implementer
> roles under one story

Not a Story title:

> Build an accountable-groups schema with a list of members

That is a Move or Brief instruction because it names the implementation rather
than the capability.

## Parent and child truth

Every child Story records its parent, and the rule below applies at every
parent/child link. A child Story may itself be a parent; whether hierarchy
depth should be limited remains an open product question under evaluation.
Before approving a breakdown, the requirements owner asks:

> If every child passed exactly as written, could the parent capability still
> fail or be useless?

If yes, the Story set has narrowed away the intent and must be repaired before
implementation starts. If no, the children may fully describe the parts, but their
separate passes still do not prove the assembled capability. Completing every
child makes the parent ready for closeout; it does not automatically complete
it. The parent passes when its integrated, reality-based witness proves their
combined value. The final child and parent may complete on the same record only
when that record directly exercises and is cited for both promises.

An OPEN Mystery or CANDIDATE-only fix that contradicts that witness stays
visible in the same checklist beneath the affected Story. Its investigation
and evidence remain separate linked records, but hiding it outside the
checklist would allow a false-green scan. The Story cannot be checked until the
Mystery is resolved or the human explicitly revises the claimed capability.

The parent witness should exercise the combined value, not merely count green
children. For a multi-agent organization, the witness is not "the groups proof
passes." It is one engineering owner coordinating overlapping server and
Apple-client work under one Story without replacing either implementer, losing
track of the work's reviewer, or making the human relay either handoff.

## From rough material to approved work

The agent capturing requirements turns notes, transcripts, and conversations
into work in this order:

1. Recover the desired reality, affected person or organization, constraints,
   concrete examples, and unresolved questions.
2. Find or write the parent Story before decomposing it.
3. Write the shortest title that remains true to the desired reality.
4. Put clarification in Detail and one reality-based proof in Witness.
5. Split independently valuable outcomes into child Stories.
6. Put enabling actions into Moves and execution instructions into a Brief.
7. Put expectation/reality gaps into Mysteries.
8. Compare the complete set back to the source conversation and parent witness,
   not only to itself.

Working record:

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
one-line, scan-friendly rendering is presentation, not a Work-model constraint:
the Work model supports parent/child nesting (depth limits under evaluation),
and Parent, Detail, Witness, Moves, Briefs, and Mysteries remain linked,
separately editable records. A linked unresolved Mystery that contradicts the
Story's witness also receives its own concise checklist row until resolved.

### Checklist progress

The checklist is an ordered work surface, not a confidence ledger. Its left
edge must reveal completed work and the next implementation focus at a glance:

- `[x]` means the Work is complete.
- `[~]` means a working implementation candidate exists, but the Work is
  waiting for its integrated witness or an unresolved Mystery.
- `[ ]` means no working implementation candidate exists; implementation work
  remains, and the first such row in an ordered delivery list is next.

`[~]` is the Markdown stand-in for a native indeterminate checkbox, not a
third completion claim. Parent progress is derived from its children, but
completing them does not automatically check the parent: the parent's own
integrated Witness still must pass. One record may close the final child and
parent together only when it directly exercises and is cited for both promises.
An unresolved Mystery is an unchecked child beneath the affected Story, so a
built Story can remain visibly indeterminate without becoming indistinguishable
from untouched work.

## Ownership and safeguards

The requirements owner owns Story meaning and approval. The implementing team
may enrich a Brief and propose Moves, but it may not silently rewrite or narrow
the approved Story.

**Work records are never runtime authority.** A Story, Move, Mystery, Witness,
or checklist row never selects the next actor, never overrides a newer
message, never binds an approval to a commit, and never becomes a hidden gate.
Product checkpoints remain valid as explicitly configured approval gates;
explicit messages remain the only runtime authority.

Throughline absorbs one narrow principle from
[Ponytail](https://github.com/DietrichGebert/ponytail) (MIT) for requirements
work: the smallest complete expression that prunes no approved capability,
user-visible invariant, counterexample, or witness. Requirements work does not
load Ponytail's full engineering discipline. Luminol applies only after an
expectation/reality gap makes the work a Mystery.

## Product direction: Work hierarchy

The current product direction for native Work records:

- Work supports parent/child hierarchy directionally; whether depth should be
  limited remains under evaluation, deliberately undecided.
- A user may capture top-level or unclassified items without following this
  taxonomy; capture stays format-free and lighter than notes-app friction.
- AI-authored or AI-organized work normally expresses Stories as outcomes,
  with child Stories, Moves, and Mysteries beneath them.
- When asked, AI may infer the outcome a set of captured Moves and Mysteries
  serves and propose or perform the organization — as an explicit, visible
  change that preserves the human's captured wording, never as hidden state.
- Brevity is rewarded, but titles never carry a hard length limit; nothing
  validates, refuses, or truncates on length.

What this direction does NOT yet decide: native schema and fields, id scheme,
depth or rendering mechanics, auto-organization triggers, or whether
unclassified captures are Stories or a pre-Story inbox type. Those remain
deliberately open.

## Provenance

**Recovered from the earlier planning grammar** (verified against its primary
sources):

- The title is the shortest believable shorthand; detail stays outside the
  title; the Story is the unit of value; a Release is the grouping layer above
  Stories.
- Shorthand capture and the enriched Story are separate; Moves enable Stories;
  Briefs package approved work.
- Concise capability titles, like the canonical example above, were the
  intended checklist rows.

**Later synthesis** (adopted while building Current, not part of the earlier
grammar):

- Parent links and Witnesses come from a requirements-preservation ritual
  adopted after a requirements-recovery postmortem, because the earlier grammar
  had no defense against children silently narrowing a parent.
- Mystery as a first-class record comes from Luminol practice; the earlier
  grammar treated Mystery as a Story *mode*.
- The earlier grammar explicitly kept hierarchy off the user surface ("no
  user-facing hierarchy"; a flat, reminders-list shape). That principle is
  superseded by the Work-hierarchy product direction above — parent/child Work
  is now the product direction and may be user-visible, while depth limits
  remain under evaluation; the supersession is recorded here rather than left
  silent.
