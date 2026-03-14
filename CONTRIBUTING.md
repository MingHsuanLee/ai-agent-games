# Contributing to AI Agent Games

Thanks for wanting to add a game! This repo has one rule above all others: **every game must be built by an AI agent**.

## Game Format

Each game lives in its own folder under `games/`:

```
games/
└── your-game-name/
    ├── index.html   ← The entire game (self-contained)
    └── AGENT.md     ← Who built it and how
```

### index.html requirements

- **Single file** — no separate CSS/JS files, no CDN imports
- **No external dependencies** — everything inlined
- **Mobile-friendly** — touch controls or responsive layout
- **No secrets** — no API keys, tokens, or credentials anywhere
- **Playable** — it must actually work in a modern browser

### AGENT.md format

```markdown
- **Agent**: Claude Code (OpenClaw)
- **Model**: claude-sonnet-4-6
- **Built by**: @your-github-username
- **Prompt**: "Build a self-contained Snake game in a single HTML file with keyboard and touch controls."
- **Date**: 2026-03-14
```

All fields are required. The `Prompt` field should be the exact prompt you gave the agent.


## ⚖️ IP & Copyright Checklist

Before submitting, make sure your game passes this checklist:

- [ ] **Original game name** — Do not use names that are trademarked or closely associated with a specific commercial product. The following names are **blocked by CI** and will fail validation:
  - `tetris` / any variation
  - `breakout` / any variation
  - `flappy bird` / `flappy-bird` / any variation

- [ ] **No original assets** — All graphics, sounds, and assets must be original or properly licensed. Do not copy sprites, music, or other assets from commercial games.

- [ ] **Original code** — Your game must be an independent reimplementation. Do not copy or decompile source code from existing games.

- [ ] **No trademark use** — Do not use trademarked logos, characters, or branding in any form.

> **When in doubt, rename it.** Game mechanics are not copyrightable, but names and assets can be. A distinctive name (e.g. "Brick Breaker" instead of "Breakout", "Pixel Flap" instead of "Flappy Bird") is safer and more original.

> Games already in this repo (e.g. Minesweeper, Asteroids, Snake, 2048, Memory Match) have been reviewed for IP risk. New submissions are subject to CI validation and maintainer review.

## Pull Request Process

1. Fork this repo
2. Create a branch: `git checkout -b add-<game-name>`
3. Add your game folder
4. Push and open a PR against `main`
5. CI will validate your submission automatically:
   - `AGENT.md` present and correctly formatted
   - `index.html` is self-contained (no external URLs)
   - No secrets detected

PRs that pass CI are auto-merged. PRs that fail get a Telegram notification to the maintainer.

## Review criteria

- Does it run without errors in Chrome/Firefox?
- Is it actually fun/interesting?
- Is it meaningfully different from existing games?

## Code of Conduct

Be excellent to each other. Games should be appropriate for all ages unless the repo description explicitly says otherwise.

## Questions?

Open an [issue](../../issues) using the Game Proposal template to pitch a game idea first.
