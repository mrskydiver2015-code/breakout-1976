# Neon Breakout release — 2026-10-07

- Game: https://breakout-1976.vercel.app
- Public source and documentation: https://github.com/mrskydiver2015-code/breakout-1976
- Local application: `C:\AI-Projects\Breakout\index.html`
- Local documentation: `C:\AI-Projects\Breakout dok\`
- Initial commit: `8956b13e18da18322d4df5a0817e481ba1ef1aae`
- Initial commit message: `feat: initial release of neon breakout`
- Git author: mrskydiver2015-code / mrskydiver2015@gmail.com
- Vercel project: breakout-1976 / prj_GSBQA12tuw28xY0877Mwc9grecup
- Initial deployment: dpl_9nXKRVZS1Ron1HG4jvWoxu7ZsHed — READY, production
- Stack: static single-file HTML / Canvas / JavaScript / Web Audio; no installation or build step

## Evidence

Local exact-file check: 25 passed assertions, no console errors. Live unauthenticated HTTPS check: 15 passed assertions, no console errors. Both measured a median 16.7 ms frame interval (59.88 FPS); p95 was 33.4 ms, so this is observed median cadence, not a guarantee of every frame meeting 16.7 ms.

Viewports: 1440×900, 393×852, 320×568, 852×393. All kept the full canvas within the viewport and above the dedicated drag zone. Start, launch, pause/resume, drag steering, localStorage round trip, and mute persistence passed on the released page. Deterministic mechanic checks used a separate instrumented copy: multiball/cap, wide paddle, laser, brick collision and counter update, speed ramp, wins, losses, particle cap and bounded effects.

`verification.json` and `live-verification.json` contain the raw browser results. Mobile checks are headless emulation. Memory is bounded by effect/ball limits and Node heap limits; a complete operating-system peak RSS measurement was not part of these checks.

## Git integration

Vercel reported `Connected` for the requested GitHub repository during project creation. The explicit `vercel git connect --yes` reported that this same repository was already connected. Documentation and CLI-generated ignore rules were then committed and pushed to main to exercise automatic deployment. Subsequent deployment evidence is recorded in CI-VERIFICATION.txt.

No changes were made to global Git identity, Codex configuration, permission settings, browser settings or stored lessons. Vercel's generated local environment file is ignored by Git.
