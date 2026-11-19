# Remove red analytical letter annotations from the orchestral score

GitHub issue: [#3](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/3)

## Requested change

Inspect all 512 bars for the red analytical a/b/c/d annotations inherited from OpenScore. Classify actual text/lyric objects and inherited stylesheet colours before removing them. The starting files each contain 185 lyric objects, but that count is not an answer key and does not authorize deleting every lyric or red object.

Remove only the unwanted analytical letter annotations. Preserve musical text, dynamics, rehearsal figures, all notes, transposition and embedded source/licence metadata. Report exact object count and affected bars/instruments. Compare structured score contents before/after, render affected pages in MuseScore and confirm unrelated content and reference material are unchanged.

## Workflow and validation

Read `AGENTS.md` and `SOURCE-PROVENANCE.md`. Work only in this movement I repository, editing `source/Beethoven_Op.68_1.mscz` under this GitHub feature-request issue. Use `feature/<actual-issue-number>-<short-description>`, reference the issue in commits and a PR, and report actual affected bars/instruments and checks performed. Keep `originals/` and `references/` immutable. Preserve unrelated edits and files. Open the PR for review; do not merge without the user's instruction.
