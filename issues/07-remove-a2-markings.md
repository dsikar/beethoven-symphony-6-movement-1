# Remove redundant a. 2 markings from the orchestral score and linked parts

Status: local draft; no GitHub issue number has been assigned.

## Requested change

After linked-part preparation, inspect the whole movement for redundant staff-text instructions whose visible text is “a. 2” / “a 2” and equivalent typographic variants. Record affected bars/instruments and remove that instruction throughout the current orchestral score and the corresponding linked excerpts. Do not remove unrelated musical instructions or occurrences of the number 2.

Refresh affected trumpet PDFs and validate them against the saved linked parts. Compare every other score element and playback setting against the pre-edit snapshot; confirm links remain intact, cues remain silent, page turns remain practical and the reference files are unchanged. Keep this focused on text removal; do not add other cleanup or audio export.

## Workflow and validation

Read `AGENTS.md` and `SOURCE-PROVENANCE.md`. Work only in this movement I repository, editing `source/Beethoven_Op.68_1.mscz` after this draft has been published as a GitHub feature-request issue. Use `feature/<actual-issue-number>-<short-description>`, reference the issue in commits and a PR, and report actual affected bars/instruments and checks performed. Keep `originals/` and `references/` immutable. Preserve unrelated edits and files. Open the PR for review; do not merge without the user's instruction.
