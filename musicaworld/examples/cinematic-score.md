# Cinematic Cue — "The Door Was Open"

> Complete worked specimen: cue spec for a fictional scene —
> "the lighthouse keeper finds the door open at dawn."
> Follows `references/cinematic-composition.md` cue workflow.

## 1. Cue Identity

| Field | Value |
|---|---|
| **Cue # / Title** | Cue 14 — "The Door Was Open" |
| **Project / scene reference** | *The Salt Meridian* — Act I, Scene 4: keeper Elias discovers the lighthouse door ajar at dawn, finds footprints in the salt, and hears something moving below. |
| **Duration** | 02:14.0 – 03:31.5 (77.5s) |
| **Timecode source** | Temp cut v3, 24fps |
| **Format** | Stereo (5.1 stem spec optional) |
| **Loudness target** | −24 LUFS integrated (cinematic, dialogue headroom) |
| **Source vs. score** | Non-diegetic score with diegetic source element (foghorn at t=1:48) |

## 2. Narrative Context

- **Before**: Elias has kept the light for 11 years. The lighthouse is his world; the mainland is a rumor. He is alone, routine-bound, quietly content.
- **During**: At dawn, he finds the door open — impossible, he locks it every night. Footprints in the salt leading *up* the stairs (inland, toward the tower). A sound below — breathing, or water, or something that shouldn't be there. He doesn't call out. He watches.
- **After**: He closes the door. The light still turns. But something has entered the story — and possibly the lighthouse.

## 3. Emotional Intention & Arc

- **One-sentence intention**: "The terror of realizing your sanctuary was never sealed — dread with the first cold finger of curiosity."
- **Intensity arc** (1–10): 2 → 3 → 5 → 7 → 3
- **Opening state → turn → climax → resolved state**:
  - **Opening** (2): routine, ritual, the comfort of isolation
  - **Turn** (5): the door is open — the first crack in the routine
  - **Climax** (7): the sound below — presence confirmed, threat implied
  - **Resolved** (3): he closes the door — but the music doesn't resolve; it withholds

## 4. Theme & Motif Spec

### Main motif — "The Keeper's Litany"

```
Notes (scale degrees + octave): 5 – 4 – 2 – 1 (in D minor)
Rhythm: dotted-quarter, eighth, quarter, half-note (sighing descent)
Instrument color: solo cello, sul tasto (on the fingerboard)
Register: D4–A4
```

**Transformations:**
- **Routine** (opening): full statement, cello alone, slow
- **Doubt** (door open): motif fragmented — only notes 5–4–2, the "1" withheld
- **Presence** (sound below): motif inverted to 1–2–4–5, rising, in low strings + contrabassoon
- **Withheld** (ending): motif returns but stops on note 2 — never resolves to 1

### Secondary motif — "Footprints"

```
Notes: single repeated pitch (A2), rhythm: irregular, like steps
Instrument: contrabass pizzicato + low tom
Distinctive: NOT melodic — it's a rhythm that walks
```

Usage: appears only when footprints are seen/heard. Always in low register. Always irregular — never a steady pulse.

### Motif usage map

| Timecode | Motif | Form | Why here |
|---|---|---|---|
| 02:14.0 | Litany | statement (full) | routine, comfort |
| 02:38.5 | Litany | fragment (5–4–2) | door open — resolution withheld |
| 03:04.0 | Footprints | first appearance | footprints seen in salt |
| 03:18.0 | Litany | inversion (1–2–4–5) | sound below — presence |
| 03:28.5 | Litany | fragment (5–4–2, stops) | door closes — no resolution |

## 5. Musical Core

| Field | Value |
|---|---|
| **Tempo map** | 60bpm rubato opening → 72bpm steady pulse at t=2:38 → ritardando at t=3:28 |
| **Meter** | 4/4 (opening in free time, no strict pulse) |
| **Key centers** | D minor throughout; brief D harmonic minor at climax |
| **Harmonic rhythm** | one chord per 2 bars opening → one per bar in build |

```
Section        | Chords                    | Function
Opening        | Dm – Bb – F – C           | i–VI–III–VII, modal, unresolved
Door open      | Dm – Eb – Dm – C          | i–bII–i–bVII, phrygian bII = wrongness
Build          | Dm – Dm – Eb – Dm         | i–i–bII–i, tritone-adjacent tension
Climax         | Bb – Eb – F – Gm          | borrowed iv, plagal lift into dread
Resolution     | Dm – A – Dm               | i–V–i, deceptive, withheld tonic
```

## 6. Instrumentation

**Core palette**: solo cello, string orchestra (divisi), contrabassoon, low brass (muted), prepared piano, sub drone.

| Section | Instruments | Technique | Role |
|---|---|---|---|
| Opening | solo cello | sul tasto, vibrato | motif statement |
| Opening | contrabass | sustained D2 | sub drone, felt not heard |
| Door open | cello + contrabassoon | fragmented motif, low | doubt enters |
| Build | string divisi | ostinato 8ths on D | pulse emerges |
| Climax | full strings + low brass | cluster + motif inversion | presence |
| Resolution | solo cello + prepared piano | motif fragment, stops on 2 | withheld |

**Hybrid elements**: sub drone is synthesized (sine 36Hz + filtered noise bed); prepared piano uses a felt-muted string for the "footprints" motif.

## 7. Arrangement Timeline

```
TC          | Section      | Music event                              | HIT POINT?
02:14.0     | pre-roll     | silence 3s, room tone (wind, foghorn distant) | ← cut in on silence
02:17.0     | opening      | solo cello states Litany (full, slow)    |
02:31.0     | opening      | contrabass D2 drone enters, filtered      |
02:38.5     | door open    | Litany fragments to 5–4–2, stops          | ← hit: door creaks, music cuts to drone only
02:52.0     | door open    | prepared piano enters, single notes       |
03:04.0     | footprints   | contrabass pizz + low tom — irregular     | ← hit: footprints visible in salt
03:18.0     | climax       | Litany inverts, strings + brass swell     | ← hit: sound below, music swells then CUTS
03:28.5     | resolution   | solo cello returns, motif stops on 2      | ← hit: door closes, final frame
03:31.5     | end          | drone fades, no cadence                    |
```

**Hit point rules applied**: all hits are **prepare** type (music builds into the cut) except t=3:18 which is **accent** (sudden cut to silence as the door closes).

## 8. Dynamics & Mix Notes

- **Dynamic curve**:
  - Opening: pp (cello alone, barely above room tone)
  - Door open: mp (drone + fragments, intimate)
  - Footprints: mf (rhythm enters, still restrained)
  - Climax: ff (full orchestra, but only 4 bars — then silence)
  - Resolution: pp (cello alone again, unresolved)

- **Reverb space**: large hall (3.5s decay), 80ms pre-delay; high-pass returns at 300Hz.
- **Low-end strategy**: contrabass owns 30–60Hz throughout; sub drone at 36Hz is mono-sum; nothing else below 80Hz.
- **Mono-compat warnings**: string divisi cluster at climax must be checked in mono — spread high strings wide, keep low strings center.
- **Sting/ending spec**: no cadence. The cue ends on the Litany's note 2 (the "4" of the descent) — the resolution to "1" is deliberately withheld. The audience doesn't get relief.

## 9. Loop / Edit Requirements

- **Loop point**: not applicable (one-shot cue)
- **Edit handles**: 2s pre-roll (silence), 3s post-roll (drone fade)
- **Alternate endings**:
  - **End A** (used): withheld — motif stops on 2, no cadence
  - **End B** (alternate): motif completes to 1, but on a low cello harmonic — ambiguous resolution
  - **End C** (trailer version): motif inverts fully, ends on tritone — unresolved dread

## 10. Generation / Production Prompt

```
[CONCEPT]
A cinematic underscore for the moment a lighthouse keeper discovers
his sanctuary was never sealed. Dread with the first cold finger of
curiosity — not jump-scare horror, but the slow realization that
something has been inside all along.

[GENRE / HYBRID]
Cinematic underscore × chamber strings × prepared piano × sub drone

[EMOTION]
Dread with reluctant curiosity — isolation violated, sanctuary breached

[TEMPO / METER / KEY]
60–72 BPM rubato → steady pulse, 4/4, D minor throughout

[INSTRUMENTATION]
Solo cello (sul tasto), string orchestra divisi, contrabassoon,
muted low brass, prepared piano (felt-muted), contrabass pizzicato,
sub drone (36Hz sine + filtered noise)

[VOCALS]
None — instrumental underscore

[MEL/HARMONIC DIRECTION]
Main motif: descending 5–4–2–1 in D minor, sighing dotted rhythm.
Verses on i–VI–III–VII, door-open section uses phrygian bII,
climax borrows iv, ending withholds tonic resolution.

[GROOVE]
Free rubato opening → steady pulse → ritardando ending. No percussion
drum kit — only contrabass pizzicato as irregular "footsteps."

[ARRANGEMENT]
Solo cello → drone → fragmented motif → ostinato build → climax
cluster → sudden cut → solo cello fragment, unresolved

[PRODUCTION AESTHETIC]
Large hall reverb (3.5s), high-pass returns at 300Hz, mono-safe
low end, prepared piano for texture, no electronic beats

[DYNAMICS / TEXTURE]
pp opening → mf build → ff climax (4 bars only) → pp resolution.
Sub drone felt not heard. Tape saturation on low strings.

[ENDING]
Unresolved — motif stops on note 2, no cadence, drone fades

[NEGATIVE CONSTRAINTS]
No vocals, no lyrics, no drums, no electronic beats, no jump-scare
stingers, no major-key resolution, no heroic brass fanfare
```

## 11. Quality Gate

| Dimension | Pts (max) | Earned | Notes |
|---|---|---|---|
| Originality | 20 | 17 | Litany motif is a known device (descending sigh) but execution is specific; footprints-as-rhythm is a fresh touch |
| Musicality | 15 | 14 | Progressions coherent, phrygian bII motivated, withheld resolution is earned |
| Emotional Impact | 15 | 14 | Arc is convincing — routine → violation → presence → withheld relief |
| Melodic Identity | 10 | 8 | Litany is memorable but the "footprints" motif is rhythmic, not melodic — intentional but limits hummability |
| Arrangement | 10 | 9 | Clear structure, purposeful layer entries, hit points all earned |
| Sound Design | 10 | 9 | Prepared piano, sub drone, contrabass pizz — all specified and motivated |
| Production | 10 | 9 | Loudness target, reverb spec, mono-compat warnings, edit handles all present |
| Memorability | 5 | 4 | Litany is recognizable; footprints rhythm is distinctive but not hummable |
| Context Fit | 5 | 5 | Perfect for the scene — dread without jump-scare, curiosity without relief |
| **TOTAL** | **100** | **89** | **High** |

**Weakest dimensions**: Melodic Identity (8/10) and Memorability (4/5).
The score is intentionally non-hummable — the Litany is memorable
but the overall cue prioritizes texture over tune. For a trailer
version, the motif would need a more singable contour.
