# Dot Bloom

A generative dot-painting piece. Hundreds to thousands of hand-wobbled circles
pack edge to edge on a warm black ground, smaller dots nested inside larger
ones, colour drifting into loose neighbourhoods. Each painting grows in from a
single point, and no two are the same.

**Live:** https://thomaspavitte-beep.github.io/dot-bloom/

The main page is a slideshow: it fills the browser window, and every few
seconds the finished painting melts away and a fresh composition blooms in,
with the assembly choreography and colour palette chosen at random each time.
No controls, no settings. Clicking anywhere skips straight to the next
painting, blooming from where you clicked. Left alone, the painting also keeps
quietly breathing, a few dots at a time.

## The Studio

**https://thomaspavitte-beep.github.io/dot-bloom/studio.html**

The full toolkit behind the piece, with every dial exposed via the button in
the corner: seed stepping, dot scale, gap, wobble, ellipticity, colour
clustering, per-dot colour jitter, paint pooling, seven palettes, five bloom
orders, bloom time, ambient drift, a surprise button that scrambles
everything, and PNG export.

Studio extras: **click** blooms a new seed from the click point, **holding
right-click** retouches dots under the brush with new colours, arrow keys step
the seed, `x` surprises, `space` replays, `s` saves.

## What it does

Dots are packed by rejection sampling so they never touch, never overlap, and
never cross the canvas edge. Sizes come in six discrete tiers; the larger ones
carry off-centre nested dots. Colour is picked from an ordered palette ring with
gentle spatial clustering, then jittered per dot so no two are identical, and
each dot pools slightly darker at its rim like settling acrylic. The wobble,
the ellipticity, and the off-centre nesting are all deliberate: the goal is work
that reads as handmade rather than as vector output.

Seven palettes (candy, earth, porcelain, ember, reef, meadow, midnight), each a
fixed ring ordered so neighbouring colours sit happily together. Five bloom
orders: ripple, sweep, painter, one-pot-at-a-time, scatter.

Every painting is seeded, so the same seed and settings reproduce it exactly.

## Built with

Two self-contained HTML files and [p5.js](https://p5js.org/). No build step.
