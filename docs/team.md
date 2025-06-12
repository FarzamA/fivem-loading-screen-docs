# 👥 Team Panel Configuration

The Team Panel appears on the right-hand side of the loading screen and showcases your server staff or contributors.

You can fully customize each member by editing the `teamMembers` array in your configuration file.

---

## JSON Structure

```json
"teamMembers": [
    { "name": "GucciFlipFlops", "role": "Head Developer", "discord": "pakinextdoor", "image": "./assets/png/fakalheadshot.png" }
]
```

## Field Breakdown

| **Field** | **Description**                                                                         |
| --------- | --------------------------------------------------------------------------------------- |
| `name`    | The display name for the team member (shown prominently)                                |
| `role`    | A smaller subheading to indicate their position or responsibility                       |
| `discord` | Optional field — usually a Discord username, but can be any text or label               |
| `image`   | Path to the avatar or profile picture to be shown in a circle (recommended: 1:1 aspect) |

!!! info "Adding More Members"
    To add more team members, simply add more objects inside the teamMembers array.

???+ note "Team Panel Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/TeamDemo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

---
