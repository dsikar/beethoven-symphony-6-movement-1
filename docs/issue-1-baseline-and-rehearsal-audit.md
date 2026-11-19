# Issue #1: baseline audit and rehearsal figures

Audited 19 November 2026 against main commit `5f731de`. This audit concerns movement I only. Bar numbers count the 512 notated bars once, without expanding the exposition repeat.

## Preserved baseline

The starting working archive matches the SHA-256 in `SOURCE-PROVENANCE.md` (`722451bc…35bf3`). It was retained, not replaced by upstream. All 15 staves have 512 measures; there are no trumpet staves or existing rehearsal-mark objects.

Comparison of every measure on every staff, excluding internal `eid` identifiers, finds one musical difference from the immutable upstream:

| Instrument / bar | Upstream | Preserved working score |
| --- | --- | --- |
| Horn II, 38 | Quarter rest, then two staccato eighth-note sounding C4s | Sounding A4 eighth, G4 sixteenth, F4 sixteenth, slurred together, then the same two staccato C4 eighths. Written E5–D5–C5, then G4–G4, for horn in F. |

The baseline therefore has three additional notes, one fewer rest and one additional slur: 12,203 notes, 4,587 rests and 1,637 Slur elements. This audit records the pre-existing change without approving, correcting or reverting it. New beam, articulation and element identifiers in this bar are retained too.

Other differences from upstream:

- Save metadata changes from MuseScore 4.7.3 / `cf9860c` to 4.7.5 / `3654226`.
- Slur `eid` values exchange positions in 120 other measures across staves 1–10. The identifier multisets in those measures agree, and the XML agrees after excluding identifiers; durations, endpoints, notes and engraving properties agree.
- `audiosettings.json` reorders tracks and sets both horn tracks (part IDs 9 and 10) to solo. Comparing tracks by `(partId, instrumentId)` finds no other track setting differences. Other audio settings agree. The thumbnail differs.
- Style, automation, view settings and container XML agree byte-for-byte.

All of these baseline differences remain. The 185 Lyrics objects, their inherited analytical colours, all other text, note spellings, dynamics, slurs, ties, clefs, instrument transpositions, layout properties and the encoded tempo of 2.2 quarter notes/second remain untouched. Annotation removal and dynamic restoration belong to later issues.

## Verified rehearsal map

The supplied full-score scan prints each letter above the upper staff and again above Violin I. Both horn scans corroborate the same positions. PDF page numbers below are one-based file pages; printed full-score folios are two lower. Horn I uses PDF pages 1–2 and Horn II pages 6–7, before “Szene am Bach”.

| Figure | Bar | Full-score PDF page (printed folio) | Counting anchor in full score | Horn I / Horn II PDF page |
| --- | --- | --- | --- | --- |
| A | 53 | 7 (5) | Lower system begins 49; fifth bar | 1 / 6 |
| B | 93 | 9 (7) | Upper system begins 86; eighth bar | 1 / 6 |
| C | 115 | 10 (8) | Upper system begins 109; seventh bar | 1 / 6 |
| D | 151 | 11 (9) | Lower system begins 143; ninth bar | 1 / 6 |
| E | 197 | 13 (11) | Lower system begins 186; twelfth bar | 1 / 6 |
| F | 263 | 17 (15) | Upper system begins 258; sixth bar | 1 / 6 |
| G | 312 | 19 (17) | Upper system begins 304; ninth bar, tutti ff entry | 1 / 6 |
| H | 372 | 21 (19) | Lower system begins 364; ninth bar | 2 / 7 |
| I | 440 | 24 (22) | Lower system begins 430; eleventh bar | 2 / 7 |
| K | 476 | 26 (24) | Lower system begins 474; third bar | 2 / 7 |

The horn parts additionally label the starts of systems at A (53), B (93, Horn II), D (151) and H (372). Their C falls after bars 111–114; G follows the crescendo leading to the tutti; K follows the half-note entry at 474 and quarter-note bar 475. These musical patterns also agree with the full score and canonical score.

The earlier B=87 lead describes the start of the horn crescendo, not rehearsal B. C=113, F=262 and K=474 are also superseded by direct counting above. G is legible and resolved at 312. The sources use I then K, with no intervening J. No rehearsal-placement ambiguity remains; no editorial choice or movement II mapping was needed.

Ten native `RehearsalMark` objects were added at the beginning of these bars in voice 1 of the top staff (Flute 1), providing system rehearsal figures. They render boxed using the preserved score style. Existing system-object placement settings were not changed or supplemented with duplicate staff text. Native linked trumpet parts remain a later ticket.

## Horn transposition observation for later work

The score encodes both horns in F, chromatic -7 / diatonic -4. Both reference parts explicitly begin “in F”. At D (151), the full-score engraving and horn parts show bass-clef C3 and C2 for Horns I and II. The surrounding F pedal and F/B-flat harmony support the historical reading sounding a fourth above those written pitches (F3/F2), rather than a fifth below. The canonical file currently stores F2/F1 (MIDI 41/29). No pitch or clef has been changed in this rehearsal-only issue.

This is a concrete warning for the sounding-pitch audit in #4, not a completed register correction. That ticket must check the complete bass-clef passages (including the previously flagged 147–169, 275–281, 383–389 and 418–422), clef transitions, ties and harmonic context before creating trumpets. Movement II's B-flat basso interpretation is inapplicable.

## Validation and limits

- MuseScore Studio **4.7.5**, offscreen CLI, opened the baseline and edited canonical MSCZ and exported complete PDFs successfully, without score-loading errors. Both PDFs have **59 A4 pages**.
- Visually inspected all ten affected rendered pages: **6, 10, 13, 17, 22, 31, 36, 43, 51, 55**. The boxed figures align with the confirmed bar starts, are legible and do not collide with notes, slurs or bar numbers. Existing red analyses remain visible.
- PDF text and bounding-coordinate comparison finds changes only on those ten pages; the other 49 pages have identical extracted words and coordinates. No explicit layout settings changed.
- A separate MuseScore save to a temporary MSCZ retained all ten native rehearsal objects at the same bars. The canonical archive retains the minimal edit, avoiding unrelated save normalization.
- Removing the ten new objects from the edited XML yields the baseline XML exactly under XML serialization, including all existing identifiers. Every other canonical archive payload is byte-identical to the working baseline, including mixer settings and thumbnail. Notes, rests, lyrics, tempo and transpositions are consequently unchanged.
- SHA-256 of all three immutable inputs still equals `SOURCE-PROVENANCE.md`: upstream `c5fd6b92…59a5`, full score `dc34bb71…5146`, horns `ba311085…264c`.
- Edited canonical SHA-256: `020ce2fe70a7815a32941841028b4225d1312fd2efd30dae0e71bcf543b4c9ad`.

Temporary PDFs, page images, extracted XML and MuseScore logs are in `/tmp/beethoven-m1-audit/` on the editing machine and are not committed. No interactive GUI audition or playback validation was performed; rehearsal labels do not alter sound. No audio/video or player parts were exported. Full musical correction, historical-pitch/register validation and part layout are outside #1. No unresolved question blocks the rehearsal map.
