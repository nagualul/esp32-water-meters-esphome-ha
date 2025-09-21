# ESP32-C3 Water Meters (Hot + Cold) — ESPHome + Home Assistant

Minimal, robust setup to read two reed switches from hot/cold water meters with an ESP32‑C3 SuperMini and expose totals (L and m³), rates (L/min), and utility meters (daily/monthly) in Home Assistant. UI uses Bubble Card.

## Quick start
1. Flash ESP32‑C3 with `esphome/apm.yaml` (update Wi‑Fi + static IP).
2. Drop `homeassistant/packages/apometre_mini.yaml` into your HA config and restart.
3. Add the Lovelace examples from `homeassistant/lovelace/` (requires HACS + Bubble Card).
4. Calibrate using the pop‑ups (set mechanical odometer and **Apply**).

## Docs
- 🇷🇴 Romanian: `README.ro.md`
- 🇬🇧 English: `README.en.md`

## Folder layout
See the `homeassistant/` and `esphome/` subfolders for ready-to-use YAML.
Images for wiring/UI are under `images/`.

## License
MIT — see `LICENSE`.


## Story
- 🇷🇴 [Povestea proiectului](STORY.ro.md)
- 🇬🇧 [Build story](STORY.en.md)
![ESP32-C3](images/esp32c3-photo.jpg)
![Lovelace – Bubble Card](images/bubble-card-photo.jpg)
