# A320 Web Cockpit Prototype

A first browser-based 3D cockpit scaffold inside the A320-Home-Cockpit repository.

## Run it locally

Because the page imports Three.js as an ES module, serve this directory over HTTP rather than opening `index.html` directly.

For example, with Python 3 installed:

```bash
cd web-sim
python3 -m http.server 8000
```

Then open http://localhost:8000 in a modern browser with WebGL 2 support.

## Controls

- Drag on the 3D view to look around.
- Use the thrust, pitch, and roll sliders.
- Arrow keys adjust pitch and roll.
- Power, engine, autopilot, and gear buttons toggle prototype state.

## Current limitations

This is an early visual and interaction scaffold. The 3D cockpit is made from placeholder geometry, and the flight-state logic is illustrative only. It is **not** a realistic or certified flight model, and the controls are not yet connected to a real flight simulator.

The parent repository mainly contains physical cockpit construction documentation and individual CAD/3D-print files. Future work should identify suitable panel assets, convert selected assets to browser-friendly glTF/GLB where appropriate, optimize them, and then connect interactive controls to a better-defined simulation model.

Three.js is loaded from jsDelivr in this prototype, so the first load requires an internet connection.
