# Instrument Invention — <INSTRUMENT NAME>

> Spec per §"Instrument Forge". If the instrument cannot be physically
> built, the synthesis method IS the deliverable — make it realizable.

## 1. Identity

| Field | Value |
|---|---|
| **Name** | (evocative, pronounceable, not random) |
| **Concept** (1–2 sentences: what is this instrument *for*?) | |
| **Sound family** | (acoustic / electroacoustic / fully synthetic / hybrid) |
| **Origin fiction** | (why does it exist — world, ritual, technology?) |

## 2. Construction (physical or conceptual)

- **Body/resonator**: (material, shape, size — or digital architecture)
- **Excitation source**: (bow / breath / struck / plucked / electric
  field / algorithmic)
- **Modifiers**: (what the player touches to change sound)
- **Build constraints**: (cost, portability, skill required)

## 3. Sound-Generation Mechanism

**If acoustic/electroacoustic:**
- Physical principle (e.g. "strings excited by electromagnetic
  impulse, resonated in a tuned metal chamber")
- Why this produces the intended timbre

**If synthetic (must specify a realizable method):**
- Engine: (subtractive / FM / granular / physical modeling / modal /
  sample-based / hybrid)
- Voice architecture: (how many partials/voices, how detuned)
- Modulation sources: (LFO rates, envelopes, performance inputs)
- Control map: (which physical gesture maps to which parameter —
  e.g. "pressure on pad = filter cutoff 200–4000Hz")

```
Recipe sketch (one voice):
Osc: saw → waveshaper → multimode filter (LP 12dB/oct)
LFO1 0.3Hz → filter cutoff ±800Hz (breathing)
LFO2 5.1Hz → osc detune ±8 cents (chorus shimmer)
Env: attack 40ms, decay 600ms, sustain 0.6, release 1.2s
Exciter: noise burst → bandpass 1.2kHz Q=2 → amplitude × envelope
Output: subtle convolution reverb (generated impulse, 1.8s decay)
```

## 4Sonic Characteristics

| Field | Value |
|---|---|
| **Register** | (lowest–highest playable note) |
| **Timbre adjectives** | (3: e.g. "glassy, breathing, metallic-warm") |
| **Attack behavior** | (instant / breathy / bowed / percussive) |
| **Decay behavior** | (sustain / natural decay / gated / evolving) |
| **Harmonic content** | (inharmonic partials? even/odd? noise floor?) |

## 5. Frequency Behavior

| Band | Energy | Character |
|---|---|---|
| 20–60Hz | | (sub presence? keep out?) |
| 60–250Hz | | |
| 250Hz–2kHz | | (core/identity band) |
| 2–6kHz | | |
| 6–16kHz | | (air/harshness risk) |

Mono/stereo note: what collapses in mono, what stays wide.

## 6. Playing Technique

| Technique | Gesture | Resulting sound |
|---|---|---|
| Sustain/basic | | |
| Articulation 1 | | |
| Articulation 2 | | |
| Extended | | |

Expressive controls: vibrato (rate/depth), timbre morphing,
dynamic response curve.

## 7. Dynamic Range & Response

- **Dynamic range**: (pp–ff equivalent; dB span if applicable)
- **Response curve**: (linear? exponential? velocity→what)
- **Polyphony**: (chords? max voices?)
- **Tuning**: (equal temperament / microtonal / dronable unison)

## 8. Musical Role

- **Primary function**: (lead / pad / rhythm / texture / bass)
- **What it replaces in an ensemble**: (what gap does it fill?)
- **Emotional identity**: (what does it make listeners feel and why)
- **Signature gesture**: (the one playable move that identifies it)

## 9. Practical Production Implementation

### A. If physically buildable

- Bill of materials / construction notes / tuning procedure
- Recording approach (mic positions, room)
- Maintenance reality check

### B. If synthesized (the usual path)

- **Platform**: (Vital / Surge XT / Pure Data / Max / Reaktor /
  custom code / physical modeling synth)
- **Preset architecture**: (macro map — which knobs do what)
- **Performance-ready spec**: (MIDI CC map, keyswitch zones,
  velocity layers if sampled)
- **Fallback**: (if synthesis is too complex — layered approximation
  from stock sources, with exact processing chain)

```
Macro map example:
Knob 1: Filter cutoff (200–6000Hz, exponential)
Knob 2: Resonance + grain density (hybrid morph)
Knob 3: Reverb mix + pitch drift ±50 cents
Pedal/CC1: Exciter noise level
CC11: Output level / expression
```

## 10. Application Notes

- Best genres/contexts (genre-agnostic spec, but note where it shines)
- Pairing suggestions (instruments/textures that complement vs. fight)
- Common failure mode (what makes it sound cheap — e.g. too much
  resonance, no breath noise)

## 11. Quality Gate

- [ ] Realizable — someone could build or program this today
- [ ] Timbre described by mechanism, not just adjectives
- [ ] Control map complete enough to perform, not just patch
- [ ] Frequency budget assigned (doesn't collide with typical mixes)
- [ ] Emotional identity stated and defensible
