# Music Generation Prompt — Template

> Master template for external AI music platforms (Suno, Udio, Stable
> Audio, ElevenLabs Music, Riffusion). Fill EVERY field with real
> content — platforms reward specificity and punish vagueness.
> Per `SKILL.md` §9, adapt format per platform; never paste blindly.

## 1. Base Prompt (universal fields)

```
[CONCEPT]
One-sentence artistic intent: what is this music FOR and what should
the listener feel? Include narrative/emotional hook, not just genre.

[GENRE / HYBRID]
Primary genre + secondary influence. Name borrowed elements:
"indie folk × lo-fi hip-hop" or "orchestral hybrid × industrial".
Avoid artist names — translate to characteristics if needed.

[EMOTION]
Primary emotion + sub-variant + arc direction
(e.g. "bittersweet nostalgia resolving into quiet defiance").

[TEMPO / METER / KEY]
BPM + time signature + key or mode.
(e.g. "92 BPM, 6/8, D Dorian")

[INSTRUMENTATION]
Core palette, 3–6 elements, with playing style:
(e.g. "fingerpicked nylon guitar, upright bass, brushed drums,
soft female lead vocal, tape-saturated Rhodes")

[VOCALS]
Presence (instrumental / lead / harmony / choir / none),
language, delivery style, register.
For instrumental: state "instrumental, no vocals" explicitly.

[MEL/HARMONIC DIRECTION]
Hook description + chord language:
(e.g. "hook centers on a falling minor-third sigh; verses on i–VI–III–VII,
chorus lifts to bVI–VII–v–i with a suspended-4 color")

[GROOVE]
Rhythmic feel: straight/swinged/double-time, where the pocket sits,
percussion character.

[ARRANGEMENT]
Section energy map: intro sparse → verse builds → chorus peak →
breakdown → final lift. State dynamics (quiet verse, big chorus).

[PRODUCTION AESTHETIC]
Sonic world: lo-fi tape / polished modern / room-live / cinematic /
granular digital. Reverb space, texture (vinyl, hiss, saturation).

[DYNAMICS / TEXTURE]
Frequency character: warm/sub-heavy / bright/airy / mid-forward.
Texture layers: noise, field recording, granular haze.

[ENDING]
How it resolves: fade / final hit / unresolved tail / loop point.

[NEGATIVE CONSTRAINTS]
What to avoid: vocals (if instrumental), clichés, specific
instruments, tempo range, "no drops," "no trap hi-hats," etc.
```

## 2. Per-Platform Adaptation Notes

### Suno (v3.5+ / v4)

- Two fields: **Style of Music** (comma-separated descriptors,
  ~120 char sweet spot) and **Lyrics** (can be `[Instrumental]`).
- Style field is keyword-dense: genre tags work better than sentences.
- For instrumentals, lyrics field = `[Instrumental]` or `[Intro]` +
  section tags to shape structure (`[Chorus]`, `[Bridge]`).
- BPM/key: Suno responds to tempo words ("slow," "uptempo") and
  genre tags better than literal "92 BPM" — put BPM in the concept
  sentence AND use feel words.
- Custom mode accepts longer prompts; use the full template.

**Adapted example:**
```
Style: indie folk, lo-fi, 92 BPM feel, D dorian, fingerpicked nylon
guitar, upright bass, brushed drums, Rhodes, tape saturation,
nostalgic but defiant, female vocals Indonesian
Lyrics: [Instrumental]   ← or full lyric sheet with section tags
```

### Udio

- **Prompt** field accepts prose descriptions — write sentences, not
  keyword lists.
- **Lyrics** field separate; `[Instrumental]` supported.
- Udio responds well to production-aesthetic language ("recorded to
tape," "live room reverb") — put sonic world in prose.
- Longer prompts (200–500 chars) work; front-load the most important
  descriptor.

**Adapted example:**
```
Prompt: An intimate Indonesian indie-folk song at a slow 92 BPM in
D dorian. Fingerpicked nylon guitar and upright bass over brushed
drums, with a soft Rhodes and tape-worn texture. A breathy female
vocal moves from quiet nostalgia to defiant warmth. Warm midrange,
lo-fi production, live-room feel.
```

### Stable Audio / Stable Audio Open

- Prompt + **negative prompt** fields; seconds duration parameter.
- Works best with descriptive phrases: "distant thunder," "analog
tape hiss," "orchestral strings swelling."
- Negative prompt is powerful — use it for real constraints
  ("vocals, drums, distortion").
- No lyrics support — instrumental/texture generator.

**Adapted example:**
```
Prompt: cinematic underscore, slow string ostinato, low drone,
subtle piano motif, distant thunder texture, 70 BPM, D minor,
hall reverb, building tension, no vocals
Negative: vocals, lyrics, drums, electronic beats, distorted guitars
```

### ElevenLabs Music / Riffusion / others

- Similar prose-prompt model; check current docs for lyric support.
- For lyric-bearing platforms, always include a **pronunciation
  guide** for non-English lyrics (Indonesian stress patterns differ
  from English).

## 3. Prompt Quality Checklist

Before submitting any prompt:

- [ ] Concept present — music has a *reason*, not just a genre tag
- [ ] Genre/hybrid named with borrowed elements identified
- [ ] Emotion + arc direction stated (not just "sad" or "epic")
- [ ] BPM/meter/key given (or deliberately omitted with reason)
- [ ] Instrumentation 3–6 elements, no more
- [ ] Vocal presence explicit (or "instrumental" stated twice)
- [ ] Melodic/harmonic direction described (hook + chord language)
- [ ] Groove/pocket defined (straight, swung, half-time)
- [ ] Arrangement energy map (intro→verse→chorus→outro)
- [ ] Production aesthetic specified (lo-fi, polished, cinematic)
- [ ] Texture/noise layers mentioned if relevant
- [ ] Ending behavior defined
- [ ] Negative constraints listed (at least 2–3)
- [ ] No artist names — characteristics only
- [ ] No claims of originality/novelty in the prompt itself

## 4. Iteration Protocol

When a generation misses:

1. **Diagnose which field failed** — wrong genre? wrong emotion?
   muddy mix? missing hook?
2. **Change ONE dimension at a time** — don't rewrite everything.
3. **Move failed descriptors earlier** — platforms weight opening
   tokens more heavily.
4. **If vocals wrong**: check language field, add pronunciation
   guide, try separate lyric sheet vs. embedded.
5. **If mix muddy**: reduce instrumentation count, specify "sparse"
   or "minimal arrangement," high-pass language ("bright top end,
   clean lows").
6. **If structure wrong**: use explicit section tags in lyrics field
   (`[Verse]`, `[Chorus]`) or describe arc in prose.

## 5. Prompt Hygiene

- **Never** paste lyrics with copyrighted text.
- **Never** use artist names even as shorthand — "in the style of X"
  fails copyright + often triggers filters.
- **Never** promise the platform will produce audio files — you're
  writing a prompt, not generating audio.
- **Always** verify current platform capabilities if unsure — features
  change between versions.
