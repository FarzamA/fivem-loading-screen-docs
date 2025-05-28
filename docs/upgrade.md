# 🔄 Upgrading to a New Version

Upgrading your loading screen is quick and easy. Just follow the steps below to safely replace the core files without affecting your custom config.json, assets, or media.

---

## 🧠 What’s Preserved

- Your config.json settings
- Custom images, audio, or videos inside html/assets/
- Any changes you've made to theme colors, rules, team, or social headers

## ⚙️ Upgrade Steps

1. Replace the HTML Entrypoint
    - Download the latest `index.html` from the `html/` folder of the new release.
    - Overwrite your existing `html/index.html` file with the new one.

2. Update Built JavaScript Assets
    - Go to your existing `html/assets/` folder.
    - Delete all `.js` files (these are the old build outputs).
    - Copy the new `.js` files from the latest release into `html/assets/`.

✅ That’s it! Your loading screen is now running the latest version.

## ⚠️ Tips & Reminders

- Do not overwrite your config.json unless the release notes explicitly say to.
- If you’ve customized core styles or components, make a backup before upgrading.
- Check the [changelog](changelog.md) for any new config options or breaking changes.

---
