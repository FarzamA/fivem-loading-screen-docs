# 👥 Team Panel Configuration

The Team Panel appears on the right-hand side of the loading screen and showcases your server staff or contributors.

You can fully customize each member by editing the `teamMembers` array in your configuration file.

!!! tip "Quicker in the Config Builder"
    The [Config Builder](https://loadingscreen.4zam.dev/builder.html) sets all of this under **Team** with a live preview, and [Build with AI](https://loadingscreen.4zam.dev/ai.html) can set it up from a plain description. Every field with its type and default is in the Config reference: [`teamMembers`](config-reference.md#teamMembers).

---

## JSON Structure

```json
"teamMembers": [
    { "name": "GucciFlipFlops", "role": "Head Developer", "discord": "pakinextdoor", "image": "./assets/png/fakalheadshot.png" }
]
```

## Field Breakdown

Each member takes `name` (shown prominently), `role` (a smaller line under it), `discord` (usually a Discord username, but any short label works) and `image` (shown in a circle, so a square 1:1 picture looks best). Types are in the [Config reference](config-reference.md#teamMembers).

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
