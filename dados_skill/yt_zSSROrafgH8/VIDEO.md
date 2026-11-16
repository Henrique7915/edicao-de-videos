---
videomd: 1
name: yt-zssrorafgh8
description: 'Made with (inferred): AI-generated video 62%, code / template render 16%, live action 11%, still image + pan/zoom 5%, 3D render 5%, static hold 1%'
source:
  file: yt_zSSROrafgH8.mp4
  sha256: 1605b2e9cb3f6fe63e6ba0c42456242161794491640f7042eef3ffc64758667e
  duration: 35.083
  size: 720x1280
  fps: 60.001
  aspect: '9:16'
shots: 21
lang: en
made_mix:
  ai_video: 0.6242
  code_render: 0.1587
  live_action: 0.113
  still_motion: 0.0504
  cg_3d: 0.048
  static_hold: 0.0057
confidence: 0.656
readers:
- tools
open_questions: 23
generator:
  name: rea-video
  version: 0.1.0
---

# yt_zSSROrafgH8.mp4

**Verdict** (inferred): Mixed production: AI-generated video 62% + code / template render 16% + live action 11% + still image + pan/zoom 5% + 3D render 5% + static hold 1% (62% of the duration lacks evidence for live action vs AI, to confirm); overlays: text labels, subtitles (composited in code / an editor); real material used: live footage (own footage or a film / drama clip, confirm by looking) (4.0s); audio: voice + music 129.2BPM (to confirm, leaning AI-generated music) + 4 possible sound effects (unconfirmed signal candidates)
**Made with** (inferred, by duration): AI-generated video 62%, code / template render 16%, live action 11%, still image + pan/zoom 5%, 3D render 5%, static hold 1%
**Remake**: 15 AI video shots + 1 3D render shot → 4 generation units, 4 Seedance 2.0 calls; live action 2 shots → 1 scene, 1 camera setup; code render / screen capture 1 shot → 1 code project; still-image move / static frame 2 shots → rebuilt locally
**Real material to collect**: 2 shots (11% of the duration), list in `video/remake.md`

## Next steps

- No VLM ran: if you can see images, review first: `rea-video review <this dir>` → fill `review_answers.json` → `rea-video apply-review <this dir>`
- Remake: `rea-video remake <this dir>` does what can be done automatically and keeps the original elsewhere; `remake/status.md` says per shot what is left. Add incoming clips to `remake/mine.json` and run it again
- Code-rendered shots are redrawn by `rea-video code-remake <this dir>` (the step above runs it): edit `code/spec.json` and rerun, do not write one from scratch
- AI shots: prompts are in the generation units of `video/remake.md`; for automatic generation run `rea-video remake-plan` + `remake-run --dry-run` (paid: ask the user first)

## Open questions

- The VLM did not run (No VLM; live action / AI / 3D are told apart from pixel statistics only, so confidence is limited. An agent that can see images: run rea-vi…
- Shot #1 (0.0–1.8s): photo / image: real material or generated, to confirm
- Shot #2 (1.8–3.8s): AI or live action, to confirm: only a sharpness rhythm, no duplicate frames (re-encodes leave it too) and no AIGC label, needs an image read…
- Shot #3 (3.8–5.5s): 3D render at only 42% confidence, runner-up ai_video
- Shot #4 (5.5–7.3s): AI or live action, to confirm: only a sharpness rhythm, no duplicate frames (re-encodes leave it too) and no AIGC label, needs an image read…
- Shot #5 (7.3–9.2s): AI, 24p camera footage or film / TV footage, to confirm: only frame-rate evidence (a 24fps source, which films and TV share) and no AIGC lab…
- Shot #6 (9.2–11.1s): AI or live action, to confirm: only a sharpness rhythm, no duplicate frames (re-encodes leave it too) and no AIGC label, needs an image rea…
- Shot #7 (11.1–13.1s): AI or live action, to confirm: only a sharpness rhythm, no duplicate frames (re-encodes leave it too) and no AIGC label, needs an image re…
- 15 more, see the `flag` lines in `video/timeline.md`

## Map

Read this page first; for detail, open only the file you need. Each line is `path | ~tokens | what is in it · when to read it`; paths are relative to this directory.

```videomd-map
video/timeline.md | 1202 | Timeline: one line per shot · what a stretch says, which shots need review, how a shot was made
video/content.md | 87 | Content and structure · what it says, the narrative line, structure, the script
video/cast.md | 54 | Cast, scenes and props · reference images for characters, first-frame prompts
video/sound.md | 779 | Sound · voice, music, sound effects, beats and sources
video/look.md | 705 | Camera, lighting and editing · for filmed shots: framing, camera, lighting, kit
video/remake.md | 2930 | Remake plan · generation units, shoots, code builds, real material to collect, acting and emotion
video/shots/*.md | 494 | Per-shot detail, tokens per file on average · checking one shot: what is seen, the inference and its basis, prompts, frames
breakdown.json | 56567 | Full raw data · for programs; a model rarely needs it
shots/ | - | contact sheet, first and last frame of each shot · checking by eye
storyboard.jpg | - | storyboard of the whole video · the whole video at a glance
sfx/ | - | a clip of each sound effect · finding matching effects
frames/ | - | picture scenes: full-size frames, the drawn layer cut out and sampled, measurements · remaking rendered pictures
audio.png | - | waveform and beat chart · seeing the rhythm
```

## How to read

- One shot per line: `#<n> start-end (s) | key value | …`. A key ending in `~` is the tools' inference; keys without it are visible on screen or measured directly.
- `story` job in the story and the point · `seen` what is on screen · `act` acting (emotion, strength, face) · `camera` camera move · `overlay` overlays · `made~` how it was made (inferred) · `material~` where the material came from (inferred) · `remake` remake route · `flag` needs a second look
- Full detail for a shot is in `video/shots/<n>.md` (e.g. `video/shots/07.md`).
- What is “seen” can be checked against the frames; what is “inferred” is the tools' and image readers' judgement, with the basis in each shot file. When they disagree, trust the frames.
