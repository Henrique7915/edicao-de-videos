---
videomd: 1
part: remake
tokens: 4044
---

## Remake plan

### Step by step

This is a beat-synced montage. Do the steps in this order; the detail for each is in the matching subsection below.

1. **Music**: find a track at the same tempo and mood (source: to confirm, about 110 BPM, F major)
2. **Edit**: follow the order and lengths in the shot list; the original has 70 shots at 0.9s each
3. **Subtitles and styled text**: timing and style under “Packaging layer”
4. **Put it together and compare**: hand the shots you made to the agent; `rea-video remake` places them on the original timeline, keeps the original where yours are missing, and renders a side-by-side comparison with the original

**61 AI video shots + 7 3D render shots → 4 generation units, 4 Seedance 2.0 calls; code render / screen capture 2 shots → 1 code project (2 parts)**

### Generation units

- Grouping: consecutive shots share a call where they fit, ≤15s per call; a long stretch is cut at a scene change first
- Inputs: the source stretch, subtitles erased, is the reference video; the model follows its shots, camera and pacing
- Audio: the model can generate action sound effects and ambience along with the picture
- Packaging: the text label, styled text, sticker on the generated shots is post-production packaging: keep it out of the prompts (erased from source references) and lay it back on from the packaging timeline after generation

| Unit | Shots | Time | Length | Feed | Prompt |
|---|---|---|---|---|---|
| G1 | #1–#18 | 0.0–13.8s | 13.8s | reference video | draft |
| G2 | #19–#35 | 13.8–28.5s | 14.7s | reference video | draft |
| G3 | #36–#44, #46–#50 | 28.5–37.0s, 37.8–42.1s | 12.8s | reference video | draft |
| G4 | #51–#69 | 42.1–57.1s | 14.9s | reference video | draft |

**G1 · shots #1–#18 · 13.8s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 0.0–13.8s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (almost no lit / shadow edge), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
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

**G2 · shots #19–#35 · 14.7s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 13.8–28.5s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (almost no lit / shadow edge), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
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
```

**G3 · shots #36–#44, #46–#50 · 12.8s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 28.5–37.0s, 37.8–42.1s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

- these shots are separated by inserts in the cut: generate them together and put the inserts back in the edit

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (almost no lit / shadow edge), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
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
```

**G4 · shots #51–#69 · 14.9s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 42.1–57.1s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (almost no lit / shadow edge), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
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
Shot 19: (no description: write one in the image review)
```

### Code composition

One Remotion / HTML project rebuilt from the text tracks and layout (text and UI are 100% controllable; changing copy is a data change). An LLM can write this project directly.

Start with `rea-video code-remake <breakdown folder>`: it writes `code/spec.json` + `code/render.py` from each scene's sampled points / cut-out, motion and background glow below, matches each scene's amount and brightness to the original, renders `code/remake.mp4` and scores it. Work from that version (edit spec.json, swap the points, or port it to Remotion) instead of writing one from scratch.

- Part 1: shots #45 (37.0–37.8s)
- Part 2: shots #70 (57.1–60.1s)

Remake assets (all in the report folder; hand them over together with the data below to whoever writes the code, or to an LLM):
- `shots/shot_XXX_first.jpg` / `_last.jpg`: first / last frame of each shot at full size, for layout, type size and margins
- `shots/shot_XXX_strip.jpg`: key frames about every 0.5 s, to follow the animation
- `shots/shot_XXX_elements.jpg` and `_el_NN.jpg` / `_st_NN.jpg` / `_ly_NN.jpg`: full-size crop of every element once settled, numbered as in the motion timeline; redraw shapes from them, cut out icons, logos and illustrations that cannot be redrawn
- `packaging/overlays.ass`, `packaging/timeline.json`: timing, position and colour of the text

How to build the pictures (by the measured picture type):
- particles / point cloud: Three.js particle system (points sampled on the target shape, morph between shapes, bloom), rendered frame by frame with @remotion/three
- vector shapes: SVG shapes + interpolate() / spring() keyframes, positions and timing measured from the frame

Particle shots: what shape the particles form in each shot and how it moves decides whether the remake works; chapter cards, labels and counters go in an HTML layer on top. Build shot by shot from the table below, not one shared background.

| Shot | Time | Build | Picture | Camera | Colours | On-screen text |
|---|---|---|---|---|---|---|
| #45 | 37.0–37.8s | particles / point cloud | (to fill from the images: what the elements form and how they move) | picture drifts left | ground #030303 · #140a0d #26151c #3a2b2c #5c443c · drawn #473543 #581813 #88695e #e5cabd | — |
| #70 | 57.1–60.1s | vector shapes | (to fill from the images: what the elements form and how they move) | push in 4%/s, picture drifts up | ground #020005 · #000002 · drawn #cfbb9d #303327 #585b4f #e0ddda | — |

**Picture scenes** (a new scene whenever what is drawn moves or changes shape as a whole inside a shot. `frames/` holds first / middle / last full-size frames per scene, `scene_XX_layer.png` the drawn layer of the middle frame (background and text removed, alpha by how strongly it stands out), `frames/points/scene_XX.json` samples of that layer, one `x y r g b a` per row with x, y in 0–1. Place particles, trace lines or redraw shapes from these instead of guessing from a description. `track` in `frames/scenes.json` follows the layer's centre and spread over time)

| Scene | Shot | Time | Ground | Background glow | Drawn colours | Pieces | Area (x0 y0 x1 y1) | Motion |
|---|---|---|---|---|---|---|---|---|
| scene_01 | #45 | 37.0–37.8s | #070502 | #423430, centre (0.42, 0.31), radius 0.17 | #47242e #735f5b | 256 | 0.02 0.17 0.98 0.49 | zoom in 3%/s, pans (-3.7%, -0.1%)/s, points wander |

When built, score it with `rea-video compare original remake --scenes frames/scenes.json -o dir` (each side's drawn layer is taken against its own ground, so a new ground colour still compares) and fix the lowest-scoring scenes first, from `compare_worst.jpg`.

Per-shot motion timeline (measured: positions in % of frame width / height, colours sampled once the element settles; read together with the key-frame strip)

**Motion #45 37.0–37.8s · 3 events**

- Ground #030303; other main colours #140a0d #26151c #3a2b2c #5c443c; drawn layer #473543 #581813 #88695e #e5cabd
Element crops (numbers match the motion list below; L = the continuously moving layer mid-shot and at the end, S = elements that never move), full-size files in `shots/`:

- S1. never moves: shape / text block · x 0%–7%, y 10%–12% · #1f1629 · [crop](shots/shot_045_st_01.jpg)
- S2. never moves: shape / text block · x 42%–63%, y 10%–16% · #231417 · [crop](shots/shot_045_st_02.jpg)
- S3. never moves: shape / text block · x 32%–40%, y 12%–15% · #23151d · [crop](shots/shot_045_st_03.jpg)
- S4. never moves: shape / text block · x 18%–29%, y 13%–16% · #1f1329 · [crop](shots/shot_045_st_04.jpg)
- S5. never moves: shape / text block · x 85%–93%, y 15%–17% · #240a0c · [crop](shots/shot_045_st_05.jpg)
- S6. never moves: shape / text block · x 60%–69%, y 18%–21% · #241319 · [crop](shots/shot_045_st_06.jpg)
- S7. never moves: shape / text block · x 62%–71%, y 22%–25% · #24161e · [crop](shots/shot_045_st_07.jpg)
- S8. never moves: shape / text block · x 29%–38%, y 29%–31% · #2c0c0d · text “GRAN / GRANDE” · [crop](shots/shot_045_st_08.jpg)
- [crop L1](shots/shot_045_ly_01.jpg) [crop L2](shots/shot_045_ly_02.jpg) · Continuous layer: 8% of the frame moves through the whole shot (x 2%–100%, y 18%–66%), e.g. drifting gradients, particle flow, breathing glow
1. 37.02–37.09s · bottom left (x 0%–9%, y 94%–100%) · disappears, instant · #1f0908 · [crop](shots/shot_045_el_01.jpg)
2. 37.02–37.35s · bottom right (x 53%–91%, y 95%–100%) · changes, unfolds leftward (draw-on / grow / wipe), ease-in-out · #060302 · [crop](shots/shot_045_el_02.jpg)
3. 37.15–37.75s · bottom right (x 71%–98%, y 59%–81%) · appears, unfolds downward (draw-on / grow / wipe), ease-in · #190807 · [crop](shots/shot_045_el_03.jpg)

**Motion #70 57.1–60.1s · 3 events**

- Ground #020005; other main colours #000002; drawn layer #cfbb9d #303327 #585b4f #e0ddda
Element crops (numbers match the motion list below; L = the continuously moving layer mid-shot and at the end, S = elements that never move), full-size files in `shots/`:

- [crop L1](shots/shot_070_ly_01.jpg) [crop L2](shots/shot_070_ly_02.jpg) · Continuous layer: 88% of the frame moves through the whole shot (x 0%–100%, y 0%–100%), e.g. drifting gradients, particle flow, breathing glow
1. 57.12–57.39s · middle right (x 84%–100%, y 39%–41%) · disappears, linear · #554e52 · [crop](shots/shot_070_el_01.jpg)
2. 57.12–57.92s · bottom right (x 44%–100%, y 61%–100%) · disappears, moves rightward, ease-out · #7a6d5c · [crop](shots/shot_070_el_02.jpg)
3. 58.66–59.19s · bottom right (x 40%–98%, y 62%–100%) · disappears, moves rightward, ease-out · #252218 · [crop](shots/shot_070_el_03.jpg)
