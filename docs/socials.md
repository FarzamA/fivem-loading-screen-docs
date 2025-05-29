# 🧷 Social Header Configuration

You can customize the social header cards that appear at the top of the loading screen. These cards allow users to quickly join your Discord, visit your Instagram, or check out other platforms.

---

## JSON Structure

```json
"socialHeaders": [
    { 
        "type": "discord", 
        "cardLabel": "Discord Server", 
        "cardInfo": "Join the discord to keep up with the latest on the FiveM server!", 
        "link": "https://discord.gg/dbFChqBh5u", 
        "buttonLabel": "Join",
        "enabled": true 
    }
]
```

## Field Breakdown

| **Field**     | **Description**                                            |
| ------------- | ---------------------------------------------------------- |
| `type`        | Platform type (used to display the appropriate icon)       |
| `cardLabel`   | The card's main title/header text                          |
| `cardInfo`    | Description shown below the header                         |
| `link`        | URL that opens when the "Join" or action button is clicked |
| `buttonLabel` | Label of "Join" or action button                           |
| `enabled`     | Whether to show this social card on the loading screen     |

!!! info "Multiple Platforms Supported"
    You can include multiple social cards by adding more objects to the socialHeaders array.

## Supported `type` values

- discord
- instagram
- telegram
- youtube
- tiktok

!!! warning "Spelling Matters"
    The type value must be lowercase and spelled exactly as shown above to display the correct icon.

???+ note "Social Media Card Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/SocialDemo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

---
