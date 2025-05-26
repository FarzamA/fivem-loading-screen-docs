# ⌨️ Keyboard Overlay Configuration

The keyboard overlay appears on the loading screen and visually highlights keybinds to help new players learn essential controls. You can fully customize this overlay using the `keyboardShortcuts` configuration.

---

## JSON Structure

```json
"keyboardShortcuts": {
    "keys": [
        { 
            "key": "B", 
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

| **Field** | **Description**                                                 |
| --------- | --------------------------------------------------------------- |
| `key`     | Key to highlight on the keyboard (see special key naming below) |
| `onFoot`  | Tooltip text shown when the player is **on foot**               |
| `inCar`   | Tooltip text shown when the player is **in a vehicle**          |

!!! info "Multiple Contexts"
    You can define different behaviors for the same key depending on whether the player is on foot or in a vehicle.

## Special Key Names

To ensure proper mapping and rendering, use the following standard key names for special or non-alphanumeric keys:

| Actual Key | JSON Key Name                                         |
| ---------- | ----------------------------------------------------- |
| Left ALT   | `LALT`                                                |
| Right ALT  | `RALT`                                                |
| Left CTRL  | `LCTRL`                                               |
| Right CTRL | `RCTRL`                                               |
| Space Bar  | `SPACE`                                               |
| Arrow Keys | `Left Arrow`, `Right Arrow`, `Up Arrow`, `Down Arrow` |

!!! warning "Naming Matters"
    Key names must match exactly as shown above — e.g., use "LALT" instead of "Alt" and "SPACE" instead of "Spacebar".

## Tips for Best Results

- Keep tooltips short and action-focused.
- Avoid repeating the same key across multiple entries unless you want to override behavior in both contexts.
- Use consistent formatting (title case is recommended).

???+ note "Keyboard Overlay Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
    <video src="./../media/mp4/KeyboardDemo.mp4" autoplay muted playsinline loop style="max-width: 100%; border-radius: 12px;">
    </video>
    </div>

---
