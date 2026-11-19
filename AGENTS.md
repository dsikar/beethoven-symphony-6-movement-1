# Score-editing workflow

This repository adapts Beethoven Symphony No. 6, movement I, for an orchestra without horns by creating B♭ trumpet parts.

- Track every subsequent score edit with a GitHub feature-request issue before editing. If the user requests an edit in conversation, create the issue from that request rather than asking them to repeat it on GitHub.
- Use `feature/<issue-number>-<short-description>` branches. Reference the issue in commits and the pull request. Describe actual affected bars, instruments, musical or engraving changes and validation.
- Edit `source/Beethoven_Op.68_1.mscz` as the canonical working orchestral score. Preserve unrelated existing edits and make only the requested changes.
- Treat `originals/` and `references/` as immutable. The initial working score differs from upstream; read `SOURCE-PROVENANCE.md` and audit those differences before changing music. Do not replace the working score with upstream or an older adapted draft.
- Preserve sounding pitch, written spelling, transposition, tempo, dynamics and layout unless the issue requires changing them. Movement I horns are encoded in F; verify printed transposition and historical bass-clef interpretation against the reference score, horn parts and orchestral harmony. Do not copy movement II's B♭ basso interpretation or bar numbers. Playback patch names do not define staff transposition.
- Prefer octave changes that preserve both horn chord tones when adapting trumpet register; review full phrases, ties and overlapping sounding notes for crossings. Document every adjusted note by bar and position. Do not substitute chord tones without explicit agreement.
- Build native linked player parts from the current canonical score, preserving master links. Cues must be small, silent, correctly transposed and labelled if octave-displaced. In treble-clef cue passages, accompanying full-bar rests should hang from the F5 top line into the E5 space. Preserve their full-bar duration.
- Validate changed passages and relevant parts through MuseScore, with playback checks where appropriate. Inspect refreshed PDFs and confirm unrelated notation and settings are unchanged. Report checks actually performed and any limitations.
- The `.gitignore` is an explicit allowlist. Add each requested deliverable's exact path when it is created. Do not commit backups, autosaves, temporary renders, sound libraries, videos or unrelated drafts.
- Keep feature requests focused and separate. Open PRs with `Closes #<number>` when fully addressed; do not merge without the user's instruction. Do not publish comments or messages outside the authorized issue/PR workflow.
- Do not edit the neighboring movement II checkout; another agent may be working there. Do not start sub-agents or parallel workers unless the user explicitly requests them.
