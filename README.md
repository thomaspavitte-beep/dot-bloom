# Dot Bloom

A generative dot-painting toy. Hundreds to thousands of hand-wobbled circles
pack edge to edge on a warm black ground, smaller dots nested inside larger
ones, colour drifting into loose neighbourhoods. Each painting grows in from a
single point, and no two are the same.

**Live:** https://thomaspavitte-beep.github.io/dot-bloom/

It fills the whole browser window. All the controls hide behind one button in
the bottom-right corner.

## Using it

- **Click anywhere** to bloom a fresh painting outward from where you clicked.
- **Hold right-click and move** to retouch: dots under the brush crossfade to
  new colours, like working back into wet paint.
- **The corner button** opens the settings panel: seed, form, colour, and
  motion, plus a **surprise** button that scrambles everything.

Keyboard: arrow keys step the seed, `r` random, `x` surprise, `space` replays
the bloom, `s` saves a PNG, `a` toggles the ambient colour drift, `t` opens the
panel.

## What it does

Dots are packed by rejection sampling so they never touch, never overlap, and
never cross the canvas edge. Sizes come in six discrete tiers; the larger ones
carry off-centre nested dots. Colour is picked from an ordered palette ring with
gentle spatial clustering, then jittered per dot so no two are identical, and
each dot pools slightly darker at its rim like settling acrylic. The wobble,
the ellipticity, and the off-centre nesting are all deliberate: the goal is work
that reads as handmade rather than as vector output.

Choose how a painting assembles from five bloom orders (ripple, sweep, painter,
one-pot-at-a-time, scatter) and from three palettes (candy, earth, porcelain).
Left to itself, the painting keeps quietly drifting one dot at a time.

Every painting is seeded, so the same seed and settings reproduce it exactly.

## Built with

A single self-contained HTML file and [p5.js](https://p5js.org/). No build step.
