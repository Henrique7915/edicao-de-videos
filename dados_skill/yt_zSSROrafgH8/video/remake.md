---
videomd: 1
part: remake
tokens: 2918
---

## Remake plan

### Step by step

This is a AI music video. Do the steps in this order; the detail for each is in the matching subsection below.

1. **Music**: find a track at the same tempo and mood (source: to confirm, about 129 BPM, A minor)
2. **Write the content**: one picture of your own for each of the 21 shots in the shot list
3. **Collect material**: the real material in the picture (live footage) needs the original files, listed under “What to prepare”
4. **AI shots**: 16 shots (24 s) to make with a video model. Pick the model first: tell the agent which one and it plans the stretches, inputs and prompts for it (`rea-video plan <folder> --model <model>`)
5. **Live shots**: 2 shots to film yourself; camera and light under “Shoot” below
6. **Stills with moves**: swap in your images; `rea-video remake` moves them the way the original does
7. **Edit**: follow the order and lengths in the shot list; the original has 21 shots at 1.7s each; 7 transitions under “Edit”
8. **Sound effects**: 4; place similar ones from a library at the times under “Sound”
9. **Put it together and compare**: hand the shots you made to the agent; `rea-video remake` places them on the original timeline, keeps the original where yours are missing, and renders a side-by-side comparison with the original

**15 AI video shots + 1 3D render shot → 4 generation units, 4 Seedance 2.0 calls; live action 2 shots → 1 scene, 1 camera setup; code render / screen capture 1 shot → 1 code project; still-image move / static frame 2 shots → rebuilt locally**

### Generation units

- Grouping: consecutive shots share a call where they fit, ≤15s per call; a long stretch is cut at a scene change first
- Inputs: the source stretch, subtitles erased, is the reference video; the model follows its shots, camera and pacing
- Audio: the model can generate action sound effects and ambience along with the picture; voice-over is better done as separate TTS and mixed in, so copy and timing stay editable

| Unit | Shots | Time | Length | Feed | Prompt |
|---|---|---|---|---|---|
| G1 | #2–#5 | 1.8–9.2s | 7.4s | reference video | draft |
| G2 | #6–#10 | 9.2–16.9s | 7.6s | reference video | draft |
| G3 | #12 | 18.5–19.8s | 1.3s | reference video | draft |
| G4 | #14, #16–#20 | 22.1–22.6s, 22.8–29.5s | 7.2s | reference video | draft |

**G1 · shots #2–#5 · 7.4s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 1.8–9.2s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background slightly soft. No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
```

**G2 · shots #6–#10 · 7.6s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 9.2–16.9s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background slightly soft. No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
Shot 5: (no description: write one in the image review)
```

**G3 · shots #12 · 1.3s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 18.5–19.8s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background slightly soft. No subtitles, captions or watermarks in the picture.
(no description: write one in the image review)
```

**G4 · shots #14, #16–#20 · 7.2s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 22.1–22.6s, 22.8–29.5s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

- these shots are separated by inserts in the cut: generate them together and put the inserts back in the edit

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background slightly soft. No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
Shot 5: (no description: write one in the image review)
Shot 6: (no description: write one in the image review)
```

### Shooting scenes

Shoot every shot of one scene before moving to the next; within a scene, shoot the wider sizes first and the close-ups last so the lighting is set only once. Leave about 1s of handle at both ends of every take.

**S1**: shots #11, #13 (3.97s on screen)
- Lighting: night / low-light ambient, no dedicated fill, key light frame right, three-quarter front, cool (daylight / cool-white LED)
- Setup medium close-up · moving camera (gimbal / handheld pan) · pan / track/push-in: shots #11, #13, 3.97s on screen, shoot about 8.0s

### Code composition

One Remotion / HTML project rebuilt from the text tracks and layout (text and UI are 100% controllable; changing copy is a data change). An LLM can write this project directly.

Start with `rea-video code-remake <breakdown folder>`: it writes `code/spec.json` + `code/render.py` from each scene's sampled points / cut-out, motion and background glow below, matches each scene's amount and brightness to the original, renders `code/remake.mp4` and scores it. Work from that version (edit spec.json, swap the points, or port it to Remotion) instead of writing one from scratch.

- Part 1: shots #21 (29.5–35.1s)

Remake assets (all in the report folder; hand them over together with the data below to whoever writes the code, or to an LLM):
- `shots/shot_XXX_first.jpg` / `_last.jpg`: first / last frame of each shot at full size, for layout, type size and margins
- `shots/shot_XXX_strip.jpg`: key frames about every 0.5 s, to follow the animation
- `shots/shot_XXX_elements.jpg` and `_el_NN.jpg` / `_st_NN.jpg` / `_ly_NN.jpg`: full-size crop of every element once settled, numbered as in the motion timeline; redraw shapes from them, cut out icons, logos and illustrations that cannot be redrawn
- `packaging/overlays.ass`, `packaging/timeline.json`: timing, position and colour of the text

How to build the pictures (by the measured picture type):
- glow on dark: Dark ground + gradient-filled text / lines, glow from two stacked CSS drop-shadows or an SVG feGaussianBlur, brightness breathing per frame

| Shot | Time | Build | Picture | Camera | Colours | On-screen text |
|---|---|---|---|---|---|---|
| #21 | 29.5–35.1s | glow on dark | (to fill from the images: what the elements form and how they move) | static | ground #000002 · #752513 #c5a881 #c09763 #8e5033 · drawn #f9d2b0 #f7bb89 #c4976e | FOLKS |

**Picture scenes** (a new scene whenever what is drawn moves or changes shape as a whole inside a shot. `frames/` holds first / middle / last full-size frames per scene, `scene_XX_layer.png` the drawn layer of the middle frame (background and text removed, alpha by how strongly it stands out), `frames/points/scene_XX.json` samples of that layer, one `x y r g b a` per row with x, y in 0–1. Place particles, trace lines or redraw shapes from these instead of guessing from a description. `track` in `frames/scenes.json` follows the layer's centre and spread over time)

| Scene | Shot | Time | Ground | Background glow | Drawn colours | Pieces | Area (x0 y0 x1 y1) | Motion |
|---|---|---|---|---|---|---|---|---|
| scene_01 | #21 | 29.5–32.5s | #000000 | #c9906c, centre (0.50, 0.50), radius 0.32 | #f3d3b5 #dfb88e #907f6d | 3 | 0.07 0.37 0.91 0.58 | near still |
| scene_02 | #21 | 32.5–35.1s | #000000 | #c68664, centre (0.48, 0.50), radius 0.32 | #f2d3b5 #d9b893 #867765 | 2 | 0.07 0.56 0.92 0.57 | morphs in from the last scene |

When built, score it with `rea-video compare original remake --scenes frames/scenes.json -o dir` (each side's drawn layer is taken against its own ground, so a new ground colour still compares) and fix the lowest-scoring scenes first, from `compare_worst.jpg`.

Per-shot motion timeline (measured: positions in % of frame width / height, colours sampled once the element settles; read together with the key-frame strip)

**Motion #21 29.5–35.1s (blur in) · 1 events**

- Ground #000002; other main colours #752513 #c5a881 #c09763 #8e5033; drawn layer #f9d2b0 #f7bb89 #c4976e
Element crops (numbers match the motion list below; L = the continuously moving layer mid-shot and at the end, S = elements that never move), full-size files in `shots/`:

1. 34.65–34.98s · middle (x 7%–93%, y 36%–64%) · disappears, linear · #f1b984 · text “FOLKS / Nao teme / Nao temena!” · [crop](shots/shot_021_el_01.jpg)

### Local rebuild

- #1 still image + pan/zoom 1.8s; #15 static hold 0.2s: one image + the measured zoom / pan parameters, rendered straight from ffmpeg

### Real material in the picture (the original files are needed)

2 shots, 3.97s (11%) contain real material (screen recordings, screenshots, photos, embedded video); a model cannot stand in for them:

- **live footage (own footage or a film / drama clip, confirm by looking)** (whole frame): shots #11, #13, 4.0s in all
