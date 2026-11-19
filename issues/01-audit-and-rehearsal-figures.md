# Audit the starting score and establish movement I rehearsal figures

GitHub issue: [#1](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/1)

## Requested change

Audit the preserved working score against the immutable upstream original before musical edits. Explain and retain existing local changes unless a separately authorized correction requires otherwise. Establish the movement I rehearsal figures from the supplied full score and horn scans, then add/correct the agreed figures in the canonical working score.

Scope: all 512 bars and relevant instrumental staves. Both input scores currently have no rehearsal-mark objects. Historical local cue notes suggest A at 53, differing B locations at 87/93, C at 113, D at 151, E at 197, F at 262, H at 372, I at 440 and K at 474; G was unresolved. These are leads to verify, not approved placements. Resolve discrepancies against the actual sources and ask the user about any genuine editorial ambiguity. Do not import movement II's A–H scheme or guess G.

Record a concise baseline audit, confirmed letter/bar mapping and unresolved questions. Use the verified map to make only the requested rehearsal edits; retain all notes, dynamics, transpositions, tempo, other text and layout except unavoidable local spacing. Render and inspect the changed pages in MuseScore. Validate against the scans and confirm the original/reference hashes are unchanged.

## Workflow and validation

Read `AGENTS.md` and `SOURCE-PROVENANCE.md`. Work only in this movement I repository, editing `source/Beethoven_Op.68_1.mscz` under this GitHub feature-request issue. Use `feature/<actual-issue-number>-<short-description>`, reference the issue in commits and a PR, and report actual affected bars/instruments and checks performed. Keep `originals/` and `references/` immutable. Preserve unrelated edits and files. Open the PR for review; do not merge without the user's instruction.
