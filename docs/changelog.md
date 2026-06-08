# 📦 Changelog

## v1.0.9

- Added full **localization** across the loading screen, the Config Builder, and the AI assistant, in **7 languages**: English (US), English (UK), Spanish, German, French, Arabic, and Urdu. See [Language & RTL](localization.md).
    - Set the loading-screen language with a new top-level `language` field in `config.json` (for example `"language": "ar"`). Missing or unknown values stay English, so older configs are unaffected.
    - **Right-to-left (RTL) text** for **Arabic** and **Urdu**: each piece of text renders in its natural direction, with an Arabic/Urdu font bundled into the resource so it displays correctly offline. The screen keeps its normal layout (panels and watermark are not moved); physical controls such as the keyboard grid stay left-to-right by design.
    - The **Config Builder** auto-detects your browser language, adds a **Language** switcher in the settings menu, remembers your choice, and writes the language into your exported `config.json` automatically.
    - The **AI assistant replies in your language**.
    - Keyboard key-cap labels now follow `language` automatically (the existing `keyboardShortcuts.locale` still overrides).
- Added localized **per-field help hints** in the Config Builder: click the **ℹ️ info icon** next to any field to reveal a short "how to fill this" explanation inline, in your language.
- Added an **AI-translation disclaimer** in the Language menu, noting that non-English translations are AI generated.
- Added a **Terms and Conditions** page (linked from the settings menu on the builder and AI pages).

## v1.0.8

- Added a free **in-browser Config Builder** on the website: edit every `config.json` option in a visual editor with color pickers, see a **true-to-life live preview** of the loading screen as you go, and **export a ready-to-run `gucci_loading.zip`** you drop straight into your server. No more editing config blind.
    - **Paste a URL or upload a file** for any image/video/audio; uploads are bundled into the download automatically.
    - **Import** an existing `config.json`, or upload a whole `gucci_loading` folder, to keep editing it. If it references **local assets** (`./assets/...`), add those files in the import dialog and they show up in the live preview right away.
    - **Light / dark / system theme** and your work **auto-saves** in the browser so a refresh never loses it.
- Added a **Build with AI** assistant: describe your server in plain language and the assistant builds and edits your loading screen for you, live, no account needed. Includes a built-in **support assistant** that answers setup and troubleshooting questions right in the chat.
- Gave the builder and AI pages a **premium restyle**: a frosted-glass UI with a single reactive accent that follows your chosen color across the whole interface, plus higher-contrast, more readable loading-screen text over busy backgrounds.
- Added configurable **title animation** with curated presets and a sweeping sheen overlay, via `watermark.label.animation` and `watermark.label.sheen`. See [Title Animation](title-animation.md).
- Added **video as the audio source**: a background video can be driven by the built-in player (play/pause, scrub, volume).
- Added **multiple background videos (playlist)**: `backgroundVideo` now accepts an array with per-video `title`/`subtitle`, forward/back controls, and a position counter. See [Background](background.md).
- Added the `videoAsAudio` toggle with a music-aware default: with a music playlist the video is muted and the music plays; with no music the video becomes the audio source.
- Added a **Pause Video** control shown only in muted-ambient mode.
- Added **gallery lightbox navigation**: open an image and browse the gallery with on-screen arrows or the arrow keys, with position dots. See [Gallery Panel](gallery.md).
- Reorganized the documentation: split **Background** into its own page.

## v1.0.7

- Added compact keyboard localization support through `keyboardShortcuts.layout` and `keyboardShortcuts.locale`.
- Added support for multiple compact keyboard layout styles:
    - `ansi`
    - `iso`
    - `jis`
- Improved keyboard overlay rendering so layout-specific key labels can be displayed without changing the compact design.
- Added compatibility handling for symbol-based key aliases such as `~` on the top-left key.
- Added a dedicated [Custom Panel Configuration](custom-panel.md) documentation page.
- Added support for preset custom panel icons through a built-in icon registry.
- Fixed an issue where multiple custom social headers could be highlighted/selected at the same time if they shared the same `type`.
- Updated social header selection logic to use an internal runtime ID so duplicate `custom` entries now behave correctly.

## v1.0.6

- Added fixed height and scroll functionality to the team members panel.
- Added a configuration item to add custom panels to the right-hand side of the loading screen.
- Fixed parallax animation to prevent zooming in on images, which was causing weird behaviors.
- Improved parallax animation and effect.
- Cleaned up and maintained the codebase.
- Updated all asset paths to use **fivemanage** URLs for a smaller delivery package.

## v1.0.5

- Updated documentation to recommend using WebM as the preferred video format for loading screens due to better compatibility with FiveM's NUI.
- Updated `fxmanifest.lua` to include paths for importing WebM files. Ensure the correct file paths are included for WebM assets when upgrading.
- Check the [Upgrade Guide](upgrade.md) for detailed instructions on updating `fxmanifest.lua` and other changes.

## v1.0.4

- Added graceful YouTube/local video failure handling with a troubleshooting modal and docs link.
    - [Implementation Explanation](background.md#youtube-embed-requirements-error-handling)
    - [Troubleshooting Guide](background.md#how-to-fix-youtube-videos-that-wont-play)
- Improved detection of YouTube embed restrictions (e.g., error 153).
- Added support for custom social media icons through config 
    - [Setup Guide](socials.md#custom-icon-support)

## v1.0.3

- Introduced a fixed-height container with scroll support to ensure usability when the gallery contains a large number of images.
- Added the ability to fully disable the music player via configuration.
- Implemented a `defaultVolume` parameter to allow setting the initial playback volume of the music player on the loading screen.

## v1.0.2

- Fixed an issue where the UI would lose hover effects if there were too many gallery images
- Added check on gallery item count in order to disable gallery

## v1.0.1

- Fixed an issue where the UI would break if no social media options were enabled in the config.
- Made the info button label on social cards configurable via `config.json`.
- Social media buttons now open their configured links when clicked.

## v1.0.0

- Initial release
- Full keyboard overlay support
- YouTube and MP4 background support
- Configurable music player
