# Slaps

A two-player face-to-face card game built for mobile browsers. Place your phone flat between two players — each player taps their side of the screen to slap when the dealt card matches the call rank.

**▶ Play now: [wsamuelw.github.io/slaps](https://wsamuelw.github.io/slaps/)**

<img width="2796" height="1290" alt="screenshot" src="https://github.com/user-attachments/assets/3ddfa280-775b-44b6-b840-bc570bd03064" />

## How to Play

1. Place the phone flat on a table between two players
2. Tap the centre card to start
3. Cards are dealt one at a time, alternating between Player A (top) and Player B (bottom)
4. When the **card rank matches the current call** (shown in the centre), slap your side of the screen
5. **Correct slap** — the other player takes the pile as a penalty
6. **Wrong slap** — you take the pile as a penalty
7. **Near miss** (rank is 1 away — K counts as next to A) — amber flash, you still take the penalty
8. First player to empty their deck wins

## Features

- **Face-to-face layout** — Player A's zone is flipped 180° for natural two-player positioning
- **Installable PWA** — add to home screen for fullscreen play; works offline once installed
- **Procedural slap sound** — generated via Web Audio API (no audio files needed)
- **Haptic feedback** — vibration on taps, matches, and errors (iOS Safari)
- **Near-miss detection** — amber feedback when you're one rank off, including K ↔ A
- **Pause/validation system** — game pauses after each slap so players can check the card before resuming
- **Responsive** — works on any screen size, uses dynamic viewport height (`dvh`) for mobile browsers
- **Zero dependencies** — vanilla HTML, CSS, and JavaScript in a single page

## Install as an App

Slaps is a Progressive Web App — no app store required:

1. Open [wsamuelw.github.io/slaps](https://wsamuelw.github.io/slaps/) on your phone
2. **iOS Safari:** Share → *Add to Home Screen*
3. **Android Chrome:** menu → *Add to Home Screen* / *Install app*

The installed game launches fullscreen with its own icon and plays offline (airplane mode works). The offline cache activates from your second visit.

## Tech Stack

- Vanilla HTML + CSS + JavaScript — zero dependencies
- Web Audio API for sound generation
- Service worker + web app manifest for PWA/offline support
- Nunito (Google Fonts) for typography
- Optimised for iOS Safari touch handling

## Running Locally

Open `index.html` in any browser. For the best experience, test on an actual mobile device.

```bash
# Optional: serve it
npx serve .
```

Serving over `http://localhost` or HTTPS enables the service worker (required for offline mode); opening the file directly (`file://`) works but skips it.

## Project Structure

```
index.html      # The entire game — markup, styles, and logic
manifest.json   # PWA manifest (name, icons, display mode)
sw.js           # Service worker: cache-first app shell for offline play
icons/          # App icons (192px, 512px, Apple touch icon)
```

## License

[MIT](LICENSE)
