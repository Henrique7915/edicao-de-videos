---
videomd: 1
part: remake
tokens: 2819
---

## Remake plan

### Step by step

This is a beat-synced montage. Do the steps in this order; the detail for each is in the matching subsection below.

1. **Music**: find a track at the same tempo and mood (source: to confirm, about 136 BPM, A minor)
2. **Collect material**: the real material in the picture (live footage) needs the original files, listed under “What to prepare”
3. **Edit**: follow the order and lengths in the shot list; the original has 71 shots at 0.8s each; 4 transitions under “Edit”
4. **Put it together and compare**: hand the shots you made to the agent; `rea-video remake` places them on the original timeline, keeps the original where yours are missing, and renders a side-by-side comparison with the original

**38 AI video shots + 31 3D render shots → 5 generation units, 5 Seedance 2.0 calls; live action 1 shot → 1 scene, 1 camera setup; still-image move / static frame 1 shot → rebuilt locally**

### Generation units

- Grouping: consecutive shots share a call where they fit, ≤15s per call; a long stretch is cut at a scene change first
- Inputs: the source stretch, subtitles erased, is the reference video; the model follows its shots, camera and pacing
- Audio: the model can generate action sound effects and ambience along with the picture

| Unit | Shots | Time | Length | Feed | Prompt |
|---|---|---|---|---|---|
| G1 | #1–#15 | 0.0–12.9s | 12.9s | reference video | draft |
| G2 | #16–#26 | 12.9–20.8s | 7.9s | reference video | draft |
| G3 | #28–#36, #38–#48 | 21.7–28.3s, 28.8–35.9s | 13.7s | reference video | draft |
| G4 | #49–#64 | 35.9–50.1s | 14.2s | reference video | draft |
| G5 | #65–#71 | 50.1–59.0s | 8.9s | reference video | draft |

**G1 · shots #1–#15 · 12.9s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 0.0–12.9s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
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
```

**G2 · shots #16–#26 · 7.9s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 12.9–20.8s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
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

**G3 · shots #28–#36, #38–#48 · 13.7s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 21.7–28.3s, 28.8–35.9s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

- these shots are separated by inserts in the cut: generate them together and put the inserts back in the edit

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
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
Shot 20: (no description: write one in the image review)
```

**G4 · shots #49–#64 · 14.2s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 35.9–50.1s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
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
```

**G5 · shots #65–#71 · 8.9s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 50.1–59.0s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), cool (daylight / cool-white LED), background clearly blurred (shallow depth of field / portrait mode). No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
Shot 5: (no description: write one in the image review)
Shot 6: (no description: write one in the image review)
Shot 7: (no description: write one in the image review)
```

### Shooting scenes

Shoot every shot of one scene before moving to the next; within a scene, shoot the wider sizes first and the close-ups last so the lighting is set only once. Leave about 1s of handle at both ends of every take.

**S1**: shots #27 (0.88s on screen)
- Lighting: night / low-light ambient, no dedicated fill, key light frame right, three-quarter front, cool (daylight / cool-white LED)
- Setup medium shot · moving camera (gimbal / handheld pan) · push-in: shots #27, 0.88s on screen, shoot about 2.9s

### Local rebuild

- #37 still image + pan/zoom 0.5s: one image + the measured zoom / pan parameters, rendered straight from ffmpeg

### Real material in the picture (the original files are needed)

1 shots, 0.88s (2%) contain real material (screen recordings, screenshots, photos, embedded video); a model cannot stand in for them:

- **live footage (own footage or a film / drama clip, confirm by looking)** (whole frame): shots #27, 0.9s in all
