---
videomd: 1
name: yt-b3kb6elfv6c
description: 'Made with (inferred): 3D render 51%, AI-generated video 47%, live action 1%, still image + pan/zoom 1%'
source:
  file: yt_B3Kb6elfv6c.mp4
  sha256: c9595b665fb647f4e8a06d557c3333dfa858a2789b2adc536eecdb863d194a0f
  duration: 59.0
  size: 720x1280
  fps: 24.0
  aspect: '9:16'
shots: 71
lang: en
made_mix:
  cg_3d: 0.5057
  ai_video: 0.4703
  live_action: 0.0148
  still_motion: 0.0092
confidence: 0.453
readers:
- tools
open_questions: 71
generator:
  name: rea-video
  version: 0.1.0
---

# yt_B3Kb6elfv6c.mp4

**Verdict** (inferred): Mixed production: 3D render 51% + AI-generated video 47% + live action 1% + still image + pan/zoom 1% (49% of the duration is live action or AI, to confirm: the platform transcode erased the noise evidence, needs a VLM pass or a human look at the frames); overlays: text labels, static graphics, subtitles, title (composited in code / an editor); real material used: live footage (own footage or a film / drama clip, confirm by looking) (0.9s); audio: music 136.0BPM (to confirm, leaning stock library music) + 1 possible sound effects (unconfirmed signal candidates)
**Made with** (inferred, by duration): 3D render 51%, AI-generated video 47%, live action 1%, still image + pan/zoom 1%
**Remake**: 38 AI video shots + 31 3D render shots → 5 generation units, 5 Seedance 2.0 calls; live action 1 shot → 1 scene, 1 camera setup; still-image move / static frame 1 shot → rebuilt locally
**Real material to collect**: 1 shots (2% of the duration), list in `video/remake.md`

## Next steps

- No VLM ran: if you can see images, review first: `rea-video review <this dir>` → fill `review_answers.json` → `rea-video apply-review <this dir>`
- Remake: `rea-video remake <this dir>` does what can be done automatically and keeps the original elsewhere; `remake/status.md` says per shot what is left. Add incoming clips to `remake/mine.json` and run it again
- AI shots: prompts are in the generation units of `video/remake.md`; for automatic generation run `rea-video remake-plan` + `remake-run --dry-run` (paid: ask the user first)

## Open questions

- The VLM did not run (No VLM; live action / AI / 3D are told apart from pixel statistics only, so confidence is limited. An agent that can see images: run rea-vi…
- Shot #1 (0.0–0.3s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #2 (0.3–0.6s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #3 (0.6–1.0s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #4 (1.0–1.2s): 3D render at only 41% confidence, runner-up ai_video
- Shot #5 (1.2–1.5s): 3D render at only 39% confidence, runner-up ai_video
- Shot #6 (1.5–2.0s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- Shot #7 (2.0–2.9s): Live action / stop motion or AI, to confirm: no AIGC label; 24fps-source marks appear in AI video, stop motion and cinema-camera footage ali…
- 63 more, see the `flag` lines in `video/timeline.md`

## Map

Read this page first; for detail, open only the file you need. Each line is `path | ~tokens | what is in it · when to read it`; paths are relative to this directory.

```videomd-map
video/timeline.md | 3646 | Timeline: one line per shot · what a stretch says, which shots need review, how a shot was made
video/content.md | 87 | Content and structure · what it says, the narrative line, structure, the script
video/cast.md | 78 | Cast, scenes and props · reference images for characters, first-frame prompts
video/sound.md | 619 | Sound · voice, music, sound effects, beats and sources
video/look.md | 626 | Camera, lighting and editing · for filmed shots: framing, camera, lighting, kit
video/remake.md | 2831 | Remake plan · generation units, shoots, code builds, real material to collect, acting and emotion
video/shots/*.md | 397 | Per-shot detail, tokens per file on average · checking one shot: what is seen, the inference and its basis, prompts, frames
breakdown.json | 153881 | Full raw data · for programs; a model rarely needs it
shots/ | - | contact sheet, first and last frame of each shot · checking by eye
storyboard.jpg | - | storyboard of the whole video · the whole video at a glance
sfx/ | - | a clip of each sound effect · finding matching effects
audio.png | - | waveform and beat chart · seeing the rhythm
```

## How to read

- One shot per line: `#<n> start-end (s) | key value | …`. A key ending in `~` is the tools' inference; keys without it are visible on screen or measured directly.
- `story` job in the story and the point · `seen` what is on screen · `act` acting (emotion, strength, face) · `camera` camera move · `overlay` overlays · `made~` how it was made (inferred) · `material~` where the material came from (inferred) · `remake` remake route · `flag` needs a second look
- Full detail for a shot is in `video/shots/<n>.md` (e.g. `video/shots/07.md`).
- What is “seen” can be checked against the frames; what is “inferred” is the tools' and image readers' judgement, with the basis in each shot file. When they disagree, trust the frames.
