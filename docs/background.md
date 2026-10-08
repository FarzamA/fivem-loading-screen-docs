# 🎥 Background

Set a background image, one video or a list of videos, and choose whether the video or your music is the sound. The [Config Builder](https://loadingscreen.4zam.dev/builder.html) does this for you under **Background**, with a live preview of the real loading screen.

[Open the Config Builder](https://loadingscreen.4zam.dev/builder.html){ .md-button .md-button--primary }
[Build with AI](https://loadingscreen.4zam.dev/ai.html){ .md-button }

Editing `config.json` by hand? Every option is in the Config reference: [`backgroundImage`](config-reference.md#backgroundImage), [`backgroundVideo`](config-reference.md#backgroundVideo) and [`videoAsAudio`](config-reference.md#videoAsAudio).

---

## YouTube embed requirements & error handling { #youtube-embed-requirements-error-handling }

YouTube backgrounds work in FiveM (since v1.3.0). If one will not play, the video owner's settings usually block it: it needs embedding allowed, no age restriction, no region blocks and public or unlisted visibility. When a video fails, the screen moves on to your next video or your music, and falls back to your background image if every video fails.

Step-by-step fixes are in [Troubleshooting: YouTube backgrounds](troubleshooting.md#youtube-backgrounds).

### How to fix YouTube videos that won't play {#how-to-fix-youtube-videos-that-wont-play}

See [Troubleshooting: if a YouTube video will not play](troubleshooting.md#how-to-fix-youtube-videos-that-wont-play). The most reliable option is a local `.webm` or `.mp4` file in `html/assets/`; more in [Video tips](troubleshooting.md#video-tips).
