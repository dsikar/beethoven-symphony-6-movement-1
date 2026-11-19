# Audit and restore confirmed missing dynamic markings

Status: local draft; no GitHub issue number has been assigned.

## Requested change

After the rehearsal-figure work, inspect the canonical score for missing dynamics and expressive markings, using the movement I reference score and horn parts. Identify the exact bars and instruments before editing and add only omissions supported by those references or the user's specific corrections. Do not infer missing dynamics solely from movement II or blindly duplicate a neighbouring staff.

Record a table of additions, reference locations and any uncertain readings. Preserve notes, rhythms, articulations, tempo, rehearsal figures, transposition and unrelated layout. Validate affected passages in MuseScore, using playback checks where useful. Leave unsupported or ambiguous readings for clarification; if no omissions are found, report that evidence without inventing edits.

## Workflow and validation

Read `AGENTS.md` and `SOURCE-PROVENANCE.md`. Work only in this movement I repository, editing `source/Beethoven_Op.68_1.mscz` after this draft has been published as a GitHub feature-request issue. Use `feature/<actual-issue-number>-<short-description>`, reference the issue in commits and a PR, and report actual affected bars/instruments and checks performed. Keep `originals/` and `references/` immutable. Preserve unrelated edits and files. Open the PR for review; do not merge without the user's instruction.
