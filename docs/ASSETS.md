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

# Azure / Microsoft authentication

`app/assets/js/ipcconstants.js` uses the DistrictRP Entra app (`da8eccac-4873-4d62-891d-745b5eed53ac`). Microsoft sign-in only works once Microsoft approves the app for Minecraft API access (form: https://aka.ms/mce-reviewappid, see [MicrosoftAuth.md](MicrosoftAuth.md)).
