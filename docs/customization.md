# 🎨 Customization Guide

You can customize the look and feel of the loading screen by editing the `config.json` file located in the `html` directory of the package. This guide walks you through the most important configuration options.

> 📁 Place any images, videos, or audio files inside the `html/assets/` folder to ensure they load correctly in the UI.


## Overall Theme Color

Customize the main highlight color used throughout the UI:

```json
"selectedColor": "#ff007b",
```

!!! info "Color Format"
    Accepts both hex and RGB formats.

## Background Options

You can use either a static image or a video background. If both are set, video will take priority.

### 📷 Static Image

```json
"backgroundImage": "./assets/path/to/background.png",
"backgroundVideo": ""
```

!!! info "Static Image Notes"
    If you're using a static image, leave `"backgroundVideo"` empty.  
    Subtle flickering and movement effects will still apply to the image for visual depth.

### 🎥 Video Background (MP4)

```json
"backgroundVideo": "./assets/path/to/bg.mp4"
```

### 📺 Video Background (YouTube)

```json
"backgroundVideo": "https://www.youtube.com/watch?v=abc123"
```

!!! info "Video Takes Priority"
    If `"backgroundVideo"` is set, the static `"backgroundImage"` will be ignored.

---