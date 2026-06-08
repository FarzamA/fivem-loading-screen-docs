# 🌐 Language & Right-to-Left (RTL)

The loading screen, the in-browser **Config Builder**, and the **Build with AI** assistant are fully localized. Pick the language your community speaks and the whole experience follows, including full right-to-left layout for Arabic and Urdu.

---

## Supported languages

| Code | Language | Direction |
|------|----------|-----------|
| `en` | English (US) — default | LTR |
| `en-GB` | English (UK) | LTR |
| `es` | Español (Spanish) | LTR |
| `de` | Deutsch (German) | LTR |
| `fr` | Français (French) | LTR |
| `ar` | العربية (Arabic) | RTL |
| `ur` | اردو (Urdu) | RTL |

English (US) is the default and the fallback: if a translation is ever missing, the English text is shown rather than a blank or a raw key.

---

## Setting the loading-screen language

Add a top-level `language` field to your `config.json`. Every player connecting to your server sees the loading screen in that language.

```json
{
    "language": "ar",
    "selectedColor": "#7C3AED",
    "...": "rest of your config"
}
```

- Set it to any code from the table above.
- For `ar` or `ur` the screen automatically switches to **right-to-left** layout.
- If `language` is missing or not recognized, the screen stays **English (LTR)** — so existing configs from older versions keep working unchanged.

!!! tip "Building in the Config Builder?"
    You usually do not need to edit this by hand. The builder sets `language` for you (see below).

---

## In the Config Builder and AI assistant

Open the [Config Builder](https://fivem-loading.vercel.app/builder.html) or [Build with AI](https://fivem-loading.vercel.app/ai.html):

- The interface **auto-detects your browser language** on first visit.
- A **Language** option in the settings (gear) menu lets you switch at any time, and your choice is remembered.
- The **AI assistant replies in your language** — describe your server in Arabic, Spanish, German, etc. and it answers in kind.
- Every field has a localized **help hint**: click the small **ℹ️ info icon** next to a label to reveal a short "how to fill this" explanation inline, in your language. Click again to hide it.
- When you **export**, the language you are building in is written into your `config.json` automatically, so the loading screen ships in the same language. You can always change the `language` field afterward.

!!! note "About non-English translations"
    The interface translations are AI generated and reviewed, and may not be perfect. The **Language** menu notes this, and the [Terms and Conditions](https://fivem-loading.vercel.app/terms.html) are provided in English, which is the authoritative version.

---

## Right-to-left text (Arabic & Urdu)

Setting the language to `ar` or `ur` makes the **text** render correctly right-to-left in each component, while keeping the screen's normal layout:

- Each piece of text (chrome and your own content) is shown in its natural direction. Arabic/Urdu reads right-to-left and right-aligns; Latin text stays left-to-right.
- An Arabic/Urdu font is **bundled** with the resource, so text renders correctly even if the player's machine has no Arabic font installed.
- Your own content (rules, team names, panel text) is shown **as you wrote it**, in the correct direction.

Language does **not** move the panels or watermark - it only fixes the text. The screen keeps its normal layout.

---

## Keyboard

The keyboard overlay adapts to your `language` automatically:

- **Key-cap labels** (Shift, Enter, Ctrl, etc.) are translated. The keys never change size for longer translations, so the layout never breaks.
- **Physical layout** follows the language: German shows **QWERTZ**, French shows **AZERTY**, and the rest use **QWERTY**. The letters sit where that language's real keyboard puts them.

If you ever want to pin a specific key-cap language regardless of `language`, the `keyboardShortcuts.locale` field still works as an override. In the Config Builder you no longer type key names by hand: click a keybind's key field and **press the actual key** on your keyboard, and it is filled in for you. See [Keyboard Overlay](keyboard-overlay.md).

---

## What is and isn't translated

- **Translated:** all of the product's own interface text — buttons, labels, status text, dialogs, the AI assistant's replies.
- **Not translated:** the content *you* write — your server rules, team member names and roles, social card text, track titles, panel entries. Those stay exactly as you enter them (and display correctly in RTL).

---

## Adding a language

The architecture is built so a new language is a single file. If you would like to contribute one (or request one), reach out on the [community Discord](https://thevibe.mooo.com/) — a new locale is one translation file plus one line in the locale registry, with no other code changes.
