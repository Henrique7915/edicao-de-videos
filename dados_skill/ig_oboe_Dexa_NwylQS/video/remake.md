---
videomd: 1
part: remake
tokens: 3169
---

## Remake plan

### Step by step

This is a beat-synced montage. Do the steps in this order; the detail for each is in the matching subsection below.

1. **Music**: find a track at the same tempo and mood (source: to confirm, about 129 BPM, C major)
2. **Edit**: follow the order and lengths in the shot list; the original has 60 shots at 1.0s each; 24 transitions under “Edit”
3. **Put it together and compare**: hand the shots you made to the agent; `rea-video remake` places them on the original timeline, keeps the original where yours are missing, and renders a side-by-side comparison with the original

**24 3D render shots + 29 AI video shots → 4 generation units, 4 Seedance 2.0 calls; code render / screen capture 2 shots → 1 code project (2 parts); still-image move / static frame 5 shots → rebuilt locally**

### Generation units

- Grouping: consecutive shots share a call where they fit, ≤15s per call; a long stretch is cut at a scene change first
- Inputs: the source stretch, subtitles erased, is the reference video; the model follows its shots, camera and pacing
- Audio: the model can generate action sound effects and ambience along with the picture

| Unit | Shots | Time | Length | Feed | Prompt |
|---|---|---|---|---|---|
| G1 | #1–#4, #7, #9–#12, #14–#22 | 0.0–3.3s, 6.3–7.0s, 7.2–9.4s, 10.4–19.1s | 15.0s | reference video | draft |
| G2 | #23–#34 | 19.1–33.5s | 14.3s | reference video | draft |
| G3 | #35–#45 | 33.5–46.3s | 12.8s | reference video | draft |
| G4 | #47–#54, #56–#59 | 46.8–54.9s, 55.3–59.8s | 12.6s | reference video | draft |

**G1 · shots #1–#4, #7, #9–#12, #14–#22 · 15.0s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 0.0–3.3s, 6.3–7.0s, 7.2–9.4s, 10.4–19.1s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

- these shots are separated by inserts in the cut: generate them together and put the inserts back in the edit

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), warm (about 3000–4000K), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
Shot 5: (no description: write one in the image review)
Shot 6: (no description: write one in the image review)
Shot 7: (no description: write one in the image review)
Shot 8: (no description: write one in the image review)
Shot 9: (no description: write one in the image review)
Shot 10: (no description: write one in the image review)
Shot 11: (no description: write one in the image review)
Shot 12: (no description: write one in the image review)
Shot 13: (no description: write one in the image review)
Shot 14: (no description: write one in the image review)
Shot 15: (no description: write one in the image review)
Shot 16: (no description: write one in the image review)
Shot 17: (no description: write one in the image review)
Shot 18: (no description: write one in the image review)
```

**G2 · shots #23–#34 · 14.3s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 19.1–33.5s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), warm (about 3000–4000K), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
Shot 5: (no description: write one in the image review)
Shot 6: (no description: write one in the image review)
Shot 7: (no description: write one in the image review)
Shot 8: (no description: write one in the image review)
Shot 9: (no description: write one in the image review)
Shot 10: (no description: write one in the image review)
Shot 11: (no description: write one in the image review)
Shot 12: (no description: write one in the image review)
```

**G3 · shots #35–#45 · 12.8s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 33.5–46.3s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), warm (about 3000–4000K), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
Shot 5: (no description: write one in the image review)
Shot 6: (no description: write one in the image review)
Shot 7: (no description: write one in the image review)
Shot 8: (no description: write one in the image review)
Shot 9: (no description: write one in the image review)
Shot 10: (no description: write one in the image review)
Shot 11: (no description: write one in the image review)
```

**G4 · shots #47–#54, #56–#59 · 12.6s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 46.8–54.9s, 55.3–59.8s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

- these shots are separated by inserts in the cut: generate them together and put the inserts back in the edit

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), warm (about 3000–4000K), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
Shot 5: (no description: write one in the image review)
Shot 6: (no description: write one in the image review)
Shot 7: (no description: write one in the image review)
Shot 8: (no description: write one in the image review)
Shot 9: (no description: write one in the image review)
Shot 10: (no description: write one in the image review)
Shot 11: (no description: write one in the image review)
Shot 12: (no description: write one in the image review)
```

### Code composition

One Remotion / HTML project rebuilt from the text tracks and layout (text and UI are 100% controllable; changing copy is a data change). An LLM can write this project directly.

Start with `rea-video code-remake <breakdown folder>`: it writes `code/spec.json` + `code/render.py` from each scene's sampled points / cut-out, motion and background glow below, matches each scene's amount and brightness to the original, renders `code/remake.mp4` and scores it. Work from that version (edit spec.json, swap the points, or port it to Remotion) instead of writing one from scratch.

- Part 1: shots #8 (7.0–7.2s)
- Part 2: shots #60 (59.8–60.6s)

Remake assets (all in the report folder; hand them over together with the data below to whoever writes the code, or to an LLM):
- `shots/shot_XXX_first.jpg` / `_last.jpg`: first / last frame of each shot at full size, for layout, type size and margins
- `shots/shot_XXX_strip.jpg`: key frames about every 0.5 s, to follow the animation
- `shots/shot_XXX_elements.jpg` and `_el_NN.jpg` / `_st_NN.jpg` / `_ly_NN.jpg`: full-size crop of every element once settled, numbered as in the motion timeline; redraw shapes from them, cut out icons, logos and illustrations that cannot be redrawn
- `packaging/overlays.ass`, `packaging/timeline.json`: timing, position and colour of the text

How to build the pictures (by the measured picture type):
- vector shapes: SVG shapes + interpolate() / spring() keyframes, positions and timing measured from the frame
- glow on dark: Dark ground + gradient-filled text / lines, glow from two stacked CSS drop-shadows or an SVG feGaussianBlur, brightness breathing per frame

| Shot | Time | Build | Picture | Camera | Colours | On-screen text |
|---|---|---|---|---|---|---|
| #8 | 7.0–7.2s | vector shapes | (to fill from the images: what the elements form and how they move) | static | ground #000204 · #7a2d05 #2a2c27 #404c42 #706848 · drawn #9a875f #954005 #060204 #327aa3 | maior Oboe da historia |
| #60 | 59.8–60.6s | glow on dark | (to fill from the images: what the elements form and how they move) | static | ground #000000 · #000002 | — |

**Picture scenes** (a new scene whenever what is drawn moves or changes shape as a whole inside a shot. `frames/` holds first / middle / last full-size frames per scene, `scene_XX_layer.png` the drawn layer of the middle frame (background and text removed, alpha by how strongly it stands out), `frames/points/scene_XX.json` samples of that layer, one `x y r g b a` per row with x, y in 0–1. Place particles, trace lines or redraw shapes from these instead of guessing from a description. `track` in `frames/scenes.json` follows the layer's centre and spread over time)

| Scene | Shot | Time | Ground | Background glow | Drawn colours | Pieces | Area (x0 y0 x1 y1) | Motion |
|---|---|---|---|---|---|---|---|---|
| scene_01 | #8 | 7.0–7.2s | #0d1407 | #6a735c, centre (0.56, 0.42), radius 0.48 | #833207 #50553a #063869 | 28 | 0.01 0.02 0.99 0.78 | — |
| scene_02 | #60 | 59.8–60.6s | #000000 | — | — | — | — | — |

When built, score it with `rea-video compare original remake --scenes frames/scenes.json -o dir` (each side's drawn layer is taken against its own ground, so a new ground colour still compares) and fix the lowest-scoring scenes first, from `compare_worst.jpg`.

Per-shot motion timeline (measured: positions in % of frame width / height, colours sampled once the element settles; read together with the key-frame strip)

**Motion #8 7.0–7.2s · 0 events**

- Ground #000204; other main colours #7a2d05 #2a2c27 #404c42 #706848; drawn layer #9a875f #954005 #060204 #327aa3
- No element motion measured (still picture or only slight changes)

**Motion #60 59.8–60.6s · 0 events**

- Ground #000000; other main colours #000002
- No element motion measured (still picture or only slight changes)

### Local rebuild

- #5 still image + pan/zoom 1.6s; #6 still image + pan/zoom 1.5s; #13 still image + pan/zoom 1.0s; #46 still image + pan/zoom 0.5s; #55 still image + pan/zoom 0.4s: one image + the measured zoom / pan parameters, rendered straight from ffmpeg
