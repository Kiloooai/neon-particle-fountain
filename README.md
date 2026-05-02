# 🌟 Neon Particle Fountain

*Click or drag to emit glowing particle fountains. Particles arc with gravity, bounce off surfaces, drift in wind. Adjustable burst count, speed, spread, gravity, bounce, wind, lifetime, glow. Color modes: rainbow, fire, ice, neon, matrix. Zero-pressure generative art toy.*

---

## What is this?

A mesmerizing particle simulator. Click anywhere (or drag) to emit bursts of glowing particles that fly upward, arc under gravity, bounce off the bottom, and drift in wind. Each particle is a tiny glowing dot with its own physics. Adjust everything: how many particles per burst, launch speed, spread angle, gravity strength, bounce factor, wind, lifetime, glow intensity, and color mode. It's part toy, part art generator, part stress reliever. Just make pretty lights and watch them dance.

---

## Features

- **Particle physics** — gravity, velocity, bounce, wind
- **Interactive emit** — click or drag to spray particles
- **Fully adjustable:**
  - Burst count (1–50)
  - Launch speed (5–25)
  - Spread angle (10°–120°)
  - Gravity (0.05–1)
  - Bounce (0–0.95)
  - Wind (-0.5 to +0.5)
  - Particle lifetime (60–400 frames)
  - Glow intensity (0–30)
- **Color modes:** Rainbow (random), Fire (orange/yellow/red), Ice (cyan/blue), Neon (cycling hue), Matrix (greens)
- **Stats overlay** — particle count, FPS
- **Clear / Random** buttons
- **Single HTML file** — no dependencies

---

## How to Play

1. Open `index.html`
2. **Click** anywhere to emit one burst of particles
3. **Drag** to create a continuous stream of bursts (like holding a fountain nozzle)
4. Watch particles arc, bounce, drift, and fade
5. Use the sliders to change the fountain's behavior in real-time
6. Try **Random Burst** to discover wild combinations
7. **Clear All** to wipe the screen

**Mobile:** Touch and drag works great.

---

## Parameters Explained

| Parameter | What it does |
|-----------|--------------|
| Particles per Shot | How many particles per click/drag emission |
| Launch Speed | Initial upward velocity |
| Spread Angle | Cone width of particle directions |
| Gravity | Downward acceleration |
| Bounce | Energy retained when hitting bottom (0 = no bounce, 0.95 = very bouncy) |
| Wind | Horizontal drift per frame (negative = left, positive = right) |
| Lifetime | Frames before a particle fades out |
| Glow Intensity | Shadow blur amount for neon glow |
| Color Mode | Hue palette of particles |

---

## Technical Notes

- Particles are simple point masses with position + velocity
- Physics: `vy += gravity; vx += wind; x += vx; y += vy`
- Bottom collision: `if y > height: y = height; vy *= -bounce; vx *= 0.95`
- Side walls: bounce with same bounce factor
- Lifetime used for alpha fade: `alpha = 1 - age / lifetime`
- Rendering: canvas arc with shadowBlur for glow
- Background: `rgba(0,0,0,0.15)` fill each frame for motion trails
- FPS counter via 1-second accumulation
- Color generation per mode: random hue ranges

---

## The Real Story

Particles are pure visual candy. There's no goal. No score. Just watching thousands of glowing dots dance around makes people smile. It's the kind of thing you leave open on a second monitor just to see the colors move. The drag-to-emit interaction feels like spraying paint or holding sparklers. Turn wind on and watch them drift like embers. Crank the bounce and they never die. Crank gravity and they plummet. It's a tiny universe of light in your browser.

Also: the name "fountain" is literal. Shoot them up and watch them arc.

---

*Made with ✨ and a lot of glowing dots during a heartbeat build cycle.*

**Repo:** https://github.com/Kiloooai/neon-particle-fountain
