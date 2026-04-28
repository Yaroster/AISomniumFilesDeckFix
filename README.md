# AI: THE SOMNIUM FILES Fix
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/W7W01UAI9)</br>
[![Github All Releases](https://img.shields.io/github/downloads/Lyall/AISomniumFilesFix/total.svg)]()

This WIP BepInEx plugin for the game **AI: THE SOMNIUM FILES** adds support for:
- Playing the game at non-16:9 aspect ratios, including Steam Deck / 16:10, 21:9, 32:9 or even higher.
- Fixing various UI issues caused by running at unsupported resolutions.
- Automatic FPS capping during somnium scenes. ([PCGW article.](https://www.pcgamingwiki.com/wiki/AI:_The_Somnium_Files#Visual_artifacts_in_somnium_scenes))
- Setting an arbitrary resolution.

## Installation
- Grab the [latest release of AISomniumFilesFix.](https://github.com/Lyall/AISomniumFilesFix/releases)
- Extract the contents of the **AISomniumFilesFix** zip to the **game directory**.
- Run the game.

## Configuration
- See the generated config file **AISomniumFilesFix.cfg** in the **Mod** folder to adjust various aspects of the mod.

### Steam Deck / 16:10
This fork adds proper support for the Steam Deck's native **1280x800** resolution and other non-16:9 aspect ratios when using the custom resolution patch.

The original UI fix only activated for ultrawide aspect ratios above `1.8`. On Steam Deck, `1280x800` is `16:10` with an aspect ratio of `1.6`, so the custom camera resolution patch could run without the matching UI/scaler fix. This could cause broken framing or black space, especially in Investigation scenes.

Recommended Steam Deck config:

```ini
CustomResolution = true
ResolutionWidth = 1280
ResolutionHeight = 800
Fullscreen = false
UIFix = true
SomniumFix = true
```

The UI fix now applies to any configured resolution that differs from `16:9` by more than `0.01`. Wider-than-16:9 resolutions scale affected UI on X, while narrower-than-16:9 resolutions, including Steam Deck / 16:10, scale affected UI on Y. Somnium FPS behavior is unchanged from the original fix.

## Known Issues
Please report any issues you see and I'll do my best to fix them.
- This fix is very much a work-in-progress. It may break or fail to function in certain scenes.

## Screenshots
![ezgif-5-0ee8d90fe6](https://user-images.githubusercontent.com/695941/178378798-bf0cd20f-8501-4e79-9892-aa121edad762.gif)

## Credits
- [MelonLoader](https://github.com/LavaGang/MelonLoader) is licensed under the Apache License, Version 2.0. See [LICENSE](https://github.com/LavaGang/MelonLoader/blob/master/LICENSE.md) for the full License.
