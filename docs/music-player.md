# 🎵 Music Player Configuration

The Music Player plays a rotating playlist during the loading screen, complete with track titles, artist names and optional cover art.

Customize your music experience by modifying the `music` array in your configuration file.

!!! tip "Quicker in the Config Builder"
    The [Config Builder](https://loadingscreen.4zam.dev/builder.html) sets all of this under **Music** with a live preview, and [Build with AI](https://loadingscreen.4zam.dev/ai.html) can set it up from a plain description. Every field with its type and default is in the Config reference: [`music`](config-reference.md#music) and [`defaultVolume`](config-reference.md#defaultVolume).

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

Each track takes `path` (the `.mp3` file), `title`, `artist` and an optional `image` for cover art (`null` when unused). Types are in the [Config reference](config-reference.md#music).

!!! info "Audio Format Support"
    Only .mp3 files are supported at this time. Make sure all audio files are properly encoded and placed under assets/mp3/.

!!! info "Track Rotation"
    Tracks rotate automatically in order. The player includes play, pause, skip and volume control functionality.

!!! info "Playlist Counter"
    When more than one track is configured, a small position counter (e.g. `2 / 5`) appears at the top-right of the player card.

## Doubles as the Video Controller

When a background video is the audio source (`videoAsAudio: true`, or left out with no `music` playlist), this same player controls the **video** instead of the mp3 playlist: play/pause, scrub and volume all drive the video, and the "now playing" text comes from each video's `title` / `subtitle`. With multiple videos, the forward/back buttons and the position counter work just like the music playlist.

See [Background](background.md) for how to configure single or multiple background videos and the `videoAsAudio` toggle.

!!! info "When does the player show?"
    The player appears when there is an mp3 playlist **or** a video acting as the audio source. In muted-ambient mode (`videoAsAudio: false`) the player controls the mp3 playlist while the video loops silently behind it.

## Optional Album Art

If you'd like to show cover art or thumbnails per track, provide the `image` field:

```json
"image": "./assets/path/to/cover_art.png"
```

Image files should ideally be square (1:1 aspect ratio) and under 500KB for fast load times.

## Optional Default Volume Setting

To set the initial volume level of the music player, add the following entry to your config:

```json
"defaultVolume": 100
```

This value accepts a number from 0 to 100, representing the percentage volume on first load.

???+ note "Music Player UI Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
    <video src="./../media/mp4/MusicDemo.mp4" autoplay muted playsinline loop style="max-width: 100%; border-radius: 12px;">
    </video>
    </div>

!!! warning "Automatic Music Player Hiding"
    The music player tab is automatically hidden if the music array is empty ([ ]) or omitted entirely from the config.
    To disable the music player, simply remove the music entry or ensure the array contains no entries.

---
