# Super Plumber Bros — Level 1 🍄

A high-resolution, mobile-first homage to the classic first level — built as a
**single self-contained HTML file** with zero dependencies. All graphics are
drawn procedurally in vectors (crisp at any screen DPI) and all music & sound
effects are synthesized live with WebAudio (an original chiptune composition).

## ▶️ Play

Open `index.html` in any modern browser — or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000 on your phone (same Wi-Fi)
```

Or enable GitHub Pages on this repo and play it straight from the URL.
Add it to your phone's home screen for a fullscreen app-like experience.

## 📱 Mobile features

- **Touch controls** — on-screen D-pad, A (jump), B (run), with multi-touch
- **Rotation support** — play portrait or landscape; the camera and HUD adapt live
- **High-DPI rendering** — vector art scaled to your device's pixel ratio (retina-crisp)
- **Safe-area aware** — controls clear the notch / home indicator
- Keyboard also works on desktop: arrows / WASD + Space (jump) + Shift (run)

## ✨ Creative effects

- 🌅 **Day → sunset cycle**: the sky, sun, hills and clouds shift as the level
  timer runs down — stars come out if you're slow
- 👻 **Speed ghost-trail** when sprinting or falling fast
- 💥 Particle systems everywhere: brick shards, coin bursts, landing dust, run dust
- 📳 Screen shake on brick breaks and stomps
- 🔢 **Stomp combos**: chain stomps without landing for ×2, ×4, ×8… score multipliers
- 🎆 Fireworks finale at the castle
- 🪙 Floating score popups & pulsing question blocks

## 🎮 The level

A full 1-1 style course: question blocks, breakable bricks, growing pipes,
mushroom power-ups (get big, break bricks, take a hit), floating coin rows,
goombas, twin pyramids, three pits, the grand staircase, flagpole and castle.
1-UP every 50 coins. 300 on the clock — height on the flagpole earns bonus points.

## 🔊 Audio

Original chiptune loop (square lead, triangle bass, noise hats) plus
synthesized SFX for jump, coin, stomp, power-up, brick break, death, flag
fanfare and fireworks. Tap the speaker icon to mute.
