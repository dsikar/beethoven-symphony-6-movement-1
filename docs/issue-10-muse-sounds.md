# Issue #10: orchestral Muse Sounds assignments

Requested 19 November 2026 after rehearsal PR #9. Branch `feature/10-orchestral-muse-sounds` starts from that PR's head, `94e086b`, preserving its ten rehearsal figures. This is a separate playback request; musical issues #2–#8 remain untouched.

## Changes

Only `audiosettings.json` inside the canonical `source/Beethoven_Op.68_1.mscz` changes. The active profile is now `MuseSounds`. All 15 orchestral tracks use installed Muse Sounds resources instead of MS Basic:

| Staff / part ID | Library | Sound | Resource ID |
| --- | --- | --- | --- |
| Flute 1 / 1 | Muse Woodwinds | Flute 1 | 118 |
| Flute 2 / 2 | Muse Woodwinds | Flute 2 | 119 |
| Oboes 1, 2 / 3, 4 | Muse Woodwinds | Oboe | 124 |
| B-flat Clarinets 1, 2 / 5, 6 | Muse Woodwinds | Clarinet in Bb | 127 |
| Bassoons 1, 2 / 7, 8 | Muse Woodwinds | Bassoon | 133 |
| F Horns 1, 2 / 9, 10 | Muse Brass | Horn in F (downloaded French Horn) | 108 |
| Violin 1 / 11 | Muse Strings | Violins 1 | 91 |
| Violin 2 / 12 | Muse Strings | Violins 2 | 92 |
| Viola / 13 | Muse Strings | Violas | 93 |
| Violoncello / 14 | Muse Strings | Violoncellos (downloaded Cellos) | 94 |
| Contrabass / 15 | Muse Strings | Contrabasses | 95 |

Wind and horn lines use individual-player sounds; string lines use section sounds. Both pre-existing horn solo flags were cleared so the other orchestral instruments can play. All mute flags, levels, pan, effects, sends and automation remain unchanged. The metronome and chord-symbol support tracks retain MS Basic. No additional instruments were added to use the installed choir, harp, keys, guitars or percussion libraries, which have no corresponding staves here.

The installed library database (`~/Muse Sounds/.instruments`, opened read-only) marks all 11 distinct selected resources installed. Each selected instrument has its `.spx` and `SFZ/*.sts` files. Library binaries and sample data stay outside Git. The score requires these local libraries and MuseSampler for its assigned sounds.

## Validation

- Every canonical archive payload except `audiosettings.json` is byte-identical to the pre-change score. This includes the entire notation XML, style, thumbnail and view settings. All 512 bars, 15 staves, notes, written spelling, dynamics, tempo, ten rehearsal figures, annotations, clefs and transpositions are retained.
- A field-level audio comparison allows only the active profile, the 15 resource metadata blocks and the two horn solo flags to change; all remaining audio settings compare equal.
- MuseScore Studio **4.7.5** opened and saved a temporary copy to native MSCZ. All 15 assigned resource metadata blocks and all track mute/solo states survived that save. The canonical file retains the minimal archive edit rather than unrelated native-save normalization.
- A separate application load of a temporary preview initialized **15 MuseSampler instances successfully**, using MuseSampler **0.106.0** and the ALSA audio engine. This verifies that the instruments resolve beyond merely saving their IDs. The short preview process was stopped after loading; no audio/video was exported and no listening assessment was made.
- That load reported **25 `Unable to add ranged articulation range end` errors**, with messages about a previous ranged articulation ending without its expected end call. The notation was unchanged; the cause and audible effect were not diagnosed. Sound assignment/loading succeeded, but slur/articulation playback is not certified by this check. Do not describe this as an error-free playback test or silently alter articulations to suppress it.
- Refreshed full-score PDF: **59 A4 pages**. Every page has identical extracted words and bounding coordinates to the rehearsal-figure PDF. Page 1 was also visually inspected. Sound selection makes no engraving change.
- The immutable upstream original and both reference PDFs still match the complete SHA-256 values in `SOURCE-PROVENANCE.md`.

Temporary inputs, native-save copy, PDF, image and logs are under `/tmp/beethoven-m1-sounds/`. The application load log is `gui-load.log`; it records both the 15 successful sampler initializations and the articulation errors. These artifacts are not committed. Direct standalone sampler initialization was unsuccessful; validation relies on MuseScore's own successful application load instead. The CLI profile-application experiment reset track assignments, so its temporary output was not used as the canonical score.

Open the canonical score afresh in MuseScore to load the saved assignments. Its Mixer should show Muse Woodwinds, Muse Brass and Muse Strings on the orchestral channels, with no soloed horns. No change was made to the historical movement I workspace or the active movement II checkout.
