# 🎨 Customization Guide

You customize the look and feel of the loading screen by editing the `config.json` file located in the `html` directory of the package. Each area has its own focused page: start here, then jump to the section you want.

> 📁 **Remember:** Place any images, videos or audio files inside the `html/assets/` folder so they load correctly in the UI.

!!! tip "Quicker in the Config Builder"
    The [Config Builder](https://loadingscreen.4zam.dev/builder.html) sets all of this with a live preview, and [Build with AI](https://loadingscreen.4zam.dev/ai.html) can set it up from a plain description. Every field with its type and default is in the Config reference: [`selectedColor`](config-reference.md#selectedColor).

---

## Overall Theme Color

Customize the main highlight UI color used across the screen:

```json
"selectedColor": "#ff007b"
```

!!! info "Color Format"
    Accepts **hex** (`#ff007b`) and `rgb()`, `rgba()`, `hsl()` or `hsla()` values. Anything else falls back to the default color.

---

## What You Can Customize

| Area | Page |
|------|------|
| 🎥 Background (image / video / playlist) | [Background](background.md) |
| 🏷️ Watermark (server name + logo) | [Watermark](watermark.md) |
| ✨ Title animation | [Title Animation](title-animation.md) |
| 🧷 Social headers & custom icons | [Social Headers](socials.md) |
| 📜 Rules panel | [Rules Panel](rules.md) |
| 👥 Team panel | [Team Panel](team.md) |
| 🖼️ Gallery grid | [Gallery Grid](gallery.md) |
| 🧩 Custom panel | [Custom Panel](custom-panel.md) |
| ⌨️ Keyboard overlay | [Keyboard Overlay](keyboard-overlay.md) |
| 🎵 Music player | [Music Player](music-player.md) |

---

---

## YouTube embed requirements & error handling { #youtube-embed-requirements-error-handling }

YouTube backgrounds work in FiveM (since v1.3.0). If one will not play, the video owner's settings usually block it: it needs embedding allowed, no age restriction, no region blocks and public or unlisted visibility. When a video fails, the screen moves on to your next video or your music, and falls back to your background image if every video fails.

Full details are on the [Background](background.md#youtube-embed-requirements-error-handling) page, and step-by-step fixes in [Troubleshooting](troubleshooting.md#youtube-backgrounds).
