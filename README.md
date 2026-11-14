# Tinkerbench

A single-file, Tinkercad-style 3D editor and slicer that runs in the browser. Built for touch (Android tablet and phone) and tuned for a Sovol SV06 running Klipper.

Open `tinkerbench.html` in a browser. It needs internet for the Three.js and Clipper libraries (loaded from jsdelivr).

## What it does
- **Shapes and editing:** primitives, text, freehand lines, SVG import, loft, revolve, hollow, round and chamfer, booleans (group, hole, intersect), mirror, align, snapping.
- **Modelling tools:** linear and circular arrays, split by plane, push/pull on flat faces, chamfer or round one straight edge, shell (hollow out any closed solid, optional open top or bottom).
- **Sketch pad:** pen, line, rectangle, circle and eraser with auto edge-joining. Revolve a profile, or extrude from the floor, a wall or a tapped face (add or cut). Select a shape to type exact sizes.
- **Inspect:** measure tool (corner, edge and face snapping, distance and angle), section view, adjustable snap grid that follows zoom.
- **Components:** make a group a component; edit one copy and every linked copy follows.
- **Sizing:** millimetres, or percentages (`105` or `50%`) for single shapes and multi-selections.
- **Workflow:** scene list, ungroup, multiple plates, new project with an unsaved-changes prompt, saved projects, undo per plate.
- **Export:** STL, 3MF, OBJ.
- **Slicer:** walls, top/bottom skins, lines or grid infill, automatic supports (bed-only or everywhere), spiral vase mode, print-failure check, skirt or brim, retraction, fan, layer preview, G-code download, optional Moonraker upload.

## Slicer limits
- Supports are plain columns: no tree supports and no support blockers.
- Features thinner than about two line widths are not handled properly.
- Direct upload to Moonraker only works if the page can reach the printer (an https page cannot call an http printer, and Moonraker needs the page under `cors_domains`). Otherwise download the G-code and upload it in Mainsail.
- Tested in headless Chromium and node, not on a real printer yet. Watch the first print.

## Storage
Autosaves to `localStorage` in the browser. Use the save icon to download a project file, or Projects to keep named copies in the browser.
