# Setup notes

Application: `C:\AI-Projects\Breakout\index.html`

Documentation: `C:\AI-Projects\Breakout dok\`

## Architecture and resource limits

Vanilla HTML, CSS, Canvas 2D, JavaScript and Web Audio in one file. requestAnimationFrame renders at the display cadence (60 Hz on a 60 Hz display); physics uses a fixed 120 Hz timestep with at most six steps per frame and a 50 ms delta cap. Rendering is not a guarantee of identical FPS on all hardware.

Caps: 60 bricks, eight balls, 12 trail points per ball, 240 particles, 12 drops, 24 laser shots, canvas device pixel ratio at most two. Expired effects are removed. Audio oscillators stop after at most 250 ms. No unbounded caches or background workers. Verification runs one headless browser with a 256 MB Node heap cap; release CLI uses a 512 MB heap cap, well below the 8 GB budget.

## Release procedure

Initialize main; set repository-local Git author to mrskydiver2015-code / mrskydiver2015@gmail.com. Commit `feat: initial release of neon breakout`. Create public GitHub repository breakout-1976 using the portable gh CLI. Deploy static files with Vercel production and connect GitHub main for subsequent automatic production releases.

`.vercel` metadata and credentials are excluded from Git. No credentials are embedded in the game or documentation. Verification evidence and final URLs belong in this documentation directory.

## Verification

`verify.cjs` runs the exact local file and checks desktop/mobile/landscape bounds, touch steering, controls, sound preference persistence, gameplay collisions and terminal outcomes, effect limits, console errors and animation cadence. Headless mobile is emulation, not physical iOS certification. Actual results are in verification.json and RELEASE.md.
