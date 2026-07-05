# Real-to-Sim 6-DoF Object Pose — project page

Project page for the 6-DoF object-pose pipeline that recovers the full per-frame
trajectory of a manipulated object from a **single egocentric RGB video (no depth
sensor)**, so teleoperated robot demonstrations can be replayed in simulation.

**Live page:** https://hudela390.github.io/real2sim-6dpose/

Team 22 · ETH Zürich — 3D Vision course project.

## What's here
- `index.html` — the project page (self-contained: inline CSS + JS).
- `videos/` — box-overlay result clips (tracked CAD pose on the source egocentric RGB, 50 fps):
  - `duck_104715 / 105719 / 112416` — full grasp→drop→settle rollouts.
  - `duck_105719_before` — released-phase before/after comparison.
  - `pan_143550 / 143954 / 144647` — MAPLE pan (cross-dataset).

## Pose pipeline code
The tracking pipeline lives in a separate repo: **[RGBTrack-3DV](https://github.com/3dv-fs26-real2sim/RGBTrack-3DV-)**
(RGBTrack base + frame-0 GoTrack anchor + in-hand `h5` correction + GoTrack drop-to-rest + compose).

## Editing / adding content
- **Authors:** edit the `.authors` / `.affil` lines in `index.html`.
- **More videos:** drop an `.mp4` in `videos/` and add a `<figure><video …></figure>` in the relevant grid.
- **3D (coming soon):** the `#threed` section is a placeholder for embedded Isaac Sim replays / interactive 3D
  (e.g. `<model-viewer>` or three.js) once the real-to-sim side is ready.

## Preview locally
Just open `index.html` in a browser (videos are relative paths). No build step.
