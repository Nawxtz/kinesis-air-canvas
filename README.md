# KINESIS — Spatial Computing Instrument

An aerospace-grade air canvas powered by **MediaPipe hand tracking** — draw in the air with your index finger, switch colors and brush sizes with pinch gestures, and export your artwork as PNG.

## ✨ Features

- **☝️ 1-Finger Draw** — Index finger extended = pen down. Curled fingers are locked out (Pen-Down Menu Lock).
- **🤏 Pinch Gestures** — Thumb + middle/ring/pinky to cycle colors or brush sizes (pen must be lifted).
- **🎨 Custom Palette** — 6 editable color slots with an interactive HSL color wheel.
- **☀️ Auto-Brightness** — Real-time luma sampling adjusts webcam gain automatically.
- **💾 Save Flow** — Peace sign (5s) → thumbs up (3s) to export canvas as PNG.
- **↩️ Undo / Clear** — `Ctrl+Z` to undo strokes, `Space` to clear.

## 🚀 Quick Start

```bash
# Just open index.html — no build step needed
python3 -m http.server 8000
# Then open http://localhost:8000
```

## 🕹️ Gesture Matrix

| Gesture | Action |
|---|---|
| ☝️ 1 finger (index) | Draw + Menu Lock |
| 🤏 Thumb + middle | Next color |
| 🤏 Thumb + ring | Previous color |
| 🤏 Thumb + pinky | Cycle brush size |
| ✌️ 2 fingers | Pen lift / hover |
| ✌️ Hold 5s | Save prompt |
| 👍 Hold 3s | Confirm save |
| 👎 Thumbs down | Cancel save |
| ✊ Fist | Standby |
| `Ctrl+Z` | Undo |
| `Space` | Clear all |

## 🛠️ Tech Stack

- [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands) — hand landmark detection
- Web Audio API — haptic-style audio feedback
- Canvas 2D API — drawing engine
- Vanilla JS / HTML — no framework, no build tool
