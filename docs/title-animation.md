# ✨ Title Animation

Control how the watermark **title** (your server name) animates, and toggle the sweeping sheen highlight over it.

These options live inside `watermark.label`, right alongside the title text.

!!! tip "Quicker in the Config Builder"
    The [Config Builder](https://loadingscreen.4zam.dev/builder.html) sets all of this under **Brand & Color** with a live preview, and [Build with AI](https://loadingscreen.4zam.dev/ai.html) can set it up from a plain description. Every field with its type and default is in the Config reference: [`watermark`](config-reference.md#watermark).

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

`label.animation` picks the preset and `label.sheen` turns the sweeping light on or off (`true` by default). Both are in the [Config reference](config-reference.md#watermark).

!!! info "Defaults"
    If `animation` is missing or set to a value that doesn't exist, the title falls back to **`wave`**. If `sheen` is omitted, the sheen is **on**: set `"sheen": false` to turn it off.

---

## Available Presets

Every preset is hand-tuned to look premium and animates smoothly without straining the FiveM UI. The full list, with what each preset looks like, is generated from the code: see [title animation presets](config-reference.md#values-watermark-label-animation).

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
