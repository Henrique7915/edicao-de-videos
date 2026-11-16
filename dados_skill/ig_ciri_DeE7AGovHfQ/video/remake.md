---
videomd: 1
part: remake
tokens: 2456
---

## Remake plan

### Step by step

This is a short AI clip (pets / spectacle / single scene). Do the steps in this order; the detail for each is in the matching subsection below.

1. **Write the content**: one picture of your own for each of the 34 shots in the shot list
2. **Collect material**: the real material in the picture (live footage) needs the original files, listed under “What to prepare”
3. **AI shots**: 13 shots (23 s) to make with a video model. Pick the model first: tell the agent which one and it plans the stretches, inputs and prompts for it (`rea-video plan <folder> --model <model>`)
4. **Live shots**: 21 shots to film yourself; camera and light under “Shoot” below
5. **Voice**: the original is TTS voice-over; record it yourself or use TTS
6. **Edit**: follow the order and lengths in the shot list; the original has 34 shots at 0.9s each; 3 transitions under “Edit”
7. **Music**: find a track at the same tempo and mood (source: to confirm, about 178 BPM, D minor)
8. **Put it together and compare**: hand the shots you made to the agent; `rea-video remake` places them on the original timeline, keeps the original where yours are missing, and renders a side-by-side comparison with the original

**3 3D render shots + 10 AI video shots → 6 generation units, 6 Seedance 2.0 calls; live action 21 shots → 3 scenes, 6 camera setups**

### Generation units

- Grouping: consecutive shots share a call where they fit, ≤15s per call; a long stretch is cut at a scene change first
- Inputs: the source stretch, subtitles erased, is the reference video; the model follows its shots, camera and pacing
- Audio: the model can generate action sound effects and ambience along with the picture; voice-over is better done as separate TTS and mixed in, so copy and timing stay editable

| Unit | Shots | Time | Length | Feed | Prompt |
|---|---|---|---|---|---|
| G1 | #2 | 0.2–0.4s | 0.2s | reference video | draft |
| G2 | #5 | 0.7–0.9s | 0.2s | reference video | draft |
| G3 | #12 | 2.6–3.7s | 1.0s | reference video | draft |
| G4 | #14–#20 | 4.4–17.5s | 13.1s | reference video | draft |
| G5 | #26, #27 | 19.7–22.1s | 2.4s | reference video | draft |
| G6 | #34 | 24.4–30.4s | 5.9s | reference video | draft |

**G1 · shots #2 · 0.2s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 0.2–0.4s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), neutral (about 5000K), background slightly soft. No subtitles, captions or watermarks in the picture.
(no description: write one in the image review)
```

**G2 · shots #5 · 0.2s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 0.7–0.9s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), neutral (about 5000K), background slightly soft. No subtitles, captions or watermarks in the picture.
(no description: write one in the image review)
```

**G3 · shots #12 · 1.0s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 2.6–3.7s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), neutral (about 5000K), background slightly soft. No subtitles, captions or watermarks in the picture.
(no description: write one in the image review)
```

**G4 · shots #14–#20 · 13.1s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 4.4–17.5s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), neutral (about 5000K), background slightly soft. No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
Shot 3: (no description: write one in the image review)
Shot 4: (no description: write one in the image review)
Shot 5: (no description: write one in the image review)
Shot 6: (no description: write one in the image review)
Shot 7: (no description: write one in the image review)
```

**G5 · shots #26, #27 · 2.4s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 19.7–22.1s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), neutral (about 5000K), background slightly soft. No subtitles, captions or watermarks in the picture.
Shot 1: (no description: write one in the image review)
Shot 2: (no description: write one in the image review)
```

**G6 · shots #34 · 5.9s · remix of the source**

| Input | Needed | From | Why |
|---|---|---|---|
| text prompt | yes | see the prompt below | final version in this model's format (remake/prompts.json) |
| reference video | yes | `@视频1` source 24.4–30.4s (subtitles and stickers erased) | the model copies its cuts, camera and action and makes the stretch in one go |

Draft prompt (generic; rewrite it in Seedance 2.0's format into remake/prompts.json before generating):

```text
@视频1 is the source: follow its shots (count, length, size, camera, movement, action and cutting rhythm) and change only what is written below. Vertical 9:16; night / low-light ambient, no dedicated fill, soft light (wide lit-to-shadow ramp), neutral (about 5000K), background slightly soft. No subtitles, captions or watermarks in the picture.
(no description: write one in the image review)
```

### Shooting scenes

Shoot every shot of one scene before moving to the next; within a scene, shoot the wider sizes first and the close-ups last so the lighting is set only once. Leave about 1s of handle at both ends of every take.

**S1**: shots #1 (0.23s on screen)
- Lighting: three-quarter key + fill (standard set-up), key light frame left, three-quarter front, warm (about 3000–4000K)
- Setup close-up · moving camera (gimbal / handheld pan) · push-in: shots #1, 0.23s on screen, shoot about 2.2s

**S2**: shots #3, #4, #8–#11, #13, #21–#25, #28–#33 (6.67s on screen)
- Setup medium shot · moving camera (gimbal / handheld pan) · pull-out/push-in: shots #8, #11, #28, 1.37s on screen, shoot about 7.4s
- Setup medium close-up · moving camera (gimbal / handheld pan) · pull-out/push-in: shots #3, #4, #9, #10, #24, #25, #30, #32, 2.47s on screen, shoot about 18.5s
- Setup close-up · moving camera (gimbal / handheld pan) · push-in: shots #13, #21–#23, #29, #31, #33, 2.83s on screen, shoot about 16.8s

**S3**: shots #6, #7 (0.67s on screen)
- Lighting: backlit / background brighter than subject, key light frontal, warm (about 3000–4000K)
- Setup medium shot · moving camera (gimbal / handheld pan) · push-in: shots #6, 0.13s on screen, shoot about 2.1s
- Setup close-up · moving camera (gimbal / handheld pan) · push-in: shots #7, 0.53s on screen, shoot about 2.5s

### Real material in the picture (the original files are needed)

21 shots, 7.57s (25%) contain real material (screen recordings, screenshots, photos, embedded video); a model cannot stand in for them:

- **live footage (own footage or a film / drama clip, confirm by looking)** (whole frame): shots #1, #3, #4, #6–#11, #13, #21–#25, #28–#33, 7.6s in all
