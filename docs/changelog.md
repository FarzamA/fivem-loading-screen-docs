# 📦 Changelog

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
    - [Implementation Explanation](overview.md#youtube-embed-requirements-error-handling)
    - [Troubleshooting Guide](overview.md#how-to-fix-youtube-videos-that-wont-play)
- Improved detection of YouTube embed restrictions (e.g., error 153).
- Added support for custom social media icons through config 
    - [Setup Guide](socials.md#custom-icon-support)
- Added [Future Plans](future-plans.md) page

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
