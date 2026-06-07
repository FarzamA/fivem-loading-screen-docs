# ✨ Title Animation

Control how the watermark **title** (your server name) animates, and toggle the sweeping sheen highlight over it.

These options live inside `watermark.label`, right alongside the title text.

---

## JSON Structure

```json
"watermark": {
  "label": {
    "text": "The Vibe RP",
    "colorWordCount": 2,
    "animation": "wave",
    "sheen": true
  }
}
```

## Field Breakdown

| **Field**             | **Description**                                                                 |
|-----------------------|---------------------------------------------------------------------------------|
| `label.animation`     | The animation preset applied to the title text. See the preset list below.       |
| `label.sheen`         | A sweeping light "sheen" that passes across the whole title. `true` by default.   |

!!! info "Defaults"
    If `animation` is missing or set to a value that doesn't exist, the title falls back to **`wave`**. If `sheen` is omitted, the sheen is **on** — set `"sheen": false` to turn it off.

---

## Available Presets

Every preset is hand-tuned to look premium and animates smoothly without straining the FiveM UI.

| **Value**       | **Style**                                                                 |
|-----------------|---------------------------------------------------------------------------|
| `wave`          | Each letter gently bobs up and down in sequence. *(Default)*              |
| `wave-reverse`  | The same bob, staggered right-to-left.                                    |
| `bounce`        | A snappier, springier per-letter hop.                                     |
| `ripple`        | Letters scale-pop in sequence, like a travelling ripple.                 |
| `sway`          | The whole title rocks gently left and right.                             |
| `reveal`        | The title wipes in left-to-right, holds, then wipes out — on a loop.      |
| `slam`          | The title punches in with a sharp impact, repeating periodically.        |
| `pulse`         | The title thumps to a beat, with a synced underline glow.                |
| `none`          | No motion — the title appears and stays still.                            |

!!! tip "Sheen layers on top"
    `sheen` is independent of `animation`. The sheen sweep runs **over whichever preset you pick**, so you can pair, for example, `wave` + sheen or `slam` + sheen.

---

## Examples

A calm, premium look:

```json
"label": { "text": "The Vibe RP", "colorWordCount": 2, "animation": "sway", "sheen": true }
```

A high-energy, beat-driven look:

```json
"label": { "text": "The Vibe RP", "colorWordCount": 2, "animation": "pulse", "sheen": true }
```

A completely static title with no sheen:

```json
"label": { "text": "The Vibe RP", "colorWordCount": 2, "animation": "none", "sheen": false }
```

!!! info "Where the title comes from"
    `text` and `colorWordCount` (the title itself and its color split) are documented on the [Watermark](watermark.md) page. `animation` and `sheen` only control how that text moves and shines.

---
