# FiveM Loading Screen

A polished, fully customizable loading screen for FiveM servers: your name and colors, video or image backgrounds, music, rules, team, gallery, social links and a keybind overlay. Free to download.

**You do not need to edit any code or JSON.** Design it in your browser with a live preview, then download a ready-to-run resource.

[Build yours in the browser](https://loadingscreen.4zam.dev/builder.html){ .md-button .md-button--primary }
[Build with AI](https://loadingscreen.4zam.dev/ai.html){ .md-button .md-button--primary }

[See the live preview](https://loadingscreen.4zam.dev/){ .md-button }
[Download the latest release](https://github.com/FarzamA/fivem-loading-screen-docs/releases/latest){ .md-button }

---

## Two ways to build it

**Config Builder:** edit every option in a visual editor and watch the real loading screen update as you go. Paste links or upload your own images, videos and music; they are bundled into the download for you.

**Build with AI:** describe your server in plain words ("dark purple, our Discord and Tebex links, five rules") and the assistant builds the screen for you. Keep chatting to change anything.

Both export the same thing: a `4zam_loading` resource with your `config.json` and files already inside.

---

## Install in 3 steps

1. **Get the resource.** Export it from the [Config Builder](https://loadingscreen.4zam.dev/builder.html), or download the stock version from the [latest release](https://github.com/FarzamA/fivem-loading-screen-docs/releases/latest).
2. **Unzip it into your resources** so the folder is `resources/4zam_loading`.
3. **Add it to `server.cfg`** and restart the server:

    ```cfg
    ensure 4zam_loading
    ```

Full steps, updating and common fixes: [Install & update](setup.md) and [Troubleshooting](troubleshooting.md).

---

## Editing by hand?

Every `config.json` option is listed in the [Config reference](config-reference.md), generated from the source code so it always matches the release. You can also import an existing `config.json` into the [Config Builder](https://loadingscreen.4zam.dev/builder.html) to keep editing it visually.

---

## See the community behind the project

This loading screen was built and refined through real use on **The Vibe RP** and across the broader **The Vibe** community.

[Visit The Vibe](https://thevibe.4zam.dev/){ .md-button }
