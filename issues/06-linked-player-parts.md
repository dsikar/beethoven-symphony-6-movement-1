# Prepare linked B-flat trumpet player parts and PDF exports

Status: local draft; no GitHub issue number has been assigned.

## Requested change

Depends on approved trumpet register. Create native linked Trumpet 1 and Trumpet 2 player parts inside the canonical MSCZ, preserving master links. Add useful small silent cues selected from the movement I horn scans and the actual current orchestral score. Historical cue notes in the neighbouring movement-1 folder are leads only; verify every source, rest and entrance. Transpose cues correctly for B♭ trumpet and clearly label any octave displacement. Do not replace played notes with cues.

Provide verified movement I rehearsal figures, correct multimeasure rests and bar numbers, readable stems/beams, dynamics, articulations, spacing and practical page turns. For treble-clef cue passages, accompanying semibreve-shaped full-bar rests should hang from the top F5 line into the E5 space; preserve the full-bar duration. Validate this in the rendered notation, not solely by guessing an XML offset.

Export separate Trumpet 1 and Trumpet 2 PDFs, add only their exact paths to the allowlist, and document cues and validation. Check both native excerpts load, their links resolve, played pitches and spellings match the master, cue notes are silent, and PDFs reflect the saved score. Inspect every PDF page and check page turns. Preserve unrelated orchestral notation, playback settings and source provenance.

## Workflow and validation

Read `AGENTS.md` and `SOURCE-PROVENANCE.md`. Work only in this movement I repository, editing `source/Beethoven_Op.68_1.mscz` after this draft has been published as a GitHub feature-request issue. Use `feature/<actual-issue-number>-<short-description>`, reference the issue in commits and a PR, and report actual affected bars/instruments and checks performed. Keep `originals/` and `references/` immutable. Preserve unrelated edits and files. Open the PR for review; do not merge without the user's instruction.
