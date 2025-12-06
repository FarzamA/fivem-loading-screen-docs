# 📦 Changelog

## v1.0.4

- Added graceful YouTube/local video failure handling with a troubleshooting modal and docs link.
- Improved detection of YouTube embed restrictions (e.g., error 153).
- Added support for custom social media icons through config 
    - [Config Setup Guide](https://farzama.github.io/fivem-loading-screen-docs/socials/#custom-icon-support).

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
