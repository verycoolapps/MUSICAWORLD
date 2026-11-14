# Game Audio Reference

Load for game music: menus, battles, exploration, adaptive scores,
procedural systems, and seamless loops.

## Musical Universe Design

A game's score is a system, not a playlist. Define in the Music Bible:

- **Main theme** — DNA motif, adaptable to all contexts.
- **Region/key map** — each area gets a mode or tonal center related to
  the main theme (e.g., forest = Lydian warmth, dungeon = Phrygian dark).
- **Battle transformation** — how the exploration theme mutates for
  combat (tempo ×2, minor swap, percussion entry).
- **Boss escalation** — each boss = motif variation + intensity tier.

## Track Types

| Type | Typical BPM | Length | Key traits |
|---|---|---|---|
| Main menu | 80–110 | 2–4 min loop | iconic motif upfront, full arrangement |
| Exploration | 90–120 | 2–5 min loop | layered, space for ambience |
| Battle | 140–180 | 1.5–3 min | driving rhythm, short harmonic rhythm |
| Boss | 150–200 | 2–4 min | motif + dissonance + metric tricks |
| Town | 70–100 | 2–3 min loop | warm, sparse, diatonic |
| Dungeon | 60–90 | 2–4 min loop | drone + pulse, minimal melody |
| Victory/defeat | one-shot | 5–20s | sting + cadence |
| Cutscene | free | varies | follows cinematic grammar |

## Adaptive & Interactive Systems

Concepts to specify (implementation-agnostic):

- **Vertical layering**: stems (drums / bass / harmony / lead / FX) mixed
  by game state. Specify which stem enters per intensity tier.
- **Horizontal resequencing**: sections A/B/C; transition rules
  (beat-matched, bar-matched, or stinger-triggered).
- **Parameter-driven**: tempo map follows player speed; filter follows
  damage; pitch-shift follows health.
- **Stinger system**: short musical punctuation for events (item get,
  level up, discovery) — must be tonally compatible with current track.
- **Seamless loops**: specify loop point, zero-crossing-safe tails,
  and intro/outro handles. For game loops, compose end→start as a
  continuous phrase, not fade-out.

## Middleware Notes

When relevant, mention Wwise/FMOD/MIDI-implementation feasibility:
- Sample-accurate sync points, stem naming conventions
  (`MUS_Battle_LayerDrums_01.wav` style), switch/RTPC maps.
- Keep MIDI spec separate from audio spec; a track may need both.

## Dynamic Difficulty Mapping

Battle music intensity tiers (example):
1. Enemies <30% → exploration layer only
2. 30–70% → drums enter
3. >70% or boss → full arrangement + lead motif
State the mapping logic so a programmer can implement it.

## Deliverable per Track

Title, context (when it plays), duration/loop, BPM, key/mode, meter,
full instrumentation, section map with timestamps, stem breakdown for
adaptive mixing, motif source (which theme it derives from), generation
prompt, quality score.
