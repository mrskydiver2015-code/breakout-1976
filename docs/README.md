# Neon Breakout

A standalone synthwave Breakout game. Open `C:\AI-Projects\Breakout\index.html` in a modern browser, or visit the production URL recorded in RELEASE.md.

Clear 60 bricks with three lives. Catch M for multiball (maximum eight balls), W for a wide paddle (14 seconds), or L for automatic laser fire (12 seconds). Ball speed rises as bricks are cleared.

Move with A/D, arrow keys, mouse, or the separate bottom drag zone. Space or a tap launches the ball. P and the Pause button pause/resume. Sound is synthesized after a user gesture; Sound on/off persists.

Records stored under `neon-breakout-v1`: all-time high score, total bricks broken, wins, losses, and muted state. Records are local to each browser/origin; direct file and HTTPS play may have separate records. Storage failure does not stop gameplay.

No runtime dependencies, CDN, assets, build tools, or paid services. Canvas uses logical 800×640 coordinates and scales within the visible viewport. The bottom touch zone remains outside the playfield.
