# Speaker Timer

A stage-ready timer for talks, panels and events. One file, no build step, no dependencies:
open `index.html` or host it anywhere (GitHub Pages works).

## Highlights

- **Several timers at once**, each with a label, count down or count up, and a chain of segments
  (Intro, Keynote, Q&A...) that advance automatically.
- **Traffic-light stage display**: green, yellow and red at thresholds you set per segment, then a
  flashing overtime counter. Full screen (`F`) or in a separate stage window for a projector.
- **Message to the speaker**, cue notes per segment, time-of-day clock, end times, spotlight one timer.
- **Chimes** (soft, bell, digital, gong, air horn, sad trombone, applause) and optional **spoken alerts**.
- **Safety nets**: refresh recovery, undo, run log with CSV export, backup and restore as JSON.
- **Scheduling**: auto-start at a time of day, segments that end at a fixed clock time, repeating chains.
- **Looks**: Paper, Ink and High-contrast themes, background pictures, colour-blind-safe palette, digit fonts.
- **Ridiculousness dial (0 to 11)**: mood emoji, a racing mascot (the rocket crashes in overtime), a heartbeat and
  ticks through the last ten seconds, an overtime meltdown (shaking that worsens every minute, falling emoji, police
  lights), confetti cannons when a segment finishes on time, air horn / sad trombone / applause chimes and a party mode.
  Level 0 turns every effect off.

## Keyboard

| Key | Action |
| --- | --- |
| `Space` | start / pause all timers |
| `1`-`9` | start / pause that timer |
| `R` / `Shift+R` | reset the selected timer / reset all |
| `N` `P` | next / previous segment of the selected timer |
| `Up` `Down` | add / remove a minute on the selected timer |
| `U` or `Ctrl+Z` | undo the last reset or skip |
| `S` | spotlight the selected timer on the stage |
| `F` / `Esc` | full-screen stage / leave it |
| `M` | mute |
| `K` / `H` / `D` | confetti cannon / air horn / party mode |
| `C` | clear the message on stage |
| `PageDown` `PageUp` `.` | in full screen: next / previous / pause (presentation clickers) |

## Notes

- Everything is stored in your browser only (localStorage and IndexedDB). Use **Backup** to move a setup
  between computers.
- The separate stage window talks to the control window through a `BroadcastChannel`, so both must be open in
  the same browser. It works from a hosted page (`https://`) and from `localhost`; some browsers block it for
  files opened straight from disk.
- Timers are measured from timestamps rather than ticks, so a hidden or throttled tab never drifts.
- Audio and speech only start after you click or press a key on the page (a browser rule).
