# 🎵 Music Player Configuration

The Music Player plays a rotating playlist during the loading screen, complete with track titles, artist names, and optional cover art.

Customize your music experience by modifying the `music` array in your configuration file.

---

## JSON Structure

```json
"music": [
  {
    "path": "./assets/mp3/1008gs.mp3",
    "title": "1008 Grams",
    "artist": "OT7 Quanny",
    "image": null
  }
]
```

## Field Breakdown

| **Field** | **Description**                                                                           |
| --------- | ----------------------------------------------------------------------------------------- |
| `path`    | Path to the `.mp3` audio file to be played                                                |
| `title`   | Display title for the track (shown in the UI)                                             |
| `artist`  | Display artist name                                                                       |
| `image`   | (Optional) Path to an image or album art to show for this track (set to `null` if unused) |

!!! info "Audio Format Support"
    Only .mp3 files are supported at this time. Make sure all audio files are properly encoded and placed under assets/mp3/.

!!! info "Track Rotation"
    Tracks rotate automatically in order. The player includes play, pause, skip, and volume control functionality.

## Optional Album Art

If you'd like to show cover art or thumbnails per track, provide the `image` field:

```json
"image": "./assets/path/to/cover_art.png"
```

Image files should ideally be square (1:1 aspect ratio) and under 500KB for fast load times.

???+ note "Music Player UI Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
    <video src="./../media/mp4/MusicDemo.mp4" autoplay muted playsinline loop style="max-width: 100%; border-radius: 12px;">
    </video>
    </div>

---
