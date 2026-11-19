# Next session: movement I

Work in `/home/daniel/Documents/music/Beethoven/Symphony-6/beethoven-symphony-6-movement-1`.

## Current status

Public repository: [dsikar/beethoven-symphony-6-movement-1](https://github.com/dsikar/beethoven-symphony-6-movement-1). Publication was explicitly authorized and is complete.

The user authorized merging [PR #9](https://github.com/dsikar/beethoven-symphony-6-movement-1/pull/9) and [PR #11](https://github.com/dsikar/beethoven-symphony-6-movement-1/pull/11). Both are merged into main (`cd94652`); issues #1 and #10 are closed. The score has 512 bars, 15 staves, the verified rehearsal figures and 15 Muse Sounds assignments. Both horn solo flags are cleared for full-orchestra playback.

The user then explicitly instructed work on [issue #2](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/2). Branch `feature/2-missing-dynamics` restores 34 confirmed staff/bar omissions: two piano markings (Violin II 65, Viola 67), Clarinet I dolce at 147, and 31 missing poco a poco/sempre qualifiers. See [`docs/issue-2-dynamics-audit.md`](docs/issue-2-dynamics-audit.md) for every instrument/bar/reference and actual checks. These changes are in [PR #12](https://github.com/dsikar/beethoven-symphony-6-movement-1/pull/12), which the user has now approved for merging. No later musical ticket has started.

On 19 November 2026 the user instructed: “Ok merge and we will leave clarinets for now.” Leave Clarinet II at 293–296 unchanged; the above-staff swell ambiguity is explicitly deferred. PR #12 is authorized for merging and #2 can close on this accepted scope. The next musical ticket is #3; await direction before starting it.

## Validation and preserved state

Issue #2 rendered successfully in MuseScore 4.7.5, and all 34 changes survived a temporary native save. All eight changed PDF pages were inspected; the score remains 59 pages. The other 51 pages have identical extracted text and coordinates. Review PDF: `/tmp/beethoven-m1-dynamics/dynamics.pdf` (temporary, not committed). Every non-notation archive payload, including all audio assignments and automation, remains byte-identical. No audio/video was exported or audible playback check performed.

Read `AGENTS.md`, `README.md` and `SOURCE-PROVENANCE.md`. Preserve the working score's existing differences from upstream; never replace it with upstream or an old adapted draft. The Horn II bar 38 local note edit remains preserved. Keep `originals/` and `references/` immutable; their hashes still match provenance.

Prior audits:

- [`docs/issue-1-baseline-and-rehearsal-audit.md`](docs/issue-1-baseline-and-rehearsal-audit.md): A=53, B=93, C=115, D=151, E=197, F=263, G=312, H=372, I=440, K=476; all historical rehearsal uncertainties resolved.
- [`docs/issue-10-muse-sounds.md`](docs/issue-10-muse-sounds.md): installed Muse Woodwinds, Muse Brass and Muse Strings mapping. All 15 samplers initialized successfully in an application load, which also reported 25 ranged-articulation end errors. Their audible effect remains unassessed; no articulation changes have been made to suppress them.

The horns are encoded in F. Historical bass-clef sounding-pitch interpretation still requires a full passage audit in #4; no pitch/register correction has been made. Do not apply movement II's B-flat basso interpretation or bar numbers.

## Remaining musical tickets

1. [#3: Remove red analytical letter annotations](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/3)
2. [#4: Create B-flat trumpet staves at verified horn sounding pitches](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/4)
3. [#5: Adapt trumpet register while preserving both horn chord tones](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/5)
4. [#6: Prepare linked B-flat trumpet parts and PDFs](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/6)
5. [#7: Remove redundant a. 2 markings](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/7)
6. [#8: Export movement I MP3 with trumpets and no horns](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/8)

Keep each ticket focused, use feature branches and PRs, and await the user's direction before moving to the next musical ticket. Do not edit the historical `../movement-1/` or active `../movement-2/` checkout, import their musical decisions automatically, or launch sub-agents without explicit user instruction.
