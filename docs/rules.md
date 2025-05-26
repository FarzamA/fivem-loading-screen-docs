# 📜 Rules Panel Configuration

The rules panel appears on the right-hand side of the loading screen and displays your server’s key guidelines.

You can fully customize these rules by modifying the `rules` array in your config file.

---

## JSON Structure

```json
"rules": [
    "No griefing or trolling other players.",
    "Respect all admins and staff decisions.",
    "No hacking, exploiting, or modding\nin unfair ways.",
    "Keep your behavior mature\nand respectful at all times.",
    "Do not spam the chat\nor use slurs or hate speech."
]
```

Each entry in the array represents one rule.
You can use \n inside strings to create intentional line breaks.

!!! info "Formatting Notes"
    - Add each rule as a quoted string inside the array.
    - You can insert \\n for line breaks in longer rules.

## Suggested Limit

!!! info "How Many Rules?"
    It's recommended to display no more than 5–6 rules to keep the panel readable and visually clean.

You’re free to experiment with more, but longer lists may appear cluttered depending on your screen layout and font size.

???+ note "Rules Panel Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/RulesDemo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

---
