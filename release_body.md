## AISomniumFilesDeckFix v0.2

Steam Deck / 16:10 focused release for **AI: THE SOMNIUM FILES**.

### Changes
- Added proper UI scaling for Steam Deck's native 1280x800 resolution and other non-16:9 aspect ratios.
- The UI fix now applies whenever the configured custom resolution differs from 16:9 by more than 0.01, instead of only activating for ultrawide aspect ratios.
- Wider-than-16:9 resolutions scale affected UI horizontally.
- Narrower-than-16:9 resolutions, including 16:10, scale affected UI vertically.
- Kept the original ultrawide/custom resolution behavior and Somnium FPS cap behavior.

### Installation
- Extract the contents of the **AISomniumFilesDeckFix** zip to the **game directory**.
- Run the game.

### Recommended Steam Deck config
```ini
CustomResolution = true
ResolutionWidth = 1280
ResolutionHeight = 800
Fullscreen = false
UIFix = true
SomniumFix = true
```
