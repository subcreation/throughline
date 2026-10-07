<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/hero-dark.png">
  <img alt="Illustration of a hand about to write on a blank sticky note at the end of a row of filled notes" src="./assets/hero-light.png">
</picture>

# Throughline

**Your original intent survives every handoff.**

![Format: Agent Skill](https://img.shields.io/badge/format-Agent_Skill-2D5B73)
![License: Apache 2.0](https://img.shields.io/badge/license-Apache--2.0-365B43)

Throughline helps agents turn rough conversations, transcripts, and notes into
capability-led Stories, Moves, Mysteries, Witnesses, and implementation Briefs
without quietly replacing what the person meant.

The recognizable failure is a project that becomes internally consistent while
drifting away from its purpose. Every child task passes, every implementation
step is complete, and yet the assembled result still does not deliver the
original capability or preserve the counterexample that made it matter.

```sh
npx skills add subcreation/throughline -g
```

The Agent Skills installer detects compatible clients and lets the user choose
where to install Throughline. Separate backend-specific commands are not
required.

## Evidence

> **Benchmark in progress.** This panel will compare **supported meaning
> retained per 1,000 tokens, paired with reader comprehension** using the same
> source packet, model, effort, tools, and starting state with and without
> Throughline. Until the fixtures, raw runs, reader protocol, and reproduction
> steps are published, this project claims no efficacy percentage.

The planned corpus, scoring gate, telemetry, and collection status are in
[benchmarks/README.md](./benchmarks/README.md).

## Before And After

Without an intent-preservation discipline:

```text
Request: Workers should carry one customer promise through several teams.
Plan:    Add a schema, a status flag, and three implementation tasks.
Result:  Every task passes, but nobody proves the combined customer promise.
```

With Throughline:

```text
Story:   Workers preserve the customer's promise across team handoffs.
Parent:  The larger customer capability this Story advances.
Detail:  The concrete example and constraints that must not be compressed away.
Witness: One integrated reality check that exercises the assembled promise.
Moves:   Schema, status, and implementation work that enable the Story.
Mystery: Any observed contradiction that keeps the Story visibly indeterminate.
```

## How It Works

1. **Recover the desired reality.** Begin with the person's intended value,
   constraints, examples, uncertainty, and affected recipient.
2. **Name the capability.** Write the shortest title that remains true to that
   reality; move implementation nouns into Moves or a Brief.
3. **Preserve hierarchy.** Every child names its parent and its own Witness.
   Green children do not replace the parent's integrated proof.
4. **Keep different work distinct.** Stories describe value, Moves enable it,
   Briefs package execution, and Mysteries expose expectation/reality gaps.
5. **Carry accepted behavior forward.** A shared-seam Brief maps every accepted
   promise to the proof that must continue to pass.

## Guardrails

- No child breakdown may silently narrow the parent promise.
- No implementation task may masquerade as the user-facing capability.
- No concise rewrite may delete an accepted requirement, counterexample,
  uncertainty, or Witness.
- No unresolved Mystery may hide outside the checklist while its Story appears
  complete.
- No Story, Move, Mystery, or checklist row becomes runtime routing authority.

## Philosophy

Clarity is not fewer words at any cost. Throughline seeks the smallest complete
expression: enough compression to keep the work graspable, with no loss of the
meaning that makes completion valuable. A tidy plan that solves the wrong
problem is not progress.

## Present Boundary

Throughline v0.1 is a software-development specialization. It was developed
while building Current, an open-source multi-agent harness (coming soon), and
its vocabulary assumes a requirements owner, an implementing team, and software
proof practices. That boundary is disclosed rather than silently generalized.

The long-term roadmap tests a smaller shape-general core plus responsibility-
or domain-specific grammars for software, research, design, report writing,
communications, and other real organizations. That generalization is not in
the current skill.

Throughline's full accepted Story Grammar ships at
[references/story-grammar.md](./references/story-grammar.md). Its rules are
the ones used inside Current. This public edition only replaces internal team,
product, and people names, ticket IDs, and internal file references with
generic role language, and moves the grammar to a standalone location.

## Installation

Install globally for every compatible agent the installer detects:

```sh
npx skills add subcreation/throughline -g
```

Omit `-g` to install into the current project instead. To list the skill
without installing it:

```sh
npx skills add subcreation/throughline --list
```

To install from a local clone:

```sh
git clone https://github.com/subcreation/throughline.git
npx skills add ./throughline -g
```

## Update

```sh
npx skills update throughline -g -y
```

For reproducible setups, pin a tagged release instead of following the default
branch, for example:

```sh
npx skills add https://github.com/subcreation/throughline/tree/v0.1.0 -g
```

## Uninstall

```sh
npx skills remove throughline -g -y
```

## Compatibility

Throughline is packaged as a root Agent Skill with optional OpenAI interface
metadata. Before release, the packaging candidate passed an isolated install,
source-tracked update, and uninstall exercise with the Agent Skills installer:

| Agent | Packaging evidence |
| --- | --- |
| Codex | The installer created the Codex copy with the candidate skill and unchanged Story Grammar at their exact hashes. |
| Claude Code | The installer created the Claude Code copy with the same two exact artifacts. |
| Grok Build | Grok's native `inspect` command discovered the installed project copy as the `throughline` skill. |

The update reported the source-tracked candidate current. Uninstall removed both
installed copies (Codex and Claude Code). The public edition's wording changes
came after these checks; the package layout is unchanged. These checks prove
packaging and discovery, not Throughline's efficacy.

Other Agent Skills clients may discover the root `SKILL.md`, but remain
unverified. Host recognition alone does not prove that an agent can preserve a
source packet's meaning or apply the Story Grammar correctly.

## Troubleshooting

**The agent cannot find Story Grammar.** Verify that the installed skill
contains `references/story-grammar.md`. A copy containing only `SKILL.md` is
incomplete.

**The plan is concise but a requirement disappeared.** Restore the source
packet's complete meaning inventory before optimizing length. Compression is
evaluated only after fidelity passes.

**All child Stories pass but the parent still feels unresolved.** Exercise the
parent's integrated Witness. Child completion makes the parent ready for
closeout; it does not prove the combined value automatically.

## Project

- Read the [roadmap](./ROADMAP.md).
- Read the full [Story Grammar](./references/story-grammar.md).
- Inspect or contribute to the [benchmark plan](./benchmarks/README.md).
- Read [CONTRIBUTING.md](./CONTRIBUTING.md) before proposing a behavior change.
- Review the portfolio [art direction](./assets/ART_DIRECTION.md).

Throughline was built alongside Current, an open-source multi-agent harness
(coming soon).

## Credits

Throughline's "smallest complete expression" principle adapts one narrow idea
from [Ponytail](https://github.com/DietrichGebert/ponytail) (MIT License). It
does not bundle or load Ponytail itself.

Throughline is licensed under the [Apache License 2.0](./LICENSE).
