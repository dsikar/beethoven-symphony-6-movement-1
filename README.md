# Beethoven Symphony No. 6 — Movement I

Create B♭ trumpet parts for the first movement of Beethoven's Symphony No. 6, Op. 68, for an orchestra without horns. Follow the issue-driven workflow established for [movement II](https://github.com/dsikar/beethoven-symphony-6-movement-2), while deriving all musical decisions from movement I.

The movement is **Erwachen heiterer Gefühle bei der Ankunft auf dem Lande — Allegro ma non troppo**.

## Files

| File | Purpose |
| --- | --- |
| [`source/Beethoven_Op.68_1.mscz`](source/Beethoven_Op.68_1.mscz) | Canonical working orchestral score, copied unchanged from the previously saved local movement I source. |
| [`originals/Beethoven_Op.68_1.mscz`](originals/Beethoven_Op.68_1.mscz) | Verified upstream original; immutable comparison material. |
| [`references/Beethoven_6_Score.pdf`](references/Beethoven_6_Score.pdf) | Supplied full-symphony orchestral score; immutable. |
| [`references/Beethoven_6_Hrns.pdf`](references/Beethoven_6_Hrns.pdf) | Supplied full-symphony horn parts; immutable. |
| [`SOURCE-PROVENANCE.md`](SOURCE-PROVENANCE.md) | Exact source revision, hashes and starting-state caveats. |
| [`NEXT-SESSION.md`](NEXT-SESSION.md) | Ordered tickets and handoff instructions. |

The working score has 512 bars and 15 orchestral staves, including two horns encoded in F. It has no new trumpet staves or rehearsal-mark objects at repository creation. Existing local edits have been retained; the working score is not byte-identical to the upstream original. Audit that difference in the first ticket. Do not infer sounding pitch from a playback patch name or copy movement II's horn transposition.

Movement I occupies Horn I PDF page 1 and the top of page 2, and Horn II page 6 and the top of page 7, ending before “Szene am Bach”. Verify rehearsal positions directly from the supplied scans. The older local cue notes identify ambiguous rehearsal letters; their mappings are leads to check, not an approved answer key.

Open the canonical score in MuseScore Studio 4. Inspect its existing sound assignments and available libraries before playback; sound libraries are not part of this repository. Preserve the current tempo and other settings unless the active issue explicitly changes them.

## Work sequence

Audit the starting score and rehearsal figures, check missing dynamics, remove red analytical annotations, create exact-sounding-pitch B♭ trumpet staves, adapt register using documented octave changes, prepare linked player parts and PDFs with silent cues, remove redundant “a. 2” instructions, then export the final orchestral MP3 with trumpets audible and horns muted. Each step has a separate local issue draft; consult `NEXT-SESSION.md` for publication status, links and dependencies. GitHub publication is pending explicit approval to upload the score/reference files.

The neighboring `../movement-1/` folder contains historical drafts, cue notes and video work. It is preserved outside this repository. Its `source/Beethoven_Op.68_1_with_trumpets_1_2.mscz` and autosave are separate older adaptations; they have not been imported or endorsed as the new canonical score. Inspect older drafts read-only when useful, and carry no musical decisions across without checking them against current sources.

## Tracking changes

Read `AGENTS.md`. Work on `feature/<issue-number>-<short-description>`, reference the issue in commits and open a PR that explains actual affected bars and instruments, musical changes and validation. Preserve unrelated edits and compare the relevant passages in MuseScore. Each requested PDF, MP3 or documentation deliverable needs an explicit allowlist entry when introduced. Open PRs for review; merge only on the user's instruction.

## Sources and attribution

The upstream original is from [OpenScore Orchestra / Hauptstimme, movement I](https://github.com/MarkGotham/Hauptstimme/tree/8f677853c45b74ca0afcd79677e5379c06c82354/data/Beethoven%2C_Ludwig_van/Symphony_No.6%2C_Op.68/1), pinned to commit `8f677853c45b74ca0afcd79677e5379c06c82354`, Git blob `e88baca00a808c2bc79397123b0da836bfd7dc9e`. Embedded metadata identifies **IMSLP #516705**. Retain embedded attribution: **Score: CC0 1.0 Universal; Annotations: CC-By-SA**. These notices do not assign a licence to the separately supplied reference scans.

The reference PDFs were copied byte-for-byte from the movement II repository's immutable references, originally supplied from the local ELLSO/2026_Autumn collection. Full input hashes are recorded in `SOURCE-PROVENANCE.md`.
