# Adapt B-flat trumpet register while preserving both horn chord tones

GitHub issue: [#5](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/5)

## Requested change

Depends on exact-sounding-pitch trumpet staves. Use written F♯3 as the lower playable threshold established in the movement II workflow. Raise coherent phrases by octaves where necessary, including selected Trumpet 1 phrases when that permits Trumpet 2 to remain below it. Preserve both original chord tones; do not import older drafts' unison substitutions or silently replace pitches.

Review phrase boundaries, ties and overlapping sounding durations, not just simultaneous attacks. Aim for a practical upper register, informed by the movement II approach, but establish movement I's actual range and document the proposed solution before editing. If octave changes cannot meet the range/voicing requirements, identify the exact passage and obtain the user's musical decision rather than substitute a chord tone.

Document every adjustment by instrument, bar, position, original/new written pitch and octave movement. Verify that pitches change only by approved octaves, rhythms/markings are unchanged, tie chains agree and there are no unintended voice crossings. Inspect changed passages and audition/check playback in context. Add an explicit allowlist entry for the requested register-change log when created.

## Workflow and validation

Read `AGENTS.md` and `SOURCE-PROVENANCE.md`. Work only in this movement I repository, editing `source/Beethoven_Op.68_1.mscz` under this GitHub feature-request issue. Use `feature/<actual-issue-number>-<short-description>`, reference the issue in commits and a PR, and report actual affected bars/instruments and checks performed. Keep `originals/` and `references/` immutable. Preserve unrelated edits and files. Open the PR for review; do not merge without the user's instruction.
