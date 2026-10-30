# Tinkerbench

A single-file, Tinkercad-style 3D editor and slicer that runs in the browser. Built for touch (Android tablet and phone) and tuned for a Sovol SV06 running Klipper.

Open `tinkerbench.html` in a browser. It needs internet for the Three.js and Clipper libraries (loaded from jsdelivr).

## What it does
- **Shapes and editing:** primitives, text, freehand lines, SVG import, loft, revolve, hollow, round and chamfer, booleans (group, hole, intersect), mirror, align, snapping.
- **Modelling tools:** linear and circular arrays, split by plane, push/pull on flat faces, chamfer or round one straight edge.
- **Sizing:** millimetres, or percentages (`105` or `50%`) for single shapes and multi-selections.
- **Workflow:** scene list, ungroup, multiple plates, new project with an unsaved-changes prompt, saved projects, undo per plate.
- **Export:** STL, 3MF, OBJ.
- **Slicer:** walls, top/bottom skins, lines or grid infill, skirt or brim, retraction, fan, layer preview, G-code download, optional Moonraker upload.

## Slicer limits
- No supports yet. Keep overhangs under about 45 degrees.
- Features thinner than about two line widths are not handled properly.
- Direct upload to Moonraker only works if the page can reach the printer (an https page cannot call an http printer, and Moonraker needs the page under `cors_domains`). Otherwise download the G-code and upload it in Mainsail.
- Tested in headless Chromium and node, not on a real printer yet. Watch the first print.

## Storage
Autosaves to `localStorage` in the browser. Use the save icon to download a project file, or Projects to keep named copies in the browser.
