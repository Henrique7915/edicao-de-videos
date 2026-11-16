---
videomd: 1
part: timeline
shots: 21
tokens: 1188
---

# Timeline

One shot per line: `#<n> start-end (s) | key value | …`. A key ending in `~` is the tools' inference; keys without it are visible on screen or measured directly.
`story` job in the story and the point · `seen` what is on screen · `act` acting (emotion, strength, face) · `camera` camera move · `overlay` overlays · `made~` how it was made (inferred) · `material~` where the material came from (inferred) · `remake` remake route · `flag` needs a second look
Full detail for a shot is in `video/shots/<n>.md` (e.g. `video/shots/07.md`).

```videomd-timeline
#01 0.0-1.8 | camera whole-frame zoom / pan | made~ still image + pan/zoom 83% · runner-up AI-generated video 10% | material~ to confirm; real or not, to confirm: pho… | remake local ffmpeg move
#02 1.8-3.8 | camera smooth move | overlay text | made~ AI-generated video 64% · runner-up live action 17% | material~ AI-generated | remake AI generation · G1 | flag to confirm
#03 3.8-5.5 | camera smooth move | overlay text | made~ 3D render 42% · runner-up AI-generated video 34% | material~ rendered by the creator | remake AI generation / 3D render · G1 | flag low confidence
#04 5.5-7.3 | camera static | transition fade through | made~ AI-generated video 53% · runner-up AI avatar (talking head) 22% | material~ AI-generated | remake AI generation · G1 | flag low confidence,to confirm
#05 7.3-9.2 | camera static (subject moves) | made~ AI-generated video 70% · runner-up AI avatar (talking head) 21% | material~ AI-generated | remake AI generation · G1 | flag to confirm
#06 9.2-11.1 | camera smooth move | overlay text | made~ AI-generated video 64% · runner-up live action 15% | material~ AI-generated | remake AI generation · G2 | flag to confirm
#07 11.1-13.1 | camera smooth move | overlay subtitle | made~ AI-generated video 70% · runner-up AI avatar (talking head) 10% | material~ AI-generated | remake AI generation · G2 | flag to confirm
#08 13.1-14.0 | camera smooth move | transition fade through | made~ AI-generated video 63% · runner-up live action 17% | material~ AI-generated | remake AI generation · G2 | flag to confirm
#09 14.0-14.7 | camera smooth move | transition fade through | made~ AI-generated video 64% · runner-up live action 16% | material~ AI-generated | remake AI generation · G2 | flag to confirm
#10 14.7-16.9 | camera smooth move | overlay subtitle | made~ AI-generated video 58% · runner-up live action 23% | material~ AI-generated | remake AI generation · G2 | flag low confidence,to confirm
#11 16.9-18.5 | camera smooth move | overlay subtitle | made~ live action 52% · runner-up AI-generated video 30% | material~ the user's real material (own footage or… | remake reshoot · S1 | flag low confidence
#12 18.5-19.8 | camera smooth move | made~ AI-generated video 64% · runner-up 3D render 10% | material~ AI-generated | remake AI generation · G3 | flag to confirm
#13 19.8-22.1 | camera smooth move | overlay text, subtitle | made~ live action 56% · runner-up AI-generated video 21% | material~ the user's real material (own footage or… | remake reshoot · S1 | flag low confidence
#14 22.1-22.6 | camera static | transition flash 0.1s | made~ AI-generated video 57% · runner-up static hold 26% | material~ AI-generated | remake AI generation · G4 | flag low confidence,to confirm
#15 22.6-22.8 | camera static | overlay subtitle, text | made~ static hold 91% · runner-up code / template render 4% | material~ to confirm; real or not, to confirm: pho… | remake static frame
#16 22.8-23.2 | camera static | transition flash 0.1s | made~ AI-generated video 52% · runner-up static hold 33% | material~ AI-generated | remake AI generation · G4 | flag low confidence,to confirm
#17 23.2-25.4 | camera smooth move | made~ AI-generated video 70% · runner-up AI avatar (talking head) 10% | material~ AI-generated | remake AI generation · G4 | flag to confirm
#18 25.4-25.8 | camera smooth move | transition jump cut | made~ AI-generated video 57% · runner-up live action 26% | material~ AI-generated | remake AI generation · G4 | flag low confidence,to confirm
#19 25.8-27.7 | camera smooth move | overlay text, subtitle | made~ AI-generated video 62% · runner-up live action 19% | material~ AI-generated | remake AI generation · G4 | flag to confirm
#20 27.7-29.5 | camera smooth move | overlay subtitle | made~ AI-generated video 59% · runner-up live action 21% | material~ AI-generated | remake AI generation · G4 | flag low confidence,to confirm
#21 29.5-35.1 | camera static | transition blur 0.6s | made~ code / template render 85% · runner-up AI-generated video 4% | material~ rendered by the creator | remake code render · Part 1
```
