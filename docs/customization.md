# 🎨 Customization Guide

Edit in `config.json`:

## Change overall theme color

Accepts both hex and rgb as value

```json
"selectedColor": "#ff007b",
```

## Change Background

### Image

If you prefer a static image modify the following:

```json
"backgroundImage": "./assets/path/to/background.png"
```

and leave the `backgroundVideo` blank

```json
"backgroundVideo": ""
```

Background movement and flickering effects are already in place for static images

### Video

If you prefer to have a video background modify the following

```json
"backgroundVideo": "./assets/path/to/bg.mp4"
```

Or for a YouTube video

```json
"backgroundVideo": "https://www.youtube.com/watch?v=abc123"
```

If you populate this field the `backgroundImage` paramter will be ignored

## Watermark

```json
"watermark": { 
    "label": { "text": "The Vibe RP", "colorWordCount": 2 }, 
    "subHeading": "Loading Screen", 
    "logo": "./assets/png/logo.png" 
}
```

- `text` refers to the title in the watermark
- `colorWordCount` refers to how many words in the heading will have the `selectedColor` applied to them
- `subHeading` refers to the text beneath the title
- `logo` refers to the file path to your logo image that you want to use

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

