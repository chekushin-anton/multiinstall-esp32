# webinstall_esp32_ps4hen

PS4 HEN web installer for ESP32, based on GitHub Pages + ESP Web Tools.

## How it works

1. Push to `main`.
2. GitHub Actions compiles firmware for supported boards and deploys `flasher/` to `gh-pages`.
3. Users open the GitHub Pages site, pick a board + PS4 firmware, click Install.

## Supported boards

- ESP32-S3 (16 MB)
- ESP32-C3 Super Mini (4 MB)
- ESP32-C3 Zero (4 MB)

## After flashing

- AP SSID: `ps4hen`
- AP password: `88880000`
- Open `http://192.168.4.1`

## Local structure

- `webinstall_esp32_ps4hen/` - Arduino sketch (`webinstall_esp32_ps4hen.ino`)
- `webinstall_esp32_ps4hen/data/` - web files packed into LittleFS
- `flasher/` - GitHub Pages (installer UI + manifests)
- `.github/workflows/build.yml` - CI

## Manual build (local)

Requires `arduino-cli` and `mklittlefs` (bundled with ESP32 core).