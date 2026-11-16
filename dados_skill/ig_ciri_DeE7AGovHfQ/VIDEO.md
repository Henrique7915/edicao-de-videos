---
videomd: 1
name: ig-ciri-dee7agovhfq
description: 'Made with (inferred): AI-generated video 71%, live action 25%, 3D render 4%'
source:
  file: ig_ciri_DeE7AGovHfQ.mp4
  sha256: b17ce31c9c0618b6564c3eb398065c767d6f145363f54b2110589de09386a1c8
  duration: 30.367
  size: 720x1280
  fps: 30.0
  aspect: '9:16'
shots: 34
lang: en
made_mix:
  ai_video: 0.7113
  live_action: 0.2492
  cg_3d: 0.0395
confidence: 0.532
readers:
- tools
open_questions: 37
generator:
  name: rea-video
  version: 0.1.0
---

# ig_ciri_DeE7AGovHfQ.mp4

**Verdict** (inferred): Mixed production: AI-generated video 71% + live action 25% + 3D render 4% (71% of the duration lacks evidence for live action vs AI, to confirm); overlays: text labels, subtitles, title (composited in code / an editor); real material used: live footage (own footage or a film / drama clip, confirm by looking) (7.6s); audio: voice + music 178.2BPM (to confirm, leaning stock library music)
**Made with** (inferred, by duration): AI-generated video 71%, live action 25%, 3D render 4%
**Remake**: 3 3D render shots + 10 AI video shots → 6 generation units, 6 Seedance 2.0 calls; live action 21 shots → 3 scenes, 6 camera setups
**Real material to collect**: 21 shots (25% of the duration), list in `video/remake.md`

## Next steps

- No VLM ran: if you can see images, review first: `rea-video review <this dir>` → fill `review_answers.json` → `rea-video apply-review <this dir>`
- Remake: `rea-video remake <this dir>` does what can be done automatically and keeps the original elsewhere; `remake/status.md` says per shot what is left. Add incoming clips to `remake/mine.json` and run it again
- AI shots: prompts are in the generation units of `video/remake.md`; for automatic generation run `rea-video remake-plan` + `remake-run --dry-run` (paid: ask the user first)

## Open questions

- The VLM did not run (No VLM; live action / AI / 3D are told apart from pixel statistics only, so confidence is limited. An agent that can see images: run rea-vi…
- Shot #1 (0.0–0.2s): live action at only 58% confidence, runner-up ai_video
- Shot #2 (0.2–0.4s): 3D render at only 50% confidence, runner-up live_action
- Shot #3 (0.4–0.6s): live action at only 50% confidence, runner-up ai_video
- Shot #4 (0.6–0.7s): live action at only 48% confidence, runner-up ai_video
- Shot #5 (0.7–0.9s): 3D render at only 39% confidence, runner-up live_action
- Shot #6 (0.9–1.0s): live action at only 57% confidence, runner-up ai_video
- Shot #7 (1.0–1.6s): live action at only 56% confidence, runner-up ai_video
- 29 more, see the `flag` lines in `video/timeline.md`

## Map

Read this page first; for detail, open only the file you need. Each line is `path | ~tokens | what is in it · when to read it`; paths are relative to this directory.

```videomd-map
video/timeline.md | 1840 | Timeline: one line per shot · what a stretch says, which shots need review, how a shot was made
video/content.md | 87 | Content and structure · what it says, the narrative line, structure, the script
video/cast.md | 61 | Cast, scenes and props · reference images for characters, first-frame prompts
video/sound.md | 555 | Sound · voice, music, sound effects, beats and sources
video/look.md | 711 | Camera, lighting and editing · for filmed shots: framing, camera, lighting, kit
video/remake.md | 2468 | Remake plan · generation units, shoots, code builds, real material to collect, acting and emotion
video/shots/*.md | 479 | Per-shot detail, tokens per file on average · checking one shot: what is seen, the inference and its basis, prompts, frames
breakdown.json | 85923 | Full raw data · for programs; a model rarely needs it
shots/ | - | contact sheet, first and last frame of each shot · checking by eye
storyboard.jpg | - | storyboard of the whole video · the whole video at a glance
audio.png | - | waveform and beat chart · seeing the rhythm
```

## How to read

- One shot per line: `#<n> start-end (s) | key value | …`. A key ending in `~` is the tools' inference; keys without it are visible on screen or measured directly.
- `story` job in the story and the point · `seen` what is on screen · `act` acting (emotion, strength, face) · `camera` camera move · `overlay` overlays · `made~` how it was made (inferred) · `material~` where the material came from (inferred) · `remake` remake route · `flag` needs a second look
- Full detail for a shot is in `video/shots/<n>.md` (e.g. `video/shots/07.md`).
- What is “seen” can be checked against the frames; what is “inferred” is the tools' and image readers' judgement, with the basis in each shot file. When they disagree, trust the frames.
