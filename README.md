# Stair model

Interactive 3D model of a left-turning U-stair with a wall-side handrail,
generated from measured plan lengths. Open `index.html` in any modern
browser, or view the hosted page at https://krusknall.github.io/stair-model/

## How it works

The stair is described by a handful of parameters: stair width, floor-to-floor
height, number of risers, number of winder treads in each turn, and the three
plan lengths along the walls (A1, B1, C1). From these the page lays out one
nosing line per riser, extrudes the steps, lays a handrail along the wall at a
set height above the nosings, and reports the resulting sloping handrail
lengths (A2, B2, C2) next to the lengths measured on site.

All of this runs in the browser; there is no server and no build step.

## Files

- `index.html` – the page, including all styling and the model code

The 3D library (three.js r128, MIT licence) is loaded from cdnjs. To make the
page work fully offline, download
https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js into this
folder and change the `<script src>` in `index.html` to `three.min.js`.

## Editing the measurements

Move the sliders in the bottom panel, or change the defaults in the
`PARAMETERS` object and the `MEASURED_SLOPING` values at the top of the script
in `index.html`.
