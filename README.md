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

- **Touch controls** — ◀ ▶ D-pad (left), **A** = jump, **B** = run / throw
  fireballs (right), with multi-touch
- **Rotation support** — play portrait or landscape; the camera and HUD adapt live
- **High-DPI rendering** — vector art scaled to your device's pixel ratio (retina-crisp)
- **Safe-area aware** — controls clear the notch / home indicator
- **No accidental zoom** — pinch / double-tap zoom is suppressed so taps never
  zoom the page
- Keyboard also works on desktop: arrows / WASD + Space (jump) + Shift (run/fire)

## 🔥 Power-ups

- **Mushroom** — grow big: break bricks and survive a hit
- **Fire flower** — appears from a power block when you're already big. Turns you
  into Fire Plumber (white shirt, red overalls) and lets you press **B** to throw
  bouncing fireballs that ricochet off the ground and burn goombas. Up to two
  fireballs in the air at once. Getting hit steps you back down: fire → big → small.

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
