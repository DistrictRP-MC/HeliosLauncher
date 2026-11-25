# Visual assets to replace

The repository currently ships the upstream Helios Launcher images as placeholders. Replace each file below **in place** (same path, same name); no code change is needed.

| File | Purpose | Expected format |
| ---- | ------- | --------------- |
| `build/icon.png` | Installer / app icon for all platforms (electron-builder) | PNG, square, at least 256x256 (512x512 or larger recommended) |
| `app/assets/images/SealCircle.png` | Launcher logo (landing page, window icon) | PNG, square, transparent background |
| `app/assets/images/SealCircle.ico` | Windows window/taskbar icon | ICO with 16, 32, 48, 256 px sizes |
| `app/assets/images/LoadingSeal.png` | Loading screen logo | PNG, square, transparent background |
| `app/assets/images/LoadingText.png` | Loading screen text/wordmark | PNG, transparent background |
| `app/assets/images/minecraft.icns` | macOS dock icon while the game runs | ICNS |
| `app/assets/images/backgrounds/0.jpg` ... `7.jpg` | Rotating launcher backgrounds | JPG, 1920x1080 |

Also set the social links (X, Instagram, YouTube, Discord) in `app/assets/lang/_custom.toml`; they are currently `#` placeholders marked `TODO(DistrictRP)`.

# Azure / Microsoft authentication TODO

`app/assets/js/ipcconstants.js` still uses the upstream Helios Azure client ID. Before a public release:

1. Register our own Azure application (see [MicrosoftAuth.md](MicrosoftAuth.md)).
2. Submit the Minecraft API access request form so the app is allowed to log in to Minecraft services.
3. Replace `AZURE_CLIENT_ID` in `app/assets/js/ipcconstants.js` and remove the `TODO(DistrictRP)` note.
