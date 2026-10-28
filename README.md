# Money Claude

**An AI co-founder operating system for Claude Code, plus a library of money-making playbooks distilled from public creators.**

Money Claude is a small, opinionated set of skills that make Claude behave less like an assistant and more like a co-founder: a partner that helps you decide what to build, pressure-tests ideas against real unit economics, kills losers fast, and turns scattered side-projects into a portfolio. It ships with a knowledge library distilled from dozens of public YouTube and TikTok creators, with the hype stripped out and the actual tactics kept.

This repo is intentionally generic. It carries no private business data. Bring your own ventures.

---

## What is in here

```
money-claude/
  skills/
    money-claude/            The co-founder operating system (the flagship skill)
    video-to-knowledge/      Turn any video into distilled, reusable notes (local, offline)
  knowledge/
    ai-content-playbooks.md   Distilled tactics from public creators (hype-flagged)
  assets/
    donate-solana.png         Support QR (see below)
```

### The skills

- **`money-claude`** - the operating system. Defines the co-founder stance, a six-point filter every idea passes through, a four-layer venture-portfolio model, kill/continue criteria, and a two-tier memory architecture (running state vs distilled knowledge). Load it at the start of any build session.
- **`video-to-knowledge`** - a fully local pipeline that turns a YouTube or TikTok link into clean, distilled notes: download audio (not the rate-limited caption endpoint), transcribe with `whisper.cpp` offline, then distil into themed notes with the hype flagged. No API keys, no cloud, no rate limits.

### The knowledge library

`knowledge/ai-content-playbooks.md` is a living distillation of what public creators actually teach about making money with AI: building and monetizing apps, AI ads and motion graphics with image/video models, short-form and faceless video, AI personas, offers and client acquisition. Every inflated revenue number is marked as hype; the reusable tactic underneath is kept.

> Honesty note: almost every "I made $X/month" video is a funnel for a paid tool, course, or community. The **tactics** are often solid; the **numbers** usually are not. This library separates the two. Treat it as a map, not a promise.

---

## Quickstart

Money Claude skills are [Claude Code](https://claude.com/claude-code) skills. To install:

```bash
git clone https://github.com/omgnoe/money-claude.git
mkdir -p ~/.claude/skills
cp -R money-claude/skills/* ~/.claude/skills/
```

Then in Claude Code, start a session and the skills activate on matching topics, or load one directly:

```
/money-claude
```

### Using `video-to-knowledge`

Requires `yt-dlp`, `ffmpeg`, and `whisper-cli` (whisper.cpp) plus a model such as `ggml-base.bin`:

```bash
brew install yt-dlp ffmpeg whisper-cpp
# download a model, e.g.:
curl -L -o ~/.cache/whisper-models/ggml-base.bin \
  https://huggingface.co/ggerganov/whisper.cpp/resolve/main/ggml-base.bin
```

Then ask Claude to run the pipeline on a link. The skill documents the exact steps.

---

## Philosophy

1. **Distribution beats the artifact.** Not the code, the site, the model, or the prompt wins. The system around it does. Prompt is 10 percent, harness is 90 percent.
2. **Separate hype from tactic.** Inflated numbers sell funnels. The tactics underneath are often real. Always split the two.
3. **Prove demand before you build.** A waitlist with a paid deposit beats a built product nobody asked for.
4. **Assets over services.** Services cap at your time. Build things you can sell more than once.
5. **Be honest.** No fake experts, no fabricated results, no health or income promises. Label AI content as AI.

---

## Support

If this saved you time, you can support the work with Solana:

**`EMTppBwvfX8b9w3jh9o21qW9JidmXRJ53yFs2y6q78PB`**

![Donate via Solana](assets/donate-solana.png)

Scan the QR with any Solana wallet. Thank you.

---

## Contributing

Issues and pull requests welcome, especially new distilled playbooks (with sources and honest hype-flagging) and improvements to the skills. Keep everything generic and free of private or personal data.

## License

MIT. See [LICENSE](LICENSE). Do what you want, no warranty. The knowledge library summarizes publicly posted content for educational purposes; credit stays with the original creators.
