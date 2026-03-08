# 🧩 Custom Panel Configuration

Custom panels let you add your own fully customizable tabs to the loading screen.  
Use them for updates, server info, guides, economy details, jobs, starter tips, store links, whitelist info, or any other structured content you want players to see while loading in.

---

## JSON Structure

```json
"customPanels": [
    {
        "panelPosition": 1,
        "uniqueId": "updates",
        "buttonLabel": "Updates",
        "icon": "bullhorn",
        "cardHeaderLabel": "Latest City Updates",
        "singularLabel": "Update",
        "entries": [
            "Daily job based quests with reward system",
            "Loot boxes with provable fairness and security",
            "New 200+ lore friendly vehicles added with more on the way"
        ]
    }
]
```

---

## Field Breakdown

| **Field**          | **Description** |
|-------------------|-----------------|
| `panelPosition`   | Determines where the custom panel button appears in the tab row. Lower numbers appear earlier. |
| `uniqueId`        | Unique internal ID used to identify the panel. Must be different for every custom panel. |
| `buttonLabel`     | Text shown on the panel button in the header. |
| `icon`            | Icon used for the panel button. Can be a preset icon name, `fa-` prefixed icon name, image path, image URL, or inline SVG string. |
| `cardHeaderLabel` | Main heading shown at the top of the panel content. |
| `singularLabel`   | Label used for each item in the panel list (for example `Update`, `Rule`, `Tip`, `Guide`). |
| `entries`         | Array of strings displayed inside the panel body. Each string becomes one list item / content entry. |

!!! info "Multiple Custom Panels Supported"
    You can add as many custom panels as you want by adding more objects to the `customPanels` array.

!!! warning "Unique IDs Must Be Unique"
    Every custom panel must use a different `uniqueId`. Reusing the same ID can cause the wrong panel to be opened or rendered.

---

## Example: Multiple Custom Panels

```json
"customPanels": [
    {
        "panelPosition": 1,
        "uniqueId": "updates",
        "buttonLabel": "Updates",
        "icon": "bullhorn",
        "cardHeaderLabel": "Latest City Updates",
        "singularLabel": "Update",
        "entries": [
            "Daily job based quests with reward system",
            "New 200+ lore friendly vehicles added with more on the way",
            "Vehicle rarity system with Discord webhook integrations"
        ]
    },
    {
        "panelPosition": 3,
        "uniqueId": "starter-guide",
        "buttonLabel": "Starter Guide",
        "icon": "book",
        "cardHeaderLabel": "Getting Started",
        "singularLabel": "Tip",
        "entries": [
            "Visit City Hall first to pick up your starter items",
            "Use the radial menu to access quick actions",
            "Join the Discord for announcements and support"
        ]
    }
]
```

---

## Panel Order (`panelPosition`)

`panelPosition` controls where the button appears in the header row.

### Example

```json
"customPanels": [
    {
        "panelPosition": 1,
        "uniqueId": "updates",
        "buttonLabel": "Updates",
        "icon": "bullhorn",
        "cardHeaderLabel": "Latest City Updates",
        "singularLabel": "Update",
        "entries": ["Example update"]
    },
    {
        "panelPosition": 2,
        "uniqueId": "guide",
        "buttonLabel": "Guide",
        "icon": "book",
        "cardHeaderLabel": "Starter Guide",
        "singularLabel": "Tip",
        "entries": ["Example tip"]
    }
]
```

In this example:

- `Updates` appears before `Guide`
- lower `panelPosition` values are placed earlier
- each position should ideally be unique for best results

!!! tip "Recommended Usage"
    Use simple values like `1`, `2`, `3`, `4`, etc. to keep tab ordering predictable and easy to manage.

---

## Choosing a `uniqueId`

The `uniqueId` is used internally by the loading screen to track which custom panel is being opened.

### Recommended format

- lowercase
- no spaces
- use hyphens if needed

### Good examples

- `updates`
- `starter-guide`
- `city-rules`
- `economy-info`

### Avoid

- duplicate IDs
- IDs with spaces
- changing IDs frequently after release unless necessary

!!! tip "Best Practice"
    Treat `uniqueId` like an internal key, not a visible label. Players will see `buttonLabel`, not `uniqueId`.

---

## Supported Icon Types

The `icon` field supports several formats.

### 1. Preset icon names (recommended)

These are the easiest to use and are the best option for most servers.

#### Example

```json
"icon": "bullhorn"
```

### Supported preset icon names

- `bullhorn`
- `users`
- `image`
- `circle`
- `star`
- `shield`
- `shield-halved`
- `gavel`
- `briefcase`
- `wrench`
- `screwdriver-wrench`
- `tools`
- `car`
- `house`
- `home`
- `store`
- `shop`
- `gift`
- `crown`
- `music`
- `newspaper`
- `globe`
- `handshake`
- `trophy`
- `flag`
- `bolt`
- `heart`
- `bell`
- `map`
- `book`
- `scroll`
- `list`
- `gear`
- `cog`
- `hammer`
- `info`
- `circle-info`
- `clipboard`
- `comments`
- `phone`
- `wallet`

!!! note "Preset Icons Are Preferred"
    Preset icon names are the easiest option to document, maintain, and style consistently.

---

### 2. `fa-` prefixed preset names

You may also use the same preset names with the `fa-` prefix.

#### Example

```json
"icon": "fa-bullhorn"
```

This works the same as:

```json
"icon": "bullhorn"
```

---

### 3. Custom image path or URL

You can use a local asset path or external image URL instead of a preset icon name.

#### Example: Local asset

```json
"icon": "./assets/icons/store.png"
```

#### Example: External URL

```json
"icon": "https://your-cdn.com/icons/store-icon.png"
```

Supported image formats include:

- `.png`
- `.jpg`
- `.jpeg`
- `.gif`
- `.webp`
- `.svg`

!!! warning "Use Small, Clean Icons"
    Custom icon images should be square or close to square for best visual results inside the header button.

---

### 4. Inline SVG string

Inline SVG is also supported.

#### Example

```json
"icon": "<svg viewBox='0 0 24 24' fill='currentColor'><path d='...'/></svg>"
```

!!! warning "Advanced Usage"
    Inline SVG is intended for advanced users. Most server owners should use a preset icon name or image path instead.

---

## Fallback Behavior

If the `icon` value is invalid or unsupported, the loading screen falls back to the default icon.

!!! note "Fallback Icon"
    Invalid panel icons automatically fall back to the default icon instead of breaking the UI.

---

## Example: Preset Icon

```json
"customPanels": [
    {
        "panelPosition": 2,
        "uniqueId": "economy",
        "buttonLabel": "Economy",
        "icon": "wallet",
        "cardHeaderLabel": "City Economy Info",
        "singularLabel": "Detail",
        "entries": [
            "Starter cash is provided when you first join",
            "Jobs and side hustles are the best way to build income",
            "Illegal routes carry higher risk and reward"
        ]
    }
]
```

---

## Example: Custom Image Icon

```json
"customPanels": [
    {
        "panelPosition": 2,
        "uniqueId": "store",
        "buttonLabel": "Store",
        "icon": "./assets/icons/store.png",
        "cardHeaderLabel": "Support the Server",
        "singularLabel": "Perk",
        "entries": [
            "Vehicle packs available in the store",
            "Exclusive cosmetic rewards available",
            "Check the store for supporter packages"
        ]
    }
]
```

---

## Tips for Best Results

- Keep `buttonLabel` short so it fits nicely in the animated header buttons.
- Keep `cardHeaderLabel` descriptive and readable.
- Use a clear `singularLabel` that matches the purpose of the panel.
- Keep entries short enough to scan quickly during loading.
- Use preset icons whenever possible for the cleanest look.
- Use unique `panelPosition` values for predictable ordering.
- Use unique, stable `uniqueId` values.

---

## Recommended Icon Formats for Custom Image Icons

For best results:

- SVG (preferred)
    - Sharp at any size
    - Great for logos and simple icons
    - Small file size

- PNG (transparent background preferred)
    - Best for custom branded icons
    - Clean presentation inside the header buttons

- JPEG / JPG (supported but not ideal)
    - Works, but transparency is not supported
    - Usually less suitable for compact icon buttons

Avoid:

- low-resolution images
- very wide logos
- very tall aspect ratios
- images with large solid backgrounds
- photos instead of icon-style graphics

---

## Full Example

```json
"customPanels": [
    {
        "panelPosition": 1,
        "uniqueId": "updates",
        "buttonLabel": "Updates",
        "icon": "bullhorn",
        "cardHeaderLabel": "Latest City Updates",
        "singularLabel": "Update",
        "entries": [
            "Daily job based quests with reward system",
            "Loot boxes with provable fairness and security",
            "New 200+ lore friendly vehicles added with more on the way",
            "Vehicle rarity system with Discord webhook integrations"
        ]
    },
    {
        "panelPosition": 2,
        "uniqueId": "guide",
        "buttonLabel": "Guide",
        "icon": "book",
        "cardHeaderLabel": "Starter Guide",
        "singularLabel": "Tip",
        "entries": [
            "Visit City Hall first to collect your starter items",
            "Use the radial menu for quick access to important features",
            "Join the Discord to stay up to date on events and support"
        ]
    },
    {
        "panelPosition": 3,
        "uniqueId": "store",
        "buttonLabel": "Store",
        "icon": "./assets/icons/store.png",
        "cardHeaderLabel": "Support the Server",
        "singularLabel": "Perk",
        "entries": [
            "Store packages help support development",
            "Exclusive cosmetic rewards are available",
            "Visit the store for the latest supporter options"
        ]
    }
]
```

---

<!-- ???+ note "Custom Panel Preview"
    Add a screenshot or short preview video here showing multiple custom panels in the header. -->

---
