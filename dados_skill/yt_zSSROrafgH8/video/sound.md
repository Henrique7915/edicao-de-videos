---
videomd: 1
part: sound
tokens: 767
---

## Sound

- loudness -14.3 dBFS, peak 0.0 dBFS; sound runs across cuts, laid in post as one bed (background changes 8.9dB at cuts vs 5.9dB within shots)
- Sources: Video type: music video / song (one sung track over the whole piece) → voice: TTS voice-over; music: AI-generated music (leaning, to confirm); SFX: added in post from an SFX library / editor (leaning, to confirm)

**Voice**

- 53% of the duration; pitch about 164.6Hz (gender unclear); sung
- Source: TTS voice-over (TTS voice-over 64%, human recording 27%, native dialogue from the AI video model 9%)
  - Voice and background sound run across cuts: the voice-over was laid on separately in post (TTS or a human voice-over)
- Remake: TTS voice-over: CapCut text-to-speech or another TTS tool, with a similar voice and pace

**Music**

- Tempo: 129.2 BPM (or 64.6/258.4); key A minor (confidence 0.928); 93% of the duration (0.0–34.5s); section changes at 27.5s; ending: cut off hard
- Cuts vs beat: 40% of cuts land on a beat (chance: about 28%)
- Source: to confirm (AI-generated music 38%, well-known song 33%, stock library music 29%)
  - Music runs wall-to-wall and the voice is sung (sustained-pitch ratio 0.37): looks like a song with vocals / music video, so an AI song is likely (no VLM; music-video prior, down-weighted)
  - The music is hard-cut at the end (still at full level when the video stops): typical of a trimmed existing track
  - How to confirm: Check the music tag on the original Douyin / Xiaohongshu / TikTok post: a song title → existing track; "original sound - @creator" → uploaded by the creator (for music videos, usually an AI song)
  - How to confirm: Run it through Shazam / ACRCloud or another song-ID service: a hit means an existing song
- Remake: The original track leans AI-generated: regenerate with Suno or similar (capsule-cinema UniversalMusicGenerationTool) matching style / BPM / key; for an MV, rewrite the lyrics for the new content too

**Sound effects** (4, all unconfirmed signal candidates)

| Time | Listen | Type | Description | On screen | Basis |
|---|---|---|---|---|---|
| 3.65s | [listen](sfx/sfx_01.wav) | whoosh | — | — | signal candidate (low confidence) |
| 24.60s | [listen](sfx/sfx_02.wav) | whoosh | — | — | signal candidate (low confidence) |
| 27.18s | [listen](sfx/sfx_03.wav) | pop | — | — | signal candidate (low confidence) |
| 27.67s | [listen](sfx/sfx_04.wav) | whoosh | — | cut | signal candidate (low confidence) |

- Source: added in post from an SFX library / editor (added in post from an SFX library / editor 57%, generated with the picture by the video model (native audio) 29%, location sound 14%)
  - Cartoon SFX in 3D / animated videos are also often procedurally synthesised or added from a library (e.g. the capsule-cinema plush recipe synthesises them)
- Remake: press “listen” to hear what each one is (cut from the original sound, so voice and music are in it), then take a similar effect from the editor's sound library and place it at that time; “On screen” says what each one lands on
