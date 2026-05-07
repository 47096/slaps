# Slaps

A two-player face-to-face card game built for mobile browsers. Place your phone flat between two players — each player taps their side of the screen to slap when the dealt card matches the call rank.

## How to Play

1. Place the phone flat on a table between two players
2. Tap the centre card to start
3. Cards are dealt one at a time, alternating between Player A (top) and Player B (bottom)
4. When the **card rank matches the current call** (shown in the centre), slap your side of the screen
5. **Correct slap** — the other player takes the pile as a penalty
6. **Wrong slap** — you take the pile as a penalty
7. **Near miss** (rank is 1 away) — amber flash, you still take the penalty
8. First player to empty their deck wins

## Features

- **Face-to-face layout** — Player A's zone is flipped 180° for natural two-player positioning
- **Procedural slap sound** — generated via Web Audio API (no audio files needed)
- **Haptic feedback** — vibration on taps, matches, and errors (iOS Safari)
- **Near-miss detection** — amber feedback when you're one rank off
- **Pause/validation system** — game pauses after each slap so players can check the card before resuming
- **Responsive** — works on any screen size, uses dynamic viewport height for mobile browsers

## Tech Stack

- Vanilla HTML + CSS + JavaScript — zero dependencies
- Nunito (Google Fonts) for typography
- Web Audio API for sound generation
- Optimised for iOS Safari touch handling

## Running Locally

Open `index.html` in any browser. For the best experience, test on an actual mobile device.

```bash
# Optional: serve it
npx serve .
```
