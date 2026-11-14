# Sound Design Reference

Load for SFX, ambiences, impacts, UI sounds, and invented sonic textures.
SFX are an independent creative discipline — design identity first, then
synthesis.

## Design Process

1. **Function**: what does this sound communicate? (weight, danger,
   magic, technology, scale)
2. **Identity**: 1–2 adjectives + 1 metaphor ("a cathedral made of glass
   collapsing inward").
3. **Physics**: what would make this sound in the fictional world?
   Real-world analogy grounds synthesis choices.
4. **Layering**: 2–5 layers (transient / body / tail / air / sub).
5. **Processing chain**: order matters — EQ before distortion, reverb send
   after compression decisions.
6. **Frequency budget**: assign bands per layer so nothing muddies.

## Layer Grammar

| Layer | Role | Typical content |
|---|---|---|
| Transient | attack definition | click, noise burst, snap |
| Body | mass/tone | pitched element, resonant sweep |
| Texture | character | granular, reversed, modulated |
| Tail | decay/release | reverb tail, pitch fall, noise wash |
| Sub | weight | sine/triangle 30–80Hz, felt not heard |

## Synthesis Methods

- **Pitched**: sine/saw/square + FM for metallic/bell; additive for
  crystalline; granular for organic-digital hybrids.
- **Noise-based**: filtered noise (bandpass sweep = whoosh; lowpass boom;
  highpass air). Always specify filter type, cutoff motion, resonance.
- **Physical modeling concepts**: modal synthesis for objects, waveguide
  for strings/air — describe target, implement via approximations.
- **Granular & clouds**: grain size 20–200ms, density, pitch scatter.
- **Pitch envelopes**: pitch drops = weight/impact; rises = power-up/portal;
  vibrato depth/rate for organic life.

## Category Playbooks

- **Magic**: rising shimmer + sub swell + reverse-reverb tail; specify
  "spell charge" (ascending partials) vs. "cast" (impact + bloom).
- **Technology**: precise transients, bit-crushed layers, square-wave
  bleeps, servo whirs; avoid organic randomness — quantize deliberately.
- **Creatures**: layered detuned oscillators + formant filters + breath
  noise; breathing = filtered noise with 0.2–0.5Hz amplitude LFO.
- **Environments**: loopable beds — wind (filtered noise, slow LFO),
  water (bubbly granular), machinery (rhythmic clanks + hum).
- **Impacts**: transient snap + low thump (60–120Hz decay) + debris
  scatter (short noise grains) + optional pitch-down tail.

## Spatial Design

- **Width**: mono sub, stereo mids, wide highs; specify decorrelation.
- **Depth**: pre-delay on reverb (10–80ms) separates dry from wet.
- **Distance**: high-frequency rolloff + reverb wet% + level as distance cues.
- **Movement**: automation curves for pan/filters on one-shots or loops.

## Implementation Spec (per SFX)

```
Name / Function / Duration / Loop? / Key freq behavior /
Layers (each: source, processing, level) /
Processing chain (ordered) / Spatial settings / Source material
suggestions (synthesize, field-record-style, library) /
Batch variants if needed
```

## Anti-Patterns

- White noise with a reverb = not a design.
- Every SFX at full bandwidth — leave room for music/dialogue.
- Unquantified "epic" — specify Hz, dB, ms, or it doesn't exist.
