# Export movement I MP3 with trumpets and no horns

GitHub issue: [#8](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/8)

## Requested change

Depends on completed notation/register/part corrections and the user's final review. Export the complete movement I orchestral adaptation to MP3, with both B♭ trumpet staves audible and both retained horn staves muted. All other intended orchestral instruments must remain audible; clear any trumpet-only solo state. Cues remain silent.

Preserve the final pitches, register, tempo, dynamics and articulation. Verify movement I's repeat structure against the agreed score and document how the export handles repeats rather than silently changing them. Check that the opening is intact and the final note/reverb tail completes; review duration, instrumentation, clipping and playback. Record MuseScore version, sound profile, MP3 settings and checks. Add the final MP3's exact path to the explicit allowlist. Do not export a video, commit sound libraries or include temporary audio files.

## Workflow and validation

Read `AGENTS.md` and `SOURCE-PROVENANCE.md`. Work only in this movement I repository, editing `source/Beethoven_Op.68_1.mscz` under this GitHub feature-request issue. Use `feature/<actual-issue-number>-<short-description>`, reference the issue in commits and a PR, and report actual affected bars/instruments and checks performed. Keep `originals/` and `references/` immutable. Preserve unrelated edits and files. Open the PR for review; do not merge without the user's instruction.
