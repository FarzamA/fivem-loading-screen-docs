# Troubleshooting & FAQ

Most problems are fixed fastest in the [Config Builder](https://loadingscreen.4zam.dev/builder.html): import your `config.json`, check the live preview and export again. The [Build with AI](https://loadingscreen.4zam.dev/ai.html) page also has a support assistant you can ask in plain words.

---

## YouTube backgrounds { #youtube-backgrounds }

**YouTube links work as backgrounds.** Since v1.3.0 they play in game through a small player page hosted at `loadingscreen.4zam.dev`, with sound, pause and volume working as usual. Paste a normal video link; no setup is needed.

!!! info "Why this was needed"
    FiveM loads loading screens from `nui://`, which sends no Referer, so YouTube used to reject every embed with **"Error 153: video player configuration error"**. The hosted player page fixes that.

### If a YouTube video will not play { #how-to-fix-youtube-videos-that-wont-play }

The video owner's settings still apply. Check the video in **YouTube Studio > Content** and make sure it has:

- **Embedding allowed** (Video > Settings > Permissions > "Allow embedding")
- **No age restriction**
- **No region or copyright blocks**
- **Public or unlisted** visibility

Also:

- Use a link to **one video**. Playlist and channel links are not supported as backgrounds. A video link that carries playlist details (`&list=...`) plays just that video.
- The player page needs `loadingscreen.4zam.dev` to be reachable from the player's PC.

When a video cannot play, the screen moves on to your next video or to your music within about 15 seconds. If every video fails, it shows a short notice and falls back to your background image, so the screen never sits black.

!!! tip "Most reliable: a local file"
    If a video still refuses to play, download it and use a local `.webm` or `.mp4` file instead. Local files never depend on YouTube or on our player page.

---

## Video tips { #video-tips }

- **Local files are fastest.** Put the file in `html/assets/` and point to it as `./assets/background.webm`. `.webm` is the safest format for FiveM.
- **Keep files small.** A short, compressed loop loads faster for every player than a long high-bitrate video.
- **A video beats an image.** When both are set, the video plays and the image is the fallback.
- **Video or music for sound?** `videoAsAudio: true` makes the video the audio source. `false` plays it muted on loop while your music playlist plays. Left out, the video is the audio only when you have no music. See [`videoAsAudio`](config-reference.md#videoAsAudio).
- **Several videos:** give `backgroundVideo` a list and players can skip between them. See [`backgroundVideo`](config-reference.md#backgroundVideo).

---

## Common issues

### The loading screen does not show

- The folder must be named exactly `4zam_loading` and your `server.cfg` must have `ensure 4zam_loading`.
- Only one loading screen can run. Stop any other resource that declares a `loadscreen`.
- Restart the server after adding it, then reconnect.

### The loading screen does not close after spawning

The resource keeps the screen up until your game mode closes it (`loadscreen_manual_shutdown 'yes'` in `fxmanifest.lua`). Most frameworks close it automatically on spawn. If yours does not, remove that line from `fxmanifest.lua` and restart.

### My changes do not show up

- Restart the resource (`restart 4zam_loading`) or the server, then reconnect.
- Make sure `config.json` is still valid JSON: one missing comma breaks the whole file. Importing it into the [Config Builder](https://loadingscreen.4zam.dev/builder.html) shows whether it reads correctly.

### An image, video or song does not load

- Local files go in `html/assets/` and are written as `./assets/your-file.png`.
- Check the exact file name, including capital letters. Avoid spaces in file names.
- For links, use a direct `https://` link to the file itself, not to a page that shows it.

### The music player is missing

The player hides when there is nothing to play: add at least one track to `music`, or use a video as the audio source.

### Text in Arabic or Urdu

Set `language` to `ar` or `ur` and the screen's text renders right to left, with a bundled font. Your own text (rules, names, panel entries) is shown as you wrote it. See [`language`](config-reference.md#language).

---

## FAQ

**Is it free?**
Yes. The resource and the Config Builder are free.

**Does it work with my framework?**
Yes. It is a standalone loading screen, so it works with any framework.

**Can I use my own images, videos and music?**
Yes. Upload them in the builder and they are bundled into your download, or put them in `html/assets/` yourself.

**Where are all the options listed?**
In the [Config reference](config-reference.md).

**Still stuck?**
Ask the support assistant on [Build with AI](https://loadingscreen.4zam.dev/ai.html), or reach the community on the [community hub](https://thevibe.4zam.dev/).
