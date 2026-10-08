# Install & update

The fastest path is the [Config Builder](https://loadingscreen.4zam.dev/builder.html) or [Build with AI](https://loadingscreen.4zam.dev/ai.html): design your screen, export it and you get a ready-to-run `4zam_loading` resource with your settings and files inside.

[Build yours in the browser](https://loadingscreen.4zam.dev/builder.html){ .md-button .md-button--primary }

---

## Download

Use the zip you exported from the builder, or the stock version:

1. Open the [latest release](https://github.com/FarzamA/fivem-loading-screen-docs/releases/latest).
2. Download `4zam_loading.zip`.
3. Extract it into your server's resources so the folder is `resources/4zam_loading`.

The folder name matters: it must match the `ensure` line below.

## Add to `server.cfg`

```cfg
ensure 4zam_loading
```

Then restart your server. The loading screen shows the next time a player connects.

!!! warning "Only one loading screen"
    FiveM shows one loading screen. If another resource also declares a `loadscreen` (an older loading screen, or one bundled with a framework), stop or remove it so it does not take over.

## Configuration

All settings live in one file:

```text
resources/4zam_loading/html/config.json
```

- **Easiest:** import that file into the [Config Builder](https://loadingscreen.4zam.dev/builder.html), change what you want and export again.
- **By hand:** every option is in the [Config reference](config-reference.md). Put your own images, videos and music in `html/assets/` and point to them as `./assets/your-file.webm`, or use full URLs.

After editing, restart the resource (`restart 4zam_loading`) or the server.

---

## Updating to a new version { #updating }

Your `config.json` and your own files carry over. To update:

1. **Back up** `html/config.json` and any files you added under `html/assets/`.
2. **Replace the resource:** delete the old `4zam_loading` folder and extract the new release in its place.
3. **Put your files back:** copy your `config.json` over the new one and your files back into `html/assets/`.
4. Restart the server.

Or skip the copying: import your old `config.json` into the [Config Builder](https://loadingscreen.4zam.dev/builder.html) and export a fresh resource, which always uses the latest version.

Check the [Changelog](changelog.md) for what changed. New options are optional, so an older `config.json` keeps working.

!!! info "Coming from `gucci_loading`?"
    The resource was renamed to `4zam_loading` in v1.2.0. Rename your folder to `4zam_loading` and change your `server.cfg` line to `ensure 4zam_loading`.
