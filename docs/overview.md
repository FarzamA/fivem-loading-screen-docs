# 🎨 Customization Guide

Customizing the loading screen means filling in its `config.json`. The [Config Builder](https://loadingscreen.4zam.dev/builder.html) does this for you, with a live preview of the real loading screen.

[Open the Config Builder](https://loadingscreen.4zam.dev/builder.html){ .md-button .md-button--primary }
[Build with AI](https://loadingscreen.4zam.dev/ai.html){ .md-button }

Editing `config.json` by hand? Every option is in the Config reference: [`selectedColor`](config-reference.md#selectedColor), [`backgroundVideo`](config-reference.md#backgroundVideo), [`watermark`](config-reference.md#watermark), [`socialHeaders`](config-reference.md#socialHeaders), [`customPanels`](config-reference.md#customPanels) and [`music`](config-reference.md#music).

---

## YouTube embed requirements & error handling { #youtube-embed-requirements-error-handling }

YouTube backgrounds work in FiveM (since v1.3.0). If one will not play, the video owner's settings usually block it: it needs embedding allowed, no age restriction, no region blocks and public or unlisted visibility. When a video fails, the screen moves on to your next video or your music, and falls back to your background image if every video fails.

Step-by-step fixes are in [Troubleshooting: YouTube backgrounds](troubleshooting.md#youtube-backgrounds).
