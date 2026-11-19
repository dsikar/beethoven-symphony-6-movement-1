# Next session: movement I

Work in `/home/daniel/Documents/music/Beethoven/Symphony-6/beethoven-symphony-6-movement-1`.

## Publication status

This is a local Git repository. The requested GitHub name is `dsikar/beethoven-symphony-6-movement-1`; a remote has not been created and files have not been uploaded. Automatic approval review rejected both public and private publication because it requires explicit user approval to transfer the local scores/reference files to GitHub. Obtain that authorization, including visibility, before retrying. This handoff is not a substitute for approval. If the user subsequently authorizes publication, create the repository with that visibility, push the prepared commits, publish the eight issue drafts in order and replace the draft links below with actual GitHub issue links. Check for existing remote work before creating duplicates.

## Starting state and scope

Read `AGENTS.md`, `README.md` and `SOURCE-PROVENANCE.md`. Setup copied the saved local working score unchanged and verified the independent upstream original. No musical edits have been made. Preserve the initial working score's existing differences from upstream; audit them before editing. Do not replace it with the upstream file or a historical adapted draft.

The neighbouring `../movement-1/` is the preserved historical workspace; `../movement-2/` is a different active repository where DeepSeek is handling cue-rest placement. Do not modify either. Movement II's workflow is useful, but its B♭ basso transposition, cue notes, bar numbers and rehearsal map are not applicable to movement I.

## Planned tickets

1. [Audit the starting score and establish movement I rehearsal figures](issues/01-audit-and-rehearsal-figures.md)
2. [Audit and restore confirmed missing dynamic markings](issues/02-missing-dynamics.md)
3. [Remove red analytical letter annotations from the orchestral score](issues/03-remove-red-annotations.md)
4. [Create B-flat trumpet staves at the verified horn sounding pitches](issues/04-create-bb-trumpet-staves.md)
5. [Adapt B-flat trumpet register while preserving both horn chord tones](issues/05-adapt-trumpet-register.md)
6. [Prepare linked B-flat trumpet player parts and PDF exports](issues/06-linked-player-parts.md)
7. [Remove redundant a. 2 markings from the orchestral score and linked parts](issues/07-remove-a2-markings.md)
8. [Export movement I MP3 with trumpets and no horns](issues/08-export-trumpet-mp3.md)

After publication, action only the first ticket: audit the baseline and establish rehearsal figures from the actual references, resolving uncertain letter locations before making unverified edits. Preserve the other tickets for separate branches and review checkpoints. A read-only baseline audit can proceed while publication approval is pending, but score edits must wait for the corresponding GitHub issue as required by AGENTS.md.

The former movement I drafts contain uncertain rehearsal mappings and earlier register substitutions. Do not treat them as approved decisions. The movement I source horns are encoded in F; verify historical bass-clef interpretation against printed parts and harmony. Do not change tempo, export audio/video, import old trumpet parts or start additional workers during the first ticket.

When the first ticket is validated, commit and open a PR describing actual bar/instrument changes and checks. Do not merge without the user's instruction. Report the PR and remaining uncertainties.
