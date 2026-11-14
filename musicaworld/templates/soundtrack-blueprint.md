# Soundtrack Blueprint — <TRACK TITLE>

> Cue spec for film/TV/trailer/documentary. Follow `references/
> cinematic-composition.md` cue workflow. Every timestamp must map to
> a real narrative event — no floating music.

## 1. Cue Identity

| Field | Value |
|---|---|
| **Cue # / Title** | |
| **Project / scene reference** | (e.g. "Act II, scene 7 — the reveal") |
| **Duration** | mm:ss.s – mm:ss.s (total :ss) |
| **Timecode source** | (film TC / temp cut / beat map) |
| **Format** | stereo / 5.1 / Atmos stem spec |
| **Loudness target** | (−23 to −27 LUFS cinematic; state value) |
| **Source vs. score** | non-diegetic / diegetic / hybrid (specify transition point) |

## 2. Narrative Context

- **What happened before this cue**: (prior scene state — reader must
  know the emotional before-state)
- **What happens during**: (action beats, in order)
- **What changes by the end**: (the narrative delta this cue must carry)
- **Character POV**: (whose interiority does the audience occupy?)

## 3. Emotional Intention & Arc

- **One-sentence intention**: (e.g. "dread with reluctant hope")
- **Intensity arc** (1–10): t=00 → t=mid → climax → end:
- **Opening state → turn → climax → resolved state**: (the emotional
  trajectory in words, then mapped to intensity numbers)

## 4. Theme & Motif Spec

### Main motif

```
Notes (scale degrees + octave): e.g. 5 – 4 – 2 – 1 (descending sigh)
Rhythm:   (note values; where it breathes)
Instrument color: (first statement: e.g. solo cello, sul tasto)
Register: (e.g. C4–G4)
Transformations:
  - heroic: (e.g. major 3rd lift, octave up, full strings)
  - threat: (e.g. minor 2nd cluster, low brass, slowed ×1.5)
  - memory: (e.g. music-box register, reversed tail)
```

### Secondary motifs (if any)

- (character motif / location motif / threat motif — 2–5 notes each,
  intervallically distinct from main motif)

### Motif usage map

| Timecode | Motif | Form (statement/development/inversion/fragment) | Why here |
|---|---|---|---|
| | | | |

## 5. Musical Core

| Field | Value |
|---|---|
| **Tempo map** | (e.g. 60bpm rubato opening → 92bpm ostinato at t=1:04; mark every change) |
| **Meter** | |
| **Key centers** | (per section; modulations marked with pivot chords) |
| **Harmonic rhythm** | (chord changes per bar minimum — write actual chords) |

```
Section / bars | Chords | Function
Opening        | Dm – Bb – F – C | i–VI–III–VII, modal, unresolved
Build          | Dm – Dm – Eb – Dm | phrygian bII = threat color
Climax         | Bb – Eb – F – Gm | borrowed iv, plagal lift
Resolution     | Dm – A – Dm | deceptive, withheld tonic
```

## 6. Instrumentation

**Core palette** (3–6 colors):

| Section | Instruments | Technique | Role |
|---|---|---|---|
| Opening | | (sul ponticello / col legno / prepared) | |
| Build | | | |
| Climax | | | |
| Resolution | | | |

**Hybrid elements** (if any): synth sub, granular texture, field
recording, choir — specify processing.

## 7. Arrangement Timeline (timestamps + hit points)

```
TC          | Section    | Music event                          | HIT POINT?
00:00.0     | pre-roll   | room tone / silence 2–4s              |
00:03.5     | opening    | solo cello states motif              |
00:11.0     | opening    | low drone enters (D2), filtered      |
00:24.0     | build      | ostinato 16ths in strings (Dm)       |
00:41.2     | build      | brass cluster swell — CUT AWAY        | ← hit: abrupt stop
00:41.5     | turn       | single piano note, motif fragment     |
00:58.0     | climax     | full orchestra + choir, motif heroic  | ← hit: cut to black
01:12.4     | resolve    | motif returns solo, unresolved tail   | ← hit: final frame
```

Rules: every cut, reveal, or emotional turn gets a marked hit point;
state whether the hit is **accent** (hit *on* the cut) or **prepare**
(music builds *into* the cut).

## 8. Dynamics & Mix Notes

- **Dynamic curve**: pp → ff marks with timestamps (use the timeline).
- **Reverb space**: (hall size, pre-delay; e.g. "large hall, 60ms
  pre-delay, high-pass returns at 250Hz")
- **Low-end strategy**: (what owns 30–80Hz per section; mono sub plan)
- **Mono-compat warnings**: (elements that collapse — check <120Hz)
- **Sting/ending spec**: (button cadence, unresolved tail, or
  deliberate non-resolution — pick one and justify)

## 9. Loop / Edit Requirements (if applicable)

- Loop point: (bar/beat)
- Edit handles: (pre/post roll seconds needed for picture edits)
- Alternate endings: (list)
- Stem requirements: (orchestra / choir / electronics splits)

## 10. Generation / Production Prompt

Cue-specific prompt per `templates/music-generation-prompt.md`, tuned
for instrumental scoring (no vocals unless specified; state "cinematic
underscore, no lyrics" explicitly to avoid sung output).

## 11. Quality Gate (internal, honest)

| Dimension | Pts (max) | Earned | Notes |
|---|---|---|---|
| Originality | 20 | | |
| Musicality | 15 | | |
| Emotional Impact | 15 | | |
| Melodic Identity | 10 | | |
| Arrangement | 10 | | |
| Sound Design | 10 | | |
| Production | 10 | | |
| Memorability | 5 | | |
| Context Fit | 5 | | |
| **TOTAL** | **100** | | |
