# Audio Production Reference

Load for mixing, mastering, production guidance, and delivery specs.

## Technical Baseline

- Sample rate: 44.1kHz (music delivery) or 48kHz (video/game/film).
- Bit depth: 24-bit during production; 16-bit only at final delivery.
- Mono compatibility: check low end (<120Hz) and center-critical elements.
- True peak: ≤ −1 dBTP for streaming; −0.3 to −1 for general delivery.
- Loudness: streaming targets ≈ −14 LUFS integrated (Spotify/Apple);
  cinematic often −23 to −27 LUFS (leave headroom for dialogue);
  state target explicitly per deliverable.

## Mix Architecture

- **Gain staging**: healthy levels pre-fader; avoid mixing with master
  already loud.
- **EQ**: subtractive first (problem frequencies), additive second
  (air 10–16kHz, weight 60–120Hz). High-pass non-bass sources at 80–120Hz.
- **Compression**: 2:1–4:1 on vocals/drums bus; slow attack/fast release
  for punch; fast attack on bass for control. Parallel compression for
  drums when needing density without squashing transients.
- **Saturation**: subtle on drums/bass/vocals adds harmonics = perceived
  loudness without peak damage.
- **Reverb**: pre-delay separates source from space; high-pass reverb
  returns (nothing below ~200Hz in the verb); freeze/reverse for texture.
- **Delay**: dotted-eighth on vocals/guitars; tempo-synced; filter repeats.
- **Stereo imaging**: keep kick/bass/vocal lead dead center; widen
  doubles/keys/pads; check phase on wide elements.
- **Automation**: ride vocal level phrase-by-phrase; automate filter/
  reverb sends for section transitions.

## Mastering Chain (conceptual)

```
Bus processing → gentle EQ balance → bus compression (1–2:1, slow) →
limiting to true-peak ceiling → loudness metering → format export
```

Never suggest "mastering" that just means making it louder — describe
the tonal and dynamic decisions.

## Frequency Zones (quick map)

| Band | Role | Common problems |
|---|---|---|
| 20–60Hz | sub weight | mud if multiple sources |
| 60–250Hz | body/warmth | boxiness ~200–400Hz, rumble |
| 250Hz–2kHz | presence/core | harshness 2–5kHz on vocals |
| 2–6kHz | attack/clarity | sibilance 5–8kHz |
| 6–16kHz | air/detail | hiss, cymbal smear |

## Dynamic Storytelling

Map dynamics to emotion: verses sit 3–6dB below choruses; breakdowns
strip to essentials; final chorus +1–2dB lift. Automate, don't just
gain-stage louder.

## Deliverable Formats

- WAV/AIFF/FLAC: production & archival
- MP3 320k/AAC 256k: distribution preview
- OGG: open/web
- MIDI: composition spec (when requested)
- Stems: drums/bass/harmony/lead/vocals/FX — named and leveled
- Multitrack spec: session notes + track list + routing diagram

## DAW-Specific Notes

- **Ableton Live**: session/arrangement duality, return tracks, Max for
  Live generative possibilities.
- **FL Studio**: pattern workflow, Patcher for complex routing.
- **Logic Pro**: alchemy/sampler depth, spatial audio, quickSwipe.
- **REAPER**: routing flexibility, cheap, scriptable — good for prototyping.
- Never assume feature parity across DAWs; specify the *sound*, not the
  button.
