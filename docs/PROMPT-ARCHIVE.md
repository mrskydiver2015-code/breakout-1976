# Prompt archive — 2026-10-07

## Autonomous Full-Pipeline Test: "Neon Breakout"

### Objective
Execute an end-to-end autonomous build, test, and release cycle for a new standalone game named "Neon Breakout" without human intervention, utilizing the pre-authenticated tools on this host.

### Execution Pipeline

1. **Filesystem Provisioning**:
   - Ensure the following two directories exist under `C:\AI-Projects\`:
     * `C:\AI-Projects\Breakout\` (Application root)
     * `C:\AI-Projects\Breakout dok\` (Documentation & prompt archive)

2. **Core Implementation (`C:\AI-Projects\Breakout\index.html`)**:
   - Create a self-contained, single-file application (`index.html`). Zero external CDN libraries or build tools.
   - **Stack**: Vanilla HTML5 Canvas + JavaScript + Web Audio API. Strictly bounded memory footprint adhering to an 8 GB RAM budget.
   - **Game Mechanics**:
     * Classic Breakout/Arkanoid gameplay with synthwave neon aesthetic (glowing bricks, ball trail, impact spark particles).
     * Power-ups (multi-ball, wide paddle, laser shot) appearing on brick destruction.
     * Dynamic speed ramp-up as bricks are cleared.
   - **State Persistence (`localStorage`)**:
     * All-time high score, total bricks broken, games won/lost, and mute/unmute state.
   - **Ergonomics & Controls**:
     * Desktop: Keyboard [A]/[D] or Left/Right arrow keys, plus mouse tracking.
     * Mobile Touch: Dedicated horizontal touch/drag zone spanning the bottom viewport (`touch-action: none`) leaving the playfield 100% visible.

3. **Documentation**:
   - Inside `C:\AI-Projects\Breakout dok\`, generate `README.md`, `SETUP-NOTES.md`, and `PROMPT-ARCHIVE.md`.

4. **Local Verification**:
   - Run the local headless browser check against `C:\AI-Projects\Breakout\index.html` to confirm 60 FPS animation loop, clean `localStorage` read/write, zero console errors, and viewport responsiveness.

5. **Remote Publication & CI/CD Linkage**:
   - Initialize Git in `C:\AI-Projects\Breakout\` and commit all files with message `feat: initial release of neon breakout`.
   - Using the portable GitHub CLI at `C:\AI-Projects\_tools\gh\gh.exe`, create a public repository named `breakout-1976` and push the `main` branch.
   - Deploy to Vercel production (`vercel --prod --yes`) and link the Git repository (`vercel git connect --yes`).

Report back the absolute local path, the public GitHub repository URL, and the verified live Vercel production URL.

## Applied task instructions

Use Git identity mrskydiver2015-code / mrskydiver2015@gmail.com, Conventional Commits, bounded local execution below 8 GB, existing authenticated tools, no extra conversational approvals for authorized routine work, and cross-device artifact delivery through the public game/repository. Global configuration remains outside task scope.
