# Source provenance and starting state

Repository initialized on 19 November 2026. No musical edits were made during setup.

The working score is copied unchanged from the existing local `../movement-1/source/Beethoven_Op.68_1.mscz`. Its SHA-256 differs from upstream; preserve it and audit the differences in the first issue. The initial working file and upstream original each contain 512 bars, 15 instrument parts, two horns encoded in F (-7 chromatic / -4 diatonic), no rehearsal-mark objects, and 185 lyric objects. Classify lyrics and colours before removing annotations; these counts do not prove all lyrics are unwanted.

The upstream original was downloaded from commit `8f677853c45b74ca0afcd79677e5379c06c82354` of `MarkGotham/Hauptstimme`, path `data/Beethoven,_Ludwig_van/Symphony_No.6,_Op.68/1/Beethoven_Op.68_1.mscz`. Its Git blob was independently computed and matched `e88baca00a808c2bc79397123b0da836bfd7dc9e`.

Historical local notes discuss an old-notation bass-clef interpretation in bars 147–169, 275–281, 383–389 and 418–422. Treat that as a hypothesis to verify against the actual engraving and harmony, not a preapproved octave correction. Older rehearsal notes also flag differing B locations and an uncertain G; resolve them from the references rather than transferring movement II letters.

## Initial files and SHA-256

| File | SHA-256 |
| --- | --- |
| `source/Beethoven_Op.68_1.mscz` | `722451bc0845e9390389f5ffbc73f83901506342d84c080a6af4ac1637c35bf3` |
| `originals/Beethoven_Op.68_1.mscz` | `c5fd6b92a920e703ab11510a71d0801894023879515c5fecb8f254839b8359a5` |
| `references/Beethoven_6_Score.pdf` | `dc34bb71ad96782369287e367712f6f6224e32825b1dbbbf1e053c173a225146` |
| `references/Beethoven_6_Hrns.pdf` | `ba311085907247af99a576db729fd57858a9ade0ac860f1e345e1f31ec76264c` |

Preserve the full embedded provenance and licence notices. The local working baseline, old adapted scores and autosaves in the historical folder were not overwritten. No local video, audio export, backup or historical draft is part of this initial repository.
