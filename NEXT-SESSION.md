# Next session: movement I

Work in `/home/daniel/Documents/music/Beethoven/Symphony-6/beethoven-symphony-6-movement-1`.

## Repository status

Published publicly with the user's explicit authorization on 19 November 2026: [dsikar/beethoven-symphony-6-movement-1](https://github.com/dsikar/beethoven-symphony-6-movement-1). The score, upstream original and reference PDFs are uploaded; the eight feature-request issues below are open. No further publication approval is pending for this setup.

## Starting state and scope

Issue #1 has now been implemented on `feature/1-audit-rehearsal-figures` in [PR #9](https://github.com/dsikar/beethoven-symphony-6-movement-1/pull/9), pending review; do not merge or start #2 without the user's instruction. See [`docs/issue-1-baseline-and-rehearsal-audit.md`](docs/issue-1-baseline-and-rehearsal-audit.md) for the baseline comparison, scan evidence and actual validation. The verified rehearsal map is A=53, B=93, C=115, D=151, E=197, F=263, G=312, H=372, I=440, K=476. Native system marks were added without other score changes. The original Horn II bar 38 local edit and both horns' solo settings remain preserved. All immutable hashes still match. MuseScore 4.7.5 PDF rendering, inspection of all ten affected pages and a temporary native-save round trip passed. Historical horn bass-clef pitch audit remains work for #4; no pitch correction was made here.

Read `AGENTS.md`, `README.md` and `SOURCE-PROVENANCE.md`. Setup copied the saved local working score unchanged and verified the independent upstream original. No musical edits were made during setup; the rehearsal additions above were made subsequently for #1. Preserve the initial working score's existing differences from upstream; audit them before editing. Do not replace it with the upstream file or a historical adapted draft.

The neighbouring `../movement-1/` is the preserved historical workspace; `../movement-2/` is a different active repository where DeepSeek is handling cue-rest placement. Do not modify either. Movement II's workflow is useful, but its B♭ basso transposition, cue notes, bar numbers and rehearsal map are not applicable to movement I.

## Open tickets

1. [Audit the starting score and establish movement I rehearsal figures](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/1)
2. [Audit and restore confirmed missing dynamic markings](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/2)
3. [Remove red analytical letter annotations from the orchestral score](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/3)
4. [Create B-flat trumpet staves at the verified horn sounding pitches](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/4)
5. [Adapt B-flat trumpet register while preserving both horn chord tones](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/5)
6. [Prepare linked B-flat trumpet player parts and PDF exports](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/6)
7. [Remove redundant a. 2 markings from the orchestral score and linked parts](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/7)
8. [Export movement I MP3 with trumpets and no horns](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/8)

The initial instruction was to action only [issue #1](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/1): audit the baseline and establish rehearsal figures from the actual references, resolving uncertain letter locations before making unverified edits. Preserve the other tickets for separate branches and review checkpoints. Issue #1 already tracks this work; use its feature branch and preserve the other issues as separate checkpoints.

The former movement I drafts contain uncertain rehearsal mappings and earlier register substitutions. Do not treat them as approved decisions. The movement I source horns are encoded in F; verify historical bass-clef interpretation against printed parts and harmony. Do not change tempo, export audio/video, import old trumpet parts or start additional workers during the first ticket.

PR #9 records the validated first ticket. It remains open and unmerged; issue #1 will close only when the PR is merged. No rehearsal-map ambiguity remains. Await the user's review and instruction before merging or beginning #2.
