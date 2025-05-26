# 🏷️ Watermark Configuration

Customize the watermark that appears in the top-left corner of the loading screen.

---

## JSON Structure

```json
"watermark": { 
    "label": { "text": "The Vibe RP", "colorWordCount": 2 }, 
    "subHeading": "Loading Screen", 
    "logo": "./assets/png/logo.png" 
}
```

## Field Breakdown

| **Field**              | **Description**                                                           |
|------------------------|---------------------------------------------------------------------------|
| `label.text`           | The main title text shown in the watermark                              |
| `label.colorWordCount` | How many words get the `selectedColor` highlight from the start         |
| `subHeading`           | The text shown underneath the title                                     |
| `logo`                 | File path to your logo image                     |

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
