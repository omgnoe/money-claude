---
name: video-to-knowledge
description: Turn any YouTube or TikTok video into clean, distilled, reusable notes, fully local and offline. Use when the user shares one or many video links and wants the useful information extracted into notes (a "submemory"), or asks to transcribe/summarize videos at scale. Bypasses caption rate limits by downloading audio and transcribing with whisper.cpp locally. Triggers: "transcribe this video", "what is in this video", "take notes from these videos", "build a knowledge base from these links", "distill these videos".
---

# Video to Knowledge

Turn a pile of video links into a themed, hype-flagged knowledge base. Fully local: no API keys, no cloud, no caption rate limits.

## Why audio, not captions
Platforms hard rate-limit the subtitle/caption endpoint (HTTP 429) after a handful of requests from one IP. The audio/media endpoint is separate and not limited the same way. So: download audio, transcribe locally. This scales to dozens of videos.

## Requirements
- `yt-dlp` and `ffmpeg` (download + audio extraction)
- `whisper-cli` (whisper.cpp) and a model, e.g. `~/.cache/whisper-models/ggml-base.bin`
  - `base` is fast and good enough for note extraction. Use `large-v3` for accuracy when it matters.

```bash
brew install yt-dlp ffmpeg whisper-cpp
curl -L -o ~/.cache/whisper-models/ggml-base.bin \
  https://huggingface.co/ggerganov/whisper.cpp/resolve/main/ggml-base.bin
```

## Pipeline (per video)
1. **Download audio as 16kHz mono WAV** (small, whisper-ready):
   ```bash
   yt-dlp -f bestaudio/best -x --audio-format wav \
     --postprocessor-args "ffmpeg:-ar 16000 -ac 1 -y" --no-playlist \
     -o "audio/<id>.%(ext)s" "<url>"
   ```
2. **Transcribe locally** (plain text, no timestamps):
   ```bash
   whisper-cli -m ~/.cache/whisper-models/ggml-base.bin \
     -f "audio/<id>.wav" -otxt -of "transcripts/<id>" -nt -t 6
   rm "audio/<id>.wav"   # save disk
   ```
3. Repeat for every link. For many videos, run a loop in the background and skip any transcript that already exists (idempotent re-runs).

## Distilling into notes
Once transcripts exist, distil them into themed notes, not one note per video. For a large batch, fan out: give each theme (or each batch of ~8 transcripts) to a sub-agent that extracts only the actionable knowledge and writes one themed note. This keeps the main context clean.

Each note should carry:
- **Source** (title + id) and date.
- **What it is for** (which venture or use case).
- The distilled tactic, grouped by insight, not by video.
- A **hype flag**: mark inflated revenue numbers and affiliate-driven claims as hype; keep the tactic underneath.
- A **next step**: how to actually use it.

## Gotchas
- TikTok photo slideshows have no audio: whisper returns nothing. Read the slides visually in a browser instead.
- Some clips are music-only: skip them.
- IDs starting with `-` are read as flags by some shell tools; pass the full URL, or guard with `--`.
- The `base` model can garble non-English or fast speech; mark affected numbers as approximate, or re-run those with `large-v3`.
