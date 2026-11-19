# Create B-flat trumpet staves at the verified horn sounding pitches

GitHub issue: [#4](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/4)

## Requested change

Depends on the score audit and preceding notation cleanup. Add Trumpet 1 and Trumpet 2 in B♭ to the current canonical orchestral score, derived from the corresponding horn lines at their verified original sounding pitches. Preserve rhythm, ties, articulation, dynamics, fermatas, tempo, rests and rehearsal figures. Keep the original horns as reference staves and mute them for substitution playback; keep other orchestral tracks audible and avoid trumpet-only solo states.

Movement I horns are encoded in F (-7 chromatic, -4 diatonic), unlike movement II's B♭ basso horns. Independently establish the sounding interpretation of historical bass-clef notation from the reference engraving and orchestral context before copying pitches. Prior local notes flag bars 147–169, 275–281, 383–389 and 418–422; inspect all clef/transposition changes. A patch named Horn in F is not sufficient evidence.

Verify all copied notes in concert pitch and written B♭ spelling, correct instrument transposition, and preserved markings. Do not adapt low notes yet: document the exact-pitch written ranges and retain this baseline for the register ticket. Assign suitable available trumpet playback sounds, document changes and validate notation and playback in MuseScore.

## Workflow and validation

Read `AGENTS.md` and `SOURCE-PROVENANCE.md`. Work only in this movement I repository, editing `source/Beethoven_Op.68_1.mscz` under this GitHub feature-request issue. Use `feature/<actual-issue-number>-<short-description>`, reference the issue in commits and a PR, and report actual affected bars/instruments and checks performed. Keep `originals/` and `references/` immutable. Preserve unrelated edits and files. Open the PR for review; do not merge without the user's instruction.
