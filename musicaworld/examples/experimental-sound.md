# Experimental Sound — "Pressure Weather"

> Complete worked specimen: experimental piece demonstrating
> drones/granular/microtonal with full process documentation.
> Follows `references/experimental-music.md` — structure and intent
> are mandatory, weirdness needs patience budget.

## 1. Identity

| Field | Value |
|---|---|
| **Title** | *Pressure Weather* |
| **Form** | Fixed-media electroacoustic composition (acousmatic) |
| **Duration** | 12:00 (intended listening: 1–3 sittings) |
| **Premise** | The sound of weather inside a sealed room — pressure changes, temperature gradients, and the creak of a building responding to a storm it can't feel. |

## 2. Source Material

All sounds are synthesized or processed from recordings:

- **Field recordings**: rain on metal roof (contact mic), wind through window frame, distant thunder (high-pass filtered to remove low end)
- **Synthesized**: detuned drone clusters, granular clouds, microtonal sine stacks
- **Found sound**: pencil on paper (contact mic), chair creak, breathing through a tube

## 3. Process Documentation

### Process 1 — "The Room" (0:00–3:00)

```
Source: rain on metal roof (contact mic, 24-bit)
Process: granular resynthesis
  - Grain size: 80–200ms
  - Density: 20 grains/sec → 80 grains/sec (slow build)
  - Pitch: D2 fundamental, scatter ±50 cents
  - Spatial: grains pan randomly in stereo field
  - Filter: bandpass 200–800Hz, slowly widening to 100–2000Hz
Result: rain becomes texture — no longer recognizable as rain,
        but the *pressure* of it remains
```

### Process 2 — "The Building" (3:00–6:00)

```
Source: chair creak + pencil on paper (contact mic)
Process: spectral freezing + time-stretch
  - Spectral freeze: capture creak's resonant frequencies,
    sustain them as drone
  - Time-stretch: 1:8 ratio, preserving pitch
  - Result: creaks become long tones — the building's "voice"
    without the building
```

### Process 3 — "The Pressure" (6:00–9:00)

```
Source: synthesized sine stacks (19-TET microtonal)
Process: beating + slow detune drift
  - 8 sine waves, fundamentals around D2 (73.42Hz)
  - Intervals: just intonation ratios (1:1, 9:8, 5:4, 4:3)
  - Detune: ±3 cents LFO at 0.05Hz (20-second period)
  - Result: slow beating creates "pressure waves" — the listener
    feels the room breathing
```

### Process 4 — "The Release" (9:00–12:00)

```
Source: all previous layers, reversed and re-processed
Process: convolution reverb with generated impulse
  - Impulse: exponential decay 4s, high-pass 100Hz
  - Reversed sources: rain grains, creak drones, sine stacks
  - Result: the room exhales — all textures dissolve into
    a single resonant wash
```

## 4. Structure Map

| Section | Time | Texture | Density | Dynamics |
|---|---|---|---|---|
| I. The Room | 0:00–3:00 | granular rain | low → medium | pp → mp |
| II. The Building | 3:00–6:00 | spectral creaks | medium | mp → mf |
| III. The Pressure | 6:00–9:00 | microtonal drones | high | mf → f |
| IV. The Release | 9:00–12:00 | convolved wash | high → none | f → pp |

## 5. Sonic Characteristics

| Field | Value |
|---|---|
| **Timbre** | granular, spectral, microtonal — "weather made audible" |
| **Spectral envelope** | low-mid dominant (200–800Hz), sparse highs |
| **Amplitude behavior** | slow swells (20s+ periods), no transients |
| **Spatial motion** | grains orbit slowly; drones static; release collapses inward |
| **Morphing trajectory** | rain → creaks → pressure → wash (A→B→C→D) |

## 6. Microtonal Specification

19-TET intervals used in Process 3:

| Just ratio | Hz (D2 base) | Cents vs. 12-TET | Character |
|---|---|---|---|
| 1:1 | 73.42 | 0 | unison |
| 9:8 | 82.60 | +203.9 | whole tone + |
| 5:4 | 91.78 | +386.3 | major third |
| 4:3 | 97.89 | +498.0 | perfect fourth |
| 7:4 | 128.49 | +968.8 | harmonic seventh |

Beating rates: 3–8 Hz between adjacent partials — creates "pressure" without dissonance harshness.

## 7. Listening Instructions

- **Duration**: 12 minutes — designed for sustained attention, not background
- **Volume**: moderate — the piece lives in low-mid frequencies; high volume causes fatigue
- **Environment**: headphones recommended for spatial detail; speakers work but lose grain placement
- **Patience budget**: first 3 minutes establish the room; the piece earns its climax at 6:00

## 8. Quality Gate

| Dimension | Pts (max) | Earned | Notes |
|---|---|---|---|
| Originality | 20 | 18 | Source material choices are fresh; processes are documented and intentional |
| Musicality | 15 | 13 | Structure is clear; microtonal spec is precise; "weather in a room" metaphor is coherent |
| Emotional Impact | 15 | 12 | The arc is subtle — pressure builds then releases; not cathartic, but earned |
| Melodic Identity | 10 | 6 | No melody — intentional; timbre is the identity |
| Arrangement | 10 | 9 | Four processes map cleanly to four sections; transitions are gradual and motivated |
| Sound Design | 10 | 10 | Every process is specified with parameters; spectral/microtonal detail is thorough |
| Production | 10 | 9 | Fixed-media, no mix needed; loudness target −16 LUFS for experimental |
| Memorability | 5 | 4 | The "pressure waves" at 6:00 are distinctive and memorable |
| Context Fit | 5 | 5 | Perfect for experimental/acousmatic contexts |
| **TOTAL** | **100** | **86** | **High** |

**Weakest dimension**: Melodic Identity (6/10) — intentional, but means
the piece won't stick in memory the way a melodic work would. The
sound design carries the memorability instead.
