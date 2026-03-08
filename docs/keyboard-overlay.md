# ⌨️ Keyboard Overlay Configuration

The keyboard overlay appears on the loading screen and visually highlights keybinds to help new players learn essential controls. You can customize the compact keyboard layout, displayed language, and individual shortcuts using the `keyboardShortcuts` configuration.

---

## JSON Structure

```json
"keyboardShortcuts": {
    "layout": "ansi",
    "locale": "en-US",
    "keys": [
        {
            "key": "~",
            "onFoot": "Point",
            "inCar": "Put on seatbelt"
        },
        {
            "key": "Left Arrow",
            "onFoot": null,
            "inCar": "Left Indicator"
        },
        {
            "key": "Right Arrow",
            "onFoot": null,
            "inCar": "Right Indicator"
        },
        {
            "key": "Up Arrow",
            "onFoot": null,
            "inCar": "Hazard Lights"
        },
        {
            "key": "L",
            "onFoot": "Lock vehicle",
            "inCar": null
        },
        {
            "key": "G",
            "onFoot": null,
            "inCar": "Toggle vehicle engine on/off"
        },
        {
            "key": "Z",
            "onFoot": "Open radial menu",
            "inCar": null
        },
        {
            "key": "X",
            "onFoot": "Hands up",
            "inCar": null
        },
        {
            "key": "LALT",
            "onFoot": "Third eye view",
            "inCar": null
        }
    ]
}
```

## Field Breakdown

| **Field** | **Description** |
|---------|-----------------|
| `layout` | Optional. Controls which compact keyboard layout is rendered. Supported values: `ansi`, `iso`, `jis`. |
| `locale` | Optional. Controls how special key labels are displayed in the overlay. Example values: `en-US`, `de-DE`, `fr-FR`, `es-ES`, `pt-BR`, `ar`, `zh-CN`, `ja-JP`. |
| `keys` | Array of keybind entries to highlight on the keyboard. |
| `key` | The key to highlight on the keyboard. Use the key label shown in the overlay preview or one of the standard names listed below. |
| `onFoot` | Tooltip text shown when the player is **on foot**. |
| `inCar` | Tooltip text shown when the player is **in a vehicle**. |

!!! info "Multiple Contexts"
    You can define different behaviors for the same key depending on whether the player is on foot or in a vehicle.

!!! info "Optional Settings"
    If `layout` or `locale` are omitted, the loading screen will fall back to default values. Existing configs without these fields will continue to work.

## Keyboard Layouts

The loading screen uses a compact keyboard overlay and supports multiple layout styles:

| Layout | Description |
|--------|-------------|
| `ansi` | Standard US-style compact keyboard layout |
| `iso` | Common European-style compact keyboard layout |
| `jis` | Japanese-style compact keyboard layout |

!!! note "What layout changes"
    The selected layout affects how symbol keys are displayed in the overlay. It does **not** change your server's actual game keybinds — it only changes the visual keyboard preview.

## Locale / Language Display

The `locale` field changes the displayed labels for special keys such as:

- `Tab`
- `Caps Lock`
- `Enter`
- `Shift`
- `Ctrl`
- `Alt`
- `Space`

Example:

```json
"keyboardShortcuts": {
    "layout": "iso",
    "locale": "de-DE",
    "keys": [
        {
            "key": "LALT",
            "onFoot": "Third eye view",
            "inCar": null
        }
    ]
}
```

This would render the keyboard using the ISO layout and German-style special key labels.

## Accepted Key Names

For best results, use the exact key label shown in the keyboard overlay preview.

### Standard Named Keys

| Actual Key | JSON Key Name |
|----------|----------------|
| Left ALT | `LALT` |
| Right ALT | `RALT` |
| Left CTRL | `LCTRL` |
| Right CTRL | `RCTRL` |
| Left SHIFT | `LSHIFT` |
| Right SHIFT | `RSHIFT` |
| Space Bar | `SPACE` |
| Backspace | `BACKSPACE` |
| Enter | `ENTER` |
| Tab | `TAB` |
| Caps Lock | `CAPS LOCK` |
| Left Arrow | `Left Arrow` |
| Right Arrow | `Right Arrow` |
| Up Arrow | `Up Arrow` |
| Down Arrow | `Down Arrow` |
| Windows Key | `WIN` |

### Letters and Numbers

You can use normal letters and numbers directly:

```json
{ "key": "A", "onFoot": "Action", "inCar": null }
{ "key": "1", "onFoot": null, "inCar": "Seat position" }
```

### Symbol Keys

Symbol keys should use the visible symbol shown in the compact keyboard overlay.

Examples:

| Key | JSON Key Name |
|-----|----------------|
| Tilde / top-left symbol key | `~` |
| Minus | `-` |
| Equals | `=` |
| Left Bracket | `[` |
| Right Bracket | `]` |
| Backslash | `\` |
| Semicolon | `;` |
| Quote | `'` |
| Comma | `,` |
| Period | `.` |
| Slash | `/` |

!!! tip "Top-left key compatibility"
    The top-left symbol key accepts `~`. Existing configs using `` ` `` are still supported for compatibility.

!!! warning "Naming Matters"
    Special named keys must match the supported values exactly. For example, use `LALT` instead of `Alt`, and `SPACE` instead of `Spacebar`.

## Tips for Best Results

- Keep tooltips short and action-focused.
- Use the same `layout` that best matches your community's keyboard style.
- Use the same `locale` as the language used throughout your loading screen.
- For symbol keys, use the exact symbol shown in the overlay preview.
- Avoid repeating the same key across multiple entries unless you intentionally want different `onFoot` and `inCar` behavior.

???+ note "Keyboard Overlay Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
    <video src="./../media/mp4/KeyboardDemo.mp4" autoplay muted playsinline loop style="max-width: 100%; border-radius: 12px;">
    </video>
    </div>

---
