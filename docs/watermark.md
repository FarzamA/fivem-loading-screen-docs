# 🏷️ Watermark Configuration

Customize the watermark that appears in the top-left corner of the loading screen.

!!! tip "Quicker in the Config Builder"
    The [Config Builder](https://loadingscreen.4zam.dev/builder.html) sets all of this under **Brand & Color** with a live preview, and [Build with AI](https://loadingscreen.4zam.dev/ai.html) can set it up from a plain description. Every field with its type and default is in the Config reference: [`watermark`](config-reference.md#watermark).

---

## JSON Structure

```json
"watermark": { 
    "label": { "text": "The Vibe RP", "colorWordCount": 2, "animation": "wave", "sheen": true }, 
    "subHeading": "Loading Screen", 
    "logo": "./assets/png/logo.png" 
}
```

## Field Breakdown

Every field (`label.text`, `label.colorWordCount`, `label.animation`, `label.sheen`, `subHeading`, `logo`) with its type and default is in the [Config reference](config-reference.md#watermark). The logo can be a URL or a path inside the resource such as `./assets/png/logo.png`.

!!! tip "Animating the title"
    `label.animation` and `label.sheen` control how the title moves and shines. See the [Title Animation](title-animation.md) page for the full preset list.

!!! info "Color Tip"
    The colorWordCount applies the highlight color to that number of starting words in the label.text.

???+ note "Watermark Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/WatermarkDemo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

---
