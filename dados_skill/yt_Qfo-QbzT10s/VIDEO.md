---
videomd: 1
name: yt-qfo-qbzt10s
description: 'Made with (inferred): AI-generated video 83%, 3D render 10%, code / template render 6%'
source:
  file: yt_Qfo-QbzT10s.mp4
  sha256: 1c95d278cb49537a48066c8f0e991f9ce1d03c393942801a32b4c2fb5b64c6c7
  duration: 60.06
  size: 720x1280
  fps: 23.976
  aspect: '9:16'
shots: 70
lang: en
made_mix:
  ai_video: 0.8347
  cg_3d: 0.1007
  code_render: 0.0646
confidence: 0.433
readers:
- tools
open_questions: 72
generator:
  name: rea-video
  version: 0.1.0
---

# yt_Qfo-QbzT10s.mp4

**Verdict** (inferred): Mixed production: AI-generated video 83% + 3D render 10% + code / template render 6% (83% of the duration is live action or AI, to confirm: the platform transcode erased the noise evidence, needs a VLM pass or a human look at the frames); overlays: animated sticker / GIF, styled text, text labels, subtitles, title (composited in code / an editor); audio: music 110.0BPM (to confirm, leaning stock library music) + 1 sound effects; packaging: styled text ×9, text labels ×75, stickers / GIFs ×1, 1 sound effects land on text / sticker pops
**Made with** (inferred, by duration): AI-generated video 83%, 3D render 10%, code / template render 6%
**Remake**: 61 AI video shots + 7 3D render shots → 4 generation units, 4 Seedance 2.0 calls; code render / screen capture 2 shots → 1 code project (2 parts)

## Next steps

- No VLM ran: if you can see images, review first: `rea-video review <this dir>` → fill `review_answers.json` → `rea-video apply-review <this dir>`
- Remake: `rea-video remake <this dir>` does what can be done automatically and keeps the original elsewhere; `remake/status.md` says per shot what is left. Add incoming clips to `remake/mine.json` and run it again
- Code-rendered shots are redrawn by `rea-video code-remake <this dir>` (the step above runs it): edit `code/spec.json` and rerun, do not write one from scratch
- AI shots: prompts are in the generation units of `video/remake.md`; for automatic generation run `rea-video remake-plan` + `remake-run --dry-run` (paid: ask the user first)

## Open questions

- The VLM did not run (No VLM; live action / AI / 3D are told apart from pixel statistics only, so confidence is limited. An agent that can see images: run rea-vi…
- Shot #1 (0.0–1.0s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #2 (1.0–1.8s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #3 (1.8–2.3s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #4 (2.3–3.0s): 3D render at only 42% confidence, runner-up ai_video
- Shot #5 (3.0–3.8s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #6 (3.8–4.3s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #7 (4.3–5.0s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- 64 more, see the `flag` lines in `video/timeline.md`

## Map

Read this page first; for detail, open only the file you need. Each line is `path | ~tokens | what is in it · when to read it`; paths are relative to this directory.

```videomd-map
video/timeline.md | 3549 | Timeline: one line per shot · what a stretch says, which shots need review, how a shot was made
video/content.md | 87 | Content and structure · what it says, the narrative line, structure, the script
video/cast.md | 83 | Cast, scenes and props · reference images for characters, first-frame prompts
video/sound.md | 553 | Sound · voice, music, sound effects, beats and sources
video/look.md | 417 | Camera, lighting and editing · for filmed shots: framing, camera, lighting, kit
video/packaging.md | 3130 | Packaging · subtitles, styled text, stickers, picture-in-picture: timing and style
video/remake.md | 4056 | Remake plan · generation units, shoots, code builds, real material to collect, acting and emotion
video/shots/*.md | 437 | Per-shot detail, tokens per file on average · checking one shot: what is seen, the inference and its basis, prompts, frames
breakdown.json | 178521 | Full raw data · for programs; a model rarely needs it
shots/ | - | contact sheet, first and last frame of each shot · checking by eye
storyboard.jpg | - | storyboard of the whole video · the whole video at a glance
stems/ | - | voice, music and effects stems · listening, remaking the sound
sfx/ | - | a clip of each sound effect · finding matching effects
packaging/ | - | subtitle files, packaging timeline, sticker frames · remaking subtitles and packaging
frames/ | - | picture scenes: full-size frames, the drawn layer cut out and sampled, measurements · remaking rendered pictures
audio.png | - | waveform and beat chart · seeing the rhythm
```

## How to read

- One shot per line: `#<n> start-end (s) | key value | …`. A key ending in `~` is the tools' inference; keys without it are visible on screen or measured directly.
- `story` job in the story and the point · `seen` what is on screen · `act` acting (emotion, strength, face) · `camera` camera move · `overlay` overlays · `made~` how it was made (inferred) · `material~` where the material came from (inferred) · `remake` remake route · `flag` needs a second look
- Full detail for a shot is in `video/shots/<n>.md` (e.g. `video/shots/07.md`).
- What is “seen” can be checked against the frames; what is “inferred” is the tools' and image readers' judgement, with the basis in each shot file. When they disagree, trust the frames.
