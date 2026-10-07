# Contributing To Throughline

Throughline should change only when a source packet or real work record proves
that its current grammar loses meaning, creates ambiguity, or loads irrelevant
guidance.

## Useful Contributions

- A source packet with an adjudicated inventory of intended meaning.
- A reproduced case where a parent promise narrowed during decomposition.
- A domain corpus that tests the current software-specific vocabulary.
- A reader-comprehension protocol or scoring correction.
- A drift check that preserves the exact skill and Story Grammar relationship.
- Clearer documentation that does not change the frozen behavior contract.

## Before Opening A Pull Request

1. Start from the intended integration base on a feature branch.
2. Keep unrelated work out of the branch.
3. State the lost meaning, comprehension gap, or domain mismatch being
   addressed.
4. Include the smallest source packet and reality-based Witness that would fail
   before the change and pass after it, when behavior changes.
5. Show that no approved requirement, counterexample, uncertainty, or authority
   boundary was removed.
6. Run `git diff --check` and inspect the full base-to-head commit and path
   range.
7. Push the exact head and open a draft pull request.

Changes to `SKILL.md` or Story Grammar require a compatibility decision and
independent review. Do not turn Throughline into a workflow engine, router,
proof discipline, Git procedure, or blanket command for shorter prose.

By submitting a contribution, you agree that it may be licensed under this
repository's Apache License 2.0.
