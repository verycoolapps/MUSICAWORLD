# Sound-Effect Blueprint — <SFX NAME>

> One file per SFX family. Follow `references/sound-design.md` layer
> grammar and implementation spec exactly. Unquantified adjectives
> ("big," "epic") are not specifications — every parameter needs a
> number.

## 1. Identity

| Field | Value |
|---|---|
| **Name** | |
| **Function** | (what it communicates: weight / danger / magic / tech / scale — one primary) |
| **Duration** | ms total (attack → tail end −60dB) |
| **Loop?** | one-shot / loopable (if loop, state seam strategy) |
| **Sonic adjectives** | (2–3: e.g. "granular, sub-heavy, crystalline") |
| **Metaphor** | (1 image that anchors the design: "a glacier calving under water") |
| **Fictional-world physics** | (what object/action produces this in-world?) |

## 2. Layer Grammar

> 2–5 layers. Each layer MUST specify: source, processing, level.
> Levels in dB relative to SFX peak (0 dBFS reference).

### Layer 1 — TRANSIENT (attack definition)

| Field | Value |
|---|---|
| Source | (click / noise burst / snap / oscillator tick) |
| Content | (e.g. 3ms bandpassed noise at 2.8kHz, Q=8) |
| Processing | (EQ / transient shaper / clip) |
| Level | dB |
| Frequency band owned | Hz |

### Layer 2 — BODY (mass/tone)

| Field | Value |
|---|---|
| Source | (pitched element / resonant sweep / modal partials) |
| Content | (e.g. sine 55Hz → pitch drop to 38Hz over 400ms) |
| Processing | |
| Level | dB |
| Frequency band owned | Hz |

### Layer 3 — TEXTURE (character)

| Field | Value |
|---|---|
| Source | (granular / reversed / modulated / formant) |
| Content | (e.g. 80ms grains, density 40/sec, pitch scatter ±200 cents) |
| Processing | |
| Level | dB |
| Frequency band owned | Hz |

### Layer 4 — TAIL (decay/release)

| Field | Value |
|---|---|
| Source | (reverb tail / pitch fall / noise wash) |
| Content | (e.g. pitch falls 220→55Hz over 1.8s + dark hall verb) |
| Processing | |
| Level | dB |
| Frequency band owned | Hz |

### Layer 5 — SUB (weight; felt not heard)

| Field | Value |
|---|---|
| Source | (sine/triangle 30–80Hz) |
| Content | |
| Processing | (mono-sum requirement) |
| Level | dB |
| Frequency band owned | Hz |

### Band budget check

| Band | Assigned layer | Notes (no mud) |
|---|---|---|
| 20–60Hz | | |
| 60–250Hz | | |
| 250Hz–2kHz | | |
| 2–6kHz | | |
| 6–16kHz | | |

## 3. Ordered Processing Chain

> Order matters: EQ before distortion, compression before reverb
> decisions, sends after dynamics.

```
1. Gain stage / trim
2. High-pass filter (state Hz — protects low band for sub layer)
3. EQ — subtractive (freq, Q, gain per cut)
4. EQ — additive (air/presence boosts)
5. Dynamics (compressor: ratio, attack, release, threshold)
6. Saturation / distortion (type, drive, mix)
7. Stereo imaging (width %, mid/side)
8. Reverb / delay (send level, pre-delay, decay, filter)
9. Limiter (ceiling dBTP)
10. Output gain / fade
```

Fill actual values into each step. Mark which are per-layer vs.
master-bus.

## 4. Frequency Behavior Over Time

| Time (ms) | Dominant band | Motion | Purpose |
|---|---|---|---|
| 0–20 | | | attack clarity |
| 20–200 | | | body establishment |
| 200–1000 | | | texture/tail |
| >1000 | | | decay, room |

## 5. Spatial Design

| Parameter | Value |
|---|---|
| Width strategy | (mono sub / stereo mids / decorrelated highs) |
| Depth | (pre-delay ms, wet %) |
| Distance cue | (HF rolloff Hz, level vs. close variant) |
| Movement | (pan/autom filter curve if one-shot or loop) |
| Surround placement (if 5.1/Atmos) | |

## 6. Implementation Instructions

**Method**: (synthesize / physical-model approximation / granular /
field-record-style / library + heavy processing)

Step-by-step build recipe (DAW-agnostic; name the *sound*, not the
button):

```
1. Create base: [source + settings]
2. Layer 2 enters at [time/level] doing [motion]
3. Apply [process] — [parameters]
4. ...
```

**Source material suggestions**: (what to record/synthesize/library —
be specific: "a wine glass struck and damped," "brown noise through
24dB/oct lowpass")

## 7. Variants (if needed)

| Variant | Change from base | Used for |
|---|---|---|
| Close/distant | | |
| Small/large scale | | |
| Friendly/hostile | | |
| Loop-safe version | | |

## 8. Mix Integration Notes

- Frequency conflicts with music (which band to duck under score)
- Dialogue carve requirements (if any)
- Batch/export spec (format, sample rate, normalization)

## 9. Quality Gate (internal)

- [ ] Function readable without seeing the event
- [ ] Every parameter quantified (Hz, dB, ms)
- [ ] Band budget assigned, no full-bandwidth collisions
- [ ] Loop seam addressed or declared one-shot
- [ ] Mono-compat checked on sub content
- [ ] Distinct from generic "whoosh/reverb" defaults
