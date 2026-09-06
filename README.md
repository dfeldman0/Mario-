# Games in this repo

| Game | File | What it is |
|---|---|---|
| 🍄 Super Plumber Bros | `index.html` | Mobile-first level 1-1 platformer |
| 🚹 The Urinal Test | `urinal-test.html` | 10 rounds of spatial etiquette under pressure |

## 🚹 The Urinal Test

A single-file browser game that tests the one skill they never teach in school:
**picking the right urinal.** Two modes: **The Gauntlet** (10 scripted rounds)
and **Endless Rush** (procedurally generated rounds until the rush claims you).

- **The etiquette engine** scores every open spot: distance from occupants,
  end bonus, divider mitigation. Optimal = *Perfect*; safe but suboptimal =
  *Acceptable* (streak resets); adjacent when you had options = **splashed** —
  haptic vibration, screen shake, droplet overlay, −1 of 3 pairs of dry pants.
- **Three fixture types**: wall urinals (with or without dividers), the
  wall-mounted **old-school trough** (running water, everyone faces the wall),
  and the free-standing clawfoot **shame tub** — people stand all around it
  facing each other, and **direct eye contact across the water** is the
  unforgivable sin.
- **The Meta smart-glasses guy** (🔴 REC) needs extra distance — dividers don't
  help, you're on his livestream. **Travelers' rolling luggage** blocks spots
  in airports & stations (pick one and you trip).
- **The drink economy is your choice**: after a winning pick, the venue
  offers a menu — and every button prints its exact math. **🍺 Beer** +10%
  score buzz but the next clock runs 12% faster; **☕ cold brew** a modest
  +6% that barely touches the clock; **⚡ espresso** +18% but the clock
  flies 25% faster. Every drink is +1 in the tank; at ×3 you're
  **desperate** — run out of time and you **piss yourself: instant game
  over** ("🌊 Puddle Maker"). Going while desperate vents the 2 oldest
  drinks. Dive bars pour doubles; the coffee shop doesn't stock beer.
- **The stall gamble**: a stall door sits at the end of every row (plus a big
  button). You get **3 stall waits per run**; each burns ~2.5 seconds and
  ~40% of the time it's occupied ("…someone's IN here!"). On unwinnable
  boards the stall is the *correct* play — and if it fails you, gritting the
  least-bad spot is honorable. On solvable boards a successful stall is a
  low-score refuge that resets your streak (but empties your bladder).
- **Center-stage announcements**: every round opens with a big intro card
  (venue, layout, warnings) before the timer starts, and critical events —
  desperation, stall verdicts, drink consequences — hit as animated
  center-screen banners you can't miss.
- **📍 Play your home ballpark**: opt-in geolocation (on-device only) finds
  the nearest of all 30 MLB parks and turns stadium rounds into *your* park —
  a big marquee sign ("WRIGLEY FIELD — HOME OF THE CUBS"), team-colored
  bunting, and signature set dressing: Wrigley's ivy wall, Fenway's Green
  Monster + scoreboard, Yankee Stadium's frieze.
- **🏟️ Photo interstitials**: ballpark rounds open with a full-screen iconic
  photo of *your* park ("NOW ENTERING WRIGLEY FIELD… find the head, hero")
  with a slow cinematic zoom before the restroom appears. Up to 4 photo
  variants per park (106 images) rotate randomly per visit — all in `parks/`
  (sources & licenses in `parks/CREDITS.md`); drop in your own JPG named
  `<park-slug>-<n>.jpg` to replace any of them.
- **🏙 City-edition venues**: with a home park set, every entrance card is a
  "special edition Monopoly" version of your city — dive bars named from
  real neighborhoods and the local pour ("THE OLD STYLE BENCH — Wicker
  Park, est. 1971"), roasteries with localized menus ("deep dish scone",
  "chicago fog"), festivals with rotating punny lineups, and airport /
  station boards listing real departures to the other 29 league cities.
  All cards float over a blurred photo of your ballpark, names and copy
  draw from no-repeat decks, and a gold "CHICAGO EDITION" chip seals it.
- **🗺️ Road Trip**: score 650+ in any mode to permanently unlock the park
  picker — play *any* of the 30 ballparks, with its photos, team colors,
  airport, station and city banner. Your home turf is earned; the league is
  a reward. Mid-run, road trips happen at **travel moments**: a
  boarding-pass **layover card** appears between rounds — the 7th-inning
  stretch in the Gauntlet, every 5th round in Endless (never in the Daily) —
  with the clock stopped. Change cities or stay; score and streak carry
  either way. Finish a run on your feet and the end screen offers to take
  your points on the road — **the score only resets when you actually
  lose**; survivors keep compounding city after city.
- **Orientation is obvious**: guys facing you at the shame tub hold a
  ballpark frank at waist level with both hands. That's what the hands are
  doing. It's a hot dog. Rated E for Everyone.
- Streak multipliers, synthesized sound effects, a one-line etiquette lesson
  after every choice, endless-mode best-run tracking, ranks from *Splash
  Survivor* to *Urinal Grandmaster*.

### Viral loop (all client-side, no backend)

- **📅 Daily Challenge** — date-seeded rounds, identical for everyone
  worldwide (deterministic seeded RNG), one recorded attempt per day, and a
  Wordle-style emoji result grid (`🟩🟩💦🚪😬…`) shared via the native share
  sheet.
- **⚔️ Challenge links** — every run is seeded; one tap builds a URL that
  makes a friend play your *exact* rounds with your score to beat. Verdict
  shown on their end screen. Score travels in the URL — no server.
- **📜 Shareable certificate** — a canvas-rendered "Certificate of Urinal
  Etiquette" PNG (rank, stats, home ballpark, gold seal, Chief Attendant
  signature) shared as an image.
- **🧻 Share → 5 free towels** — completing any share banks 5 free respawns
  in a cookie + localStorage.
- **📺 Rewarded-ad respawn slot** — after pissing yourself (or any loss):
  use a banked towel, or hit the "watch ad for a towel" flow — currently a
  placeholder modal with a single `showRewardedAd(callback)` hook ready for
  Google AdMob / Ad Manager.
- **🌆 Metro-wide localization** — your home park also localizes the airport
  round (O'Hare, LGA, Sea-Tac…), the train-station round (Union Station,
  Grand Central, 30th Street…), and stamps a "CHICAGO EDITION" banner on the
  title screen.

### 🌡️ Local climate

Your home city's actual weather is part of the joke, derived from the park's own
coordinates — no data table to go stale. **Phoenix in July** throws up a
🥵 *HEAT ADVISORY* (dry-heat cities) and **Houston or Miami** get 💧 *SWAMP AIR*:
amber heat shimmer over the room, warm lighting, and the clock runs 10% faster
because you've been chugging water all day. **Boston, Minneapolis, Toronto or
Denver in January** get 🥶 *DEEP FREEZE*: icy blue cast, drifting flurries, frost
creeping in from the edges — and since cold makes you go, **you hit desperate at
2 drinks instead of 3**. Spring and fall play neutral. The mechanical half is
skipped in the Daily so the shared challenge stays identical worldwide.

### 🔥 Streaks, 🛂 passport & personal bests

All client-side in `localStorage` — no backend, nothing to sign up for.

- **Daily streak** — playing the Daily on consecutive days builds a streak with
  permanent-feeling perks: **3 days = +1 pair of pants**, **7 days = +1 stall
  wait**, 30 days = bragging rights. Yesterday still counts until midnight.
- **🛂 The passport** — a stamp for every one of the 30 ballparks visited, all 9
  venue types cleared, and all 8 characters met. Earned stamps fill in with the
  team's own colour and a tilted rubber-stamp look; the rest sit as dashed
  placeholders daring you to finish the set.
- **Per-city personal bests** — your high score in each city, shown on its
  passport stamp and beside it in the Road Trip picker.
- **Near-miss framing** — the end screen tells you exactly how far you fell
  short ("😤 140 points short of RESTROOM STRATEGIST") or celebrates a new city
  record, so a loss ends pointing at the retry.
- **Earned titles** — Rookie → Regular → Veteran of the Row → Divider Diplomat →
  Porcelain Professor → Grand Marshal of the Urinal, by career pees.

### 🏅 Career progression

Every **10 successful pees** (lifetime, saved on-device) levels you up and
adds a new mechanic to the rotation, so the game keeps evolving instead of
repeating. The juvenile stuff comes early on purpose:

| Level | Unlock |
|---|---|
| 2 | ⚠️ **Wet floors** — a caution sign at a random spot; picking it costs a 2-second slip |
| 3 | 🐀 **The rat** — sprints in mid-round and parks under a urinal; nobody stands over a rat (−2.0 comfort: never the pro pick), neighbors jump a spot. Tap it: +50 EXTERMINATOR |
| 4 | 👀 **The side-glancer** — one guy keeps looking sideways; dividers can't stop a wandering neck |
| 5 | 👋 **Two shakes** — after a perfect pick, tap exactly twice (+10). One is a drip (−5). Three is playing with it (−15, and he noticed) |
| 6 | 🎲 **The send-it gamble** — on no-good-option boards, going anyway is a coin flip, not an automatic splash |
| 7 | 🕷️ **The spider** — hangs over the BEST urinal. Brave it: 70% +30 NERVES OF STEEL, 30% it drops on you (−2s). Or tap it onto the neighbor, who leaves |
| 8 | 🫧 **Soap jackpot** — a tappable dispenser worth +8 |
| 9 | 📱 **The phone zombie** — mid-round, a guy drifts one urinal over without looking up; the board re-scores |
| 10 | 👟 **Nice shoes** — box-fresh white sneakers are a splash zone (−0.35 aura). Unless he's an 🧢 **away fan** in rival colors: then his kicks are fair game (+0.35, and +40 for splashing them) |
| 11 | 🧍 **The lurker** — standing at a urinal, facing the room, not going, not leaving |
| 12 | 🍺 **Aim** — two drinks deep the stream sways; tap left/right for 1.6s to keep it in the bowl. Steady = +40; miss = −20%, a puddle, and a wet floor next round that is entirely your fault |
| 13 | 🎤 **The crooner** — mid-ballad; his radius is bigger than his talent |
| 14 | ✍️ **Write your name** — every 3-streak (wall rooms, not the Daily): the camera walks up to the wall and you swipe your name. In piss. Legible = +100 LEGEND, sloppy = +25, either way it empties your bladder, skips the bar, and stays on that building's wall on every return visit. If the boss or the REC guy saw, the attendant charges double on your next stall |
| 15 | 🚪 **Rush-hour walk-ins** — dawdle and someone takes the best spot |
| 16 | 🌪️ **Full chaos** — every hazard rolls hotter and stacks |
| 17 | 🌫️ **Festival steam** — the room opens in fog; you can't see who's where until it lifts (~2s) |
| 18 | 🧊 **The iced urinal** — stadium tradition; picking it pays +15 |
| 19 | 👔 **The boss** — stand next to him and you WILL discuss Q3 (−25) |
| 20 | 🎥 **The news crew** — half the room is ON AIR (red rings, comfort penalty) |
| 21 | 🧻 **No paper** — new stall heartbreak: door opens, dispenser's empty, you back out |
| 22 | 🔧 **The rattling pipe** — telegraphs all round, then blows mid-round and blocks the spot |
| 23 | 🐕 **The service dog** — petting urge: −1 second, +5 cuteness |
| 24 | 🔌 **Power dips** — lights out for a full second; the clock does not care |
| 25 | 🚪 **The propped door** — the end spot near it loses its corner privilege |
| 26 | 🤝 **Attendant haggling** — negotiate; stakes escalate every time (+15 → ±35 → +60/−30) |

The juvenile tier (rat, spider, shoes, aim, shakes, graffiti) is all taps and
swipes in the scene — no new buttons. The rat and spider are tappable in 3D
via the same nearest-marker resolution as the urinals; AIM and the graffiti
share one 3D stream (a bezier tube from you to wherever you're pointing it),
and the graffiti canvas unprojects your finger onto the wall plane so the
stream, the paint and the baked wall decal all agree. Tags are stored in
`localStorage` (`ut_tags`, keyed by park + venue).

Level-ups are announced before the next round; the start screen tracks your
career. The Daily Challenge always runs the full rotation so it stays
identical worldwide.

### 🧪 3D Mode

Always on — wall-urinal rounds render as a low-poly 3D room
(three.js, lazy-loaded from `vendor/`) with a **custom post-processing
pipeline built on core render targets** (no extra libs): bloom pulled from
the blurred frame, tilt-shift depth-of-field for a diorama look, in-shader
color grade and vignette — plus **animated patrons**: rush-hour walk-ins
enter through the door with a full leg-swinging walk cycle, phone zombies
side-step one urinal over without looking up, and everyone idles, sways
and breathes. The room itself gets first-person
walk-in from the door, corridor POV down the row, capsule people with
personas (the REC guy's LED blinks in 3D), hazards as real meshes, the
flickering-light hazard as an actually flickering point light,
time-of-day-graded lighting, drag-to-look, tap-to-pick via raycasting, and
the stall door standing at the end of the corridor. **Every layout is 3D**:
the old-school trough renders as one long porcelain river with animated
running water, and the shame tub is a proper clawfoot centerpiece — water
drifting, brass feet, patrons all the way around it (the far side faces
the camera, regulation ballpark frank at waist level), viewed from a
raised diorama angle with floor rings on the near side and bobbing pick-
pins over the far side. The classic 2D view remains only as the fallback
for devices without WebGL. All scoring, HUD, FX and game logic are shared
with 2D.

Open `urinal-test.html` in any browser — best on a phone, where wrong picks
trigger real haptic feedback.

---

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
