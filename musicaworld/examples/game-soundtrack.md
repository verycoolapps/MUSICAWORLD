# Game Soundtrack — "Echoes of the Drowned City"

> Complete worked specimen: musical universe spec for a fictional
> underwater exploration game. Main theme + 4 region/battle tracks
> with motif relationships, stem breakdown, adaptive intensity mapping.
> Follows `references/game-audio.md` universe design.

## Project Overview

| Field | Value |
|---|---|
| **Game** | *Echoes of the Drowned City* — underwater exploration + puzzle-solving in a flooded metropolis |
| **World premise** | A city that sank 100 years ago; the player is a "resonance diver" who can hear the city's memories through its architecture |
| **Musical ambition** | Music that feels like the city is *remembering itself* — every track is a layer of the same memory |
| **Audio format** | Stereo + stems for adaptive mixing (Wwise/FMOD-ready) |

## Music Bible Integration

This score follows a Music Bible (`templates/music-bible.md`) with:
- **Primary mode**: D Dorian (minor with raised 6th — hopeful, watery)
- **Signature rhythm**: 6/8 compound meter (lighthouse-sweep feel)
- **Core palette**: prepared piano, contrabass pizzicato, glass harmonica, sub drone, granular textures
- **Forbidden**: no EDM drums, no orchestral strings (too "epic"), no vocals (the city doesn't sing — it resonates)

## Main Theme — "Resonance"

### Identity

| Field | Value |
|---|---|
| **Title** | "Resonance" |
| **Context** | Main menu + all exploration tracks derive from this |
| **Duration** | 3:24 loop |
| **BPM** | 72 (6/8 feel) |
| **Key/Mode** | D Dorian |
| **Meter** | 6/8 |
| **Motifs** | M1 (main), M2 (memory), M3 (depth) |

### Motif Library

**M1 — Main Theme ("Resonance")**
```
Notes: D4 – F4 – A4 – D5 – A4 – F4 (ascending lift, falling release)
Rhythm: dotted-quarter, eighth, dotted-quarter, quarter, eighth, dotted-quarter
Instrument: prepared piano + glass harmonica doubling
Register: D4–D5
Transformations: minor→major lift (exploration→discovery), half-time (depth tracks), fragmented (danger)
```

**M2 — Memory Motif**
```
Notes: A3 – C4 – E4 – A4 (arpeggiated, music-box register)
Rhythm: steady eighths, like a music box slowing down
Instrument: music box sample + granular processing
Register: A3–A4
Usage: appears when player discovers lore/memories — always sparse, always unresolved
```

**M3 — Depth Motif**
```
Notes: D2 – A2 – D3 (low, slow, descending)
Rhythm: whole notes, no pulse
Instrument: contrabass pizzicato + sub drone
Register: D2–D3
Usage: depth/danger tracks — the further down, the lower the motif
```

### Track Structure (3:24)

| Section | Bars | Energy | Layers |
|---|---|---|---|
| Intro | 4 | 2 | M1 fragment on prepared piano |
| A | 8 | 3 | M1 full statement + contrabass drone |
| B | 8 | 4 | M2 enters (memory layer), glass harmonica |
| A' | 8 | 3 | M1 returns, texture thins |
| C | 8 | 5 | M3 enters, pulse emerges |
| D | 8 | 6 | Full arrangement, all motifs |
| Outro | 4 | 2 | M1 fragment, decay |

### Stem Breakdown (for adaptive mixing)

| Stem | Content | Enters at intensity |
|---|---|---|
| `MUS_Resonance_Drums` | soft pulse (not drums — prepared piano percussion) | 3+ |
| `MUS_Resonance_Bass` | contrabass + sub drone | always |
| `MUS_Resonance_Harmony` | glass harmonica + granular pads | 2+ |
| `MUS_Resonance_Lead` | M1/M2 melodies | 3+ |
| `MUS_Resonance_FX` | bubbles, sonar pings, water movement | context-dependent |

## Region/Track Map

### Track 2 — "The Shallows" (Exploration — Upper City)

| Field | Value |
|---|---|
| **Context** | First area — flooded streets, intact buildings, sunlight through water |
| **Duration** | 4:12 loop |
| **BPM** | 76 |
| **Key/Mode** | D Dorian |
| **Meter** | 6/8 |
| **Motifs** | M1 (main), M2 (memory) |
| **Intensity range** | 2–4 (exploration only, no combat) |

**Arrangement**: M1 in music-box register (M2's instrumentation), sparse; water movement textures; occasional M1 fragments in low register.

### Track 3 — "The Archives" (Puzzle/Story)

| Field | Value |
|---|---|
| **Context** | Library/archive area — lore-heavy, puzzle-solving |
| **Duration** | 3:48 loop |
| **BPM** | 60 |
| **Key/Mode** | B-flat Dorian (tritone shift from D — "wrongness") |
| **Meter** | 6/8 |
| **Motifs** | M2 (memory, primary), M1 (fragmented) |
| **Intensity range** | 1–3 (pure exploration, no threat) |

**Arrangement**: M2 music-box motif dominant; M1 appears only as fragmented echo; heavy granular textures; no pulse — free time.

### Track 4 — "The Drowned Arena" (Battle)

| Field | Value |
|---|---|
| **Context** | Combat area — flooded stadium, structural hazards |
| **Duration** | 2:36 loop |
| **BPM** | 140 (double-time feel from 70bpm half-time) |
| **Key/Mode** | D harmonic minor (raised 7th = danger) |
| **Meter** | 4/4 (shift from 6/8 — "the city fighting back") |
| **Motifs** | M1 (inverted), M3 (depth) |
| **Intensity range** | 4–7 (combat tiers) |

**Arrangement**: M1 inverted (5–4–2–1 becomes 1–2–4–5); M3 in low strings; prepared piano becomes percussive; glass harmonica becomes dissonant clusters.

### Track 5 — "The Core" (Boss/Final Area)

| Field | Value |
|---|---|
| **Context** | The city's heart — the resonance engine, final boss |
| **Duration** | 4:48 loop |
| **BPM** | 120 → 160 (tempo ramp at midpoint) |
| **Key/Mode** | D diminished (octatonic — unstable, dangerous) |
| **Meter** | 7/8 (asymmetric — "the city is off-kilter") |
| **Motifs** | M1 (fully transformed), M3 (dominant), M2 (haunted) |
| **Intensity range** | 6–9 (boss tiers) |

**Arrangement**: M1 transformed beyond recognition — same contour, different intervals; M3 becomes the main pulse; M2 appears as "ghost" — music box slowing down, detuned.

## Adaptive Intensity Mapping

### Vertical Layering (stems)

| Intensity | Drums | Bass | Harmony | Lead | FX |
|---|---|---|---|---|---|
| 1–2 | off | drone only | sparse pads | M1 fragment | water only |
| 3–4 | soft pulse | full | glass harmonica | M1 full | bubbles, sonar |
| 5–6 | driving | full + sub | dissonant | M1 inverted | structural groans |
| 7–8 | aggressive | distorted | clusters | M3 dominant | sonar pings |
| 9 | maximum | maximum | maximum | M1+M3 combined | all FX |

### Horizontal Resequencing

- **Sections**: A (exploration) → B (memory) → C (pulse) → D (climax)
- **Transitions**: bar-matched at 6/8 boundaries; stinger on discovery (M2 fragment)
- **Danger state**: switch to Track 4/5 stems; return to exploration on combat end

### Dynamic Difficulty Mapping

| Game state | Intensity | Layers active |
|---|---|---|
| Exploring | 1–2 | Bass + sparse harmony |
| Puzzles | 2–3 | + lead fragments |
| Combat (normal) | 4–6 | + drums, full harmony |
| Combat (elite) | 7–8 | + FX, dissonance |
| Boss | 8–9 | all layers, tempo ramp |

## Motif Relationships Across Tracks

```
M1 (Resonance) — main theme
  ├── Track 2: music-box register (M2's instrument)
  ├── Track 3: fragmented echo only
  ├── Track 4: inverted (danger)
  └── Track 5: fully transformed (boss)

M2 (Memory) — lore motif
  ├── Track 2: secondary layer
  ├── Track 3: primary (archive = memory)
  └── Track 5: "ghost" — detuned, slowing

M3 (Depth) — danger motif
  ├── Track 2: absent (shallow = safe)
  ├── Track 4: secondary (combat)
  └── Track 5: dominant (core = depth)
```

## Production Standards

| Standard | Value |
|---|---|
| Sample rate | 48kHz (game standard) |
| Bit depth | 24-bit stems |
| Loudness | −16 LUFS (game, leave headroom for SFX) |
| Loop requirements | seamless, bar-matched, 2s intro handle, 4s outro handle |
| Stem naming | `MUS_[Track]_[Layer]_[Version].wav` |
| Export formats | WAV stems + OGG compressed |

## Quality Gate

| Dimension | Pts (max) | Earned | Notes |
|---|---|---|---|
| Originality | 20 | 18 | "City remembering itself" concept is strong; motif relationships are systematic |
| Musicality | 15 | 14 | D Dorian → harmonic minor → diminished progression is motivated; 7/8 for boss is earned |
| Emotional Impact | 15 | 14 | Loneliness → discovery → danger → awe arc is clear |
| Melodic Identity | 10 | 8 | M1 is memorable; M2/M3 are texture-driven, less hummable |
| Arrangement | 10 | 9 | Stem system is well-designed; adaptive mapping is implementable |
| Sound Design | 10 | 9 | Prepared piano, glass harmonica, granular — all specified |
| Production | 10 | 9 | Stems, loops, loudness targets all defined |
| Memorability | 5 | 4 | M1 is recognizable; the "water" feel is distinctive |
| Context Fit | 5 | 5 | Perfect for underwater exploration — the music *feels* submerged |
| **TOTAL** | **100** | **90** | **Exceptional** |
