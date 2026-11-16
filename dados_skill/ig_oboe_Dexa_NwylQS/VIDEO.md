---
videomd: 1
name: ig-oboe-dexa-nwylqs
description: 'Made with (inferred): AI-generated video 50%, 3D render 40%, still image + pan/zoom 8%, code / template render 2%'
source:
  file: ig_oboe_Dexa_NwylQS.mp4
  sha256: 9b75c6dc0e6d8b88ff9cdf7db13fd102bdd461657bd5c9f0c2361a71db625d62
  duration: 60.602
  size: 720x1280
  fps: 23.976
  aspect: '9:16'
shots: 60
lang: en
made_mix:
  ai_video: 0.5038
  cg_3d: 0.3992
  still_motion: 0.0819
  code_render: 0.0151
confidence: 0.513
readers:
- tools
open_questions: 57
generator:
  name: rea-video
  version: 0.1.0
---

# ig_oboe_Dexa_NwylQS.mp4

**Verdict** (inferred): Mixed production: AI-generated video 50% + 3D render 40% + still image + pan/zoom 8% + code / template render 2%; overlays: text labels, subtitles, title (composited in code / an editor); audio: music 129.2BPM (to confirm, leaning stock library music) + 9 possible sound effects (unconfirmed signal candidates)
**Made with** (inferred, by duration): AI-generated video 50%, 3D render 40%, still image + pan/zoom 8%, code / template render 2%
**Remake**: 24 3D render shots + 29 AI video shots → 4 generation units, 4 Seedance 2.0 calls; code render / screen capture 2 shots → 1 code project (2 parts); still-image move / static frame 5 shots → rebuilt locally

## Next steps

- No VLM ran: if you can see images, review first: `rea-video review <this dir>` → fill `review_answers.json` → `rea-video apply-review <this dir>`
- Remake: `rea-video remake <this dir>` does what can be done automatically and keeps the original elsewhere; `remake/status.md` says per shot what is left. Add incoming clips to `remake/mine.json` and run it again
- Code-rendered shots are redrawn by `rea-video code-remake <this dir>` (the step above runs it): edit `code/spec.json` and rerun, do not write one from scratch
- AI shots: prompts are in the generation units of `video/remake.md`; for automatic generation run `rea-video remake-plan` + `remake-run --dry-run` (paid: ask the user first)

## Open questions

- The VLM did not run (No VLM; live action / AI / 3D are told apart from pixel statistics only, so confidence is limited. An agent that can see images: run rea-vi…
- Shot #1 (0.0–0.9s): 3D render at only 40% confidence, runner-up ai_video
- Shot #2 (0.9–1.8s): 3D render at only 53% confidence, runner-up code_render
- Shot #3 (1.8–2.3s): AI-generated video at only 36% confidence, runner-up cg_3d
- Shot #5 (3.3–4.8s): photo / image: real material or generated, to confirm
- Shot #6 (4.8–6.3s): photo / image: real material or generated, to confirm
- Shot #7 (6.3–7.0s): AI-generated video at only 32% confidence, runner-up cg_3d
- Shot #8 (7.0–7.2s): code / template render at only 52% confidence, runner-up static_hold
- 49 more, see the `flag` lines in `video/timeline.md`

## Map

Read this page first; for detail, open only the file you need. Each line is `path | ~tokens | what is in it · when to read it`; paths are relative to this directory.

```videomd-map
video/timeline.md | 3233 | Timeline: one line per shot · what a stretch says, which shots need review, how a shot was made
video/content.md | 87 | Content and structure · what it says, the narrative line, structure, the script
video/cast.md | 66 | Cast, scenes and props · reference images for characters, first-frame prompts
video/sound.md | 786 | Sound · voice, music, sound effects, beats and sources
video/look.md | 484 | Camera, lighting and editing · for filmed shots: framing, camera, lighting, kit
video/remake.md | 3181 | Remake plan · generation units, shoots, code builds, real material to collect, acting and emotion
video/shots/*.md | 368 | Per-shot detail, tokens per file on average · checking one shot: what is seen, the inference and its basis, prompts, frames
breakdown.json | 130175 | Full raw data · for programs; a model rarely needs it
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
