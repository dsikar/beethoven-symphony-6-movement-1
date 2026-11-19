# Issue #2: dynamics and expressive-marking audit

Audited 19 November 2026 from clean main `cd94652`, after the user-authorized merges of rehearsal PR #9 and sound-assignment PR #11. Work branch: `feature/2-missing-dynamics`. Scope is movement I only, all 512 notated bars and 15 orchestral staves. Bar numbers do not expand the exposition repeat.

## References and method

Compared the canonical score's native Dynamic objects (including custom text embedded in dynamics), Expression and playing-technique objects, and dynamic spanners with the supplied orchestral scan. Movement I occupies full-score PDF pages **5–27**, printed folios **3–25**; PDF page 28 begins movement II and was excluded. Coverage was bars 1–85 (PDF 5–8), 86–174 (9–12), 175–257 (13–16), 258–350 (17–20), 351–440 (21–24), and 441–512 (25–27).

Also checked the horn scans, PDF pages **1–2** for Horn I and **6–7** for Horn II, stopping before “Szene am Bach”. Their D=151 “cresc. poco a poco” instructions corroborate the horn additions below. Neither a different movement nor an older adapted score supplied any marking.

The reference combines paired winds and horns on shared staves. Separate-player activity and voice placement were checked in the canonical score before assigning a marking. Matching a nearby staff alone was not considered evidence of an omission. Existing differences that are not omissions were retained.

## Confirmed additions

PDF pages below are one-based file pages, not printed folios. A staff/bar qualifier change counts once even when the same instruction appears across a scan's system or page break.

| Bar / position | Instrument(s) | Restoration | Orchestral reference PDF page(s) | Count |
| --- | --- | --- | --- | --- |
| 65, second eighth-note position, first arco attack | Violin II | Native `p`, velocity 40 | 8, upper system beginning 61, fifth bar; printed directly below arco entry | 1 |
| 67, bar start | Viola | Native `p`, velocity 40 | 8, same system, seventh bar; printed below arco entry | 1 |
| 128, bar start | Violins I and II; Violoncello | Restore **sempre** in existing diminuendo: `dimin. sempre` | 10, lower system beginning 120, ninth bar | 3 |
| 147, second eighth-note position, first clarinet attack | Clarinet I | Native Expression `dolce` | 11, lower system beginning 143, fifth bar; Clarinet II is resting | 1 |
| 151, bar start (D) | Clarinets I/II; Bassoons I/II; Horns I/II; Violin I; Viola; Violoncello; Contrabass | Restore **poco a poco** in existing crescendo: `cresc. poco a poco` | 11, lower system, ninth bar; also both horn scans | 10 |
| 155, bar start | Flute I; Violin II | Restore `cresc. poco a poco` | 12, upper system beginning 155 | 2 |
| 163, bar start | Oboe I | Restore `cresc. poco a poco` | 12, upper system, ninth bar; Oboe II is resting | 1 |
| 197, bar start (E) | Clarinets I/II; Bassoons I/II; Violin I; Viola; Violoncello; Contrabass | Restore `cresc. poco a poco` | 13, final bar; wording continues “a poco” at start of PDF 14 | 8 |
| 201, bar start | Oboe I; Violin II | Restore `cresc. poco a poco` | 14, upper system beginning 198, fourth bar; Oboe II is resting | 2 |
| 406, bar start | Violins I/II; Viola; Violoncello; Contrabass | Restore **sempre** in existing diminuendo: `dimin. sempre` | 23, last bar of upper system; “sempre” follows at beginning of lower system | 5 |

**Total: 34 staff/bar changes — two new Dynamic objects, one new Expression, and 31 existing HairPin begin-text additions.**

For the extended crescendos and diminuendos, the existing native spanner subtype, start/end positions, playback parameters, identifiers and segment offsets remain intact. Only `beginText` is supplied to restore the missing qualifier. “Dimin. … sempre” printed across a reference system break is expressed as the complete instruction at the existing diminuendo's start; subsequent system continuation text retains the score's existing style. No new hairpin or invented dynamic level was added.

## Readings retained and user-approved deferral

- **Clarinet II, bars 293–296:** the combined clarinet staff has the swell printed above it (full-score PDF 18, upper system's final bar and beginning of lower system). Clarinet I already has native crescendo 293→295 and diminuendo 295→297. Clarinet II has notes but no corresponding swell. Above-staff placement may address the upper player specifically; it does not establish an unambiguous omission in Clarinet II. On 19 November 2026 the user instructed: “Ok merge and we will leave clarinets for now.” **Clarinet II remains unchanged by explicit user decision.** The source ambiguity is deferred; no copied spanner was introduced. Revisit it only on further instruction.
- Oboes at 97 and bassoons at 98 already contain **p dolce** inside custom Dynamic text; Violin I at 285 already contains **pp stacc.** in the same way. These were not duplicated as Expression objects.
- At 426–427 the combined clarinet staff's **ten.** belongs to the quarter-note line, Clarinet II, where it already exists. Clarinet I has the running line. The following **dolce** at 428 is already on Clarinet I's new melody. No blind duplication between players was made.
- The reference's piano/fortissimo instructions at 376/379 are on the combined **clarinet** staff, where both canonical clarinet parts already contain them; the oboes are resting. Likewise the oboe diminuendo at 402 belongs to active Oboe I; Oboe II is resting.
- Existing dynamic values, per-note velocities, repeated markings and print/playback differences were not standardized. This ticket restores supported omissions rather than imposing a new interpretation. Horn bass-clef pitch/register decisions remain for #4.

## Validation

- MuseScore Studio **4.7.5** successfully opened the edited canonical MSCZ, rendered the complete PDF, and separately saved a temporary native MSCZ. All **34** additions/qualifiers survived that save.
- The two new piano marks attach to the confirmed first arco attacks, after the opening eighth rest in Violin II 65 and at the bar start in Viola 67. Clarinet-I dolce attaches after the opening eighth rest at 147. All existing note durations and velocities remain unchanged.
- Removing exactly the 34 approved additions restores the pre-change notation XML under canonical XML serialization (ignoring formatting-only whitespace), including all existing identifiers. Notes, written spelling, rhythm, articulation, tempo, rehearsal figures, clefs, transpositions, old Horn-II bar 38 edit and explicit layout settings therefore remain unchanged.
- **Every other MSCZ archive payload is byte-identical**, including `audiosettings.json`, automation, style, thumbnail and view settings. All 15 Muse Sounds assignments and the cleared horn solo flags remain intact.
- The refreshed PDF remains **59 A4 pages**. Inspected all eight changed pages: **8, 14, 16, 17, 18, 22, 23, 47**. Added marks and qualifiers are legible and do not collide with notation or clip at the page edges. Long instructions near the end of a system extend into the available margin; no layout settings were changed. All other **51** pages have identical extracted words and bounding coordinates to the rehearsal/Muse Sounds baseline render.
- The upstream original and both reference PDFs retain their full recorded SHA-256 hashes from `SOURCE-PROVENANCE.md`.
- Edited canonical SHA-256: `6e22ef0cb8e5a6aecbaaf7566910a7acc148af7d67e27572da346b017c91d9a8`.

Review PDF: `/tmp/beethoven-m1-dynamics/dynamics.pdf`. Temporary extracted XML, native-save copy, reference details, page images, change manifest and logs are in the same temporary directory and are not committed. No audio/video was exported and no audible playback evaluation was made. The previously documented MuseSampler articulation-range limitation from #10 was not investigated or changed here.

The user accepted the confirmed restorations and authorized merging PR #12, with the clarinet ambiguity deferred as above. Issue #2 can close with this accepted scope. Do not start #3 without further direction.
