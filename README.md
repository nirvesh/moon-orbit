# Moon Orbit

A small animated space scene built in pure HTML and CSS — no JavaScript, no
images. It started as the freeCodeCamp "Moon Orbit" CSS lab and grew into a
spinning Jupiter with four moons drifting around it against a twinkling
starfield.

## What's in the scene

- **Jupiter** at the center, with soft banded cloud belts that scroll sideways
  under a fixed light source, so the planet reads as turning on its axis rather
  than spinning like a pinwheel.
- **Four moons** on separate orbit rings at different radii and speeds, tinted
  after the Galilean moons (pale-yellow Io, icy Europa, large tan-grey Ganymede,
  and dark Callisto). Each stays upright as it circles.
- **A twinkling starfield** and the occasional **shooting star** crossing the
  background.

## How it works

The whole system is sized from one custom property, `--sys`, so it scales with
the viewport. A few techniques do the heavy lifting:

- **Axial spin** — each body's surface is a double-width strip (`::before`) that
  slides by exactly one tile (`translateX(-50%)`) for a seamless loop, sitting
  under a fixed highlight-and-shadow layer (`::after`) so the light stays put
  while the surface moves.
- **Orbits** — each `.orbit` ring is centered with negative margins and rotated
  with a `rotate()` keyframe; the moon inside counter-rotates so it never tips
  over as it goes around.
- **Accessibility** — all motion is disabled under
  `@media (prefers-reduced-motion: reduce)`.

## Files

```
moon-orbit/
├── index.html
├── css/
│   └── styles.css
└── README.md
```

## Running it

Open `index.html` in any modern browser. That's it — there's nothing to build
or install.

## Credits

Based on the freeCodeCamp Moon Orbit CSS lab, then extended.
