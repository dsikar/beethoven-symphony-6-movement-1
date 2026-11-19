# Next session: movement I

Work in `/home/daniel/Documents/music/Beethoven/Symphony-6/beethoven-symphony-6-movement-1`.

## Repository status

Published publicly with the user's explicit authorization on 19 November 2026: [dsikar/beethoven-symphony-6-movement-1](https://github.com/dsikar/beethoven-symphony-6-movement-1). The score, upstream original and reference PDFs are uploaded; the eight feature-request issues below are open. No further publication approval is pending for this setup.

## Starting state and scope

Read `AGENTS.md`, `README.md` and `SOURCE-PROVENANCE.md`. Setup copied the saved local working score unchanged and verified the independent upstream original. No musical edits have been made. Preserve the initial working score's existing differences from upstream; audit them before editing. Do not replace it with the upstream file or a historical adapted draft.

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

Action only [issue #1](https://github.com/dsikar/beethoven-symphony-6-movement-1/issues/1): audit the baseline and establish rehearsal figures from the actual references, resolving uncertain letter locations before making unverified edits. Preserve the other tickets for separate branches and review checkpoints. Issue #1 already tracks this work; use its feature branch and preserve the other issues as separate checkpoints.

The former movement I drafts contain uncertain rehearsal mappings and earlier register substitutions. Do not treat them as approved decisions. The movement I source horns are encoded in F; verify historical bass-clef interpretation against printed parts and harmony. Do not change tempo, export audio/video, import old trumpet parts or start additional workers during the first ticket.

When the first ticket is validated, commit and open a PR describing actual bar/instrument changes and checks. Do not merge without the user's instruction. Report the PR and remaining uncertainties.
