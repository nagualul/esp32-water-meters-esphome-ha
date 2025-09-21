---
name: "📦 Project launch — checklist (EN)"
about: Final steps for publishing + promotion (GitHub + Home Assistant Community)
title: "Project launch: ESP32‑C3 Water Meters — checklist"
labels: ["project-launch", "documentation", "enhancement"]
assignees: []
---

## 🎯 Goal
Finish the repo and publish the project on Home Assistant Community (RO/EN).

## 🗂️ Repo housekeeping
- [ ] Set **Description** (short, 1–2 sentences)
- [ ] Add **Topics**: `ESP32-C3`, `ESPHome`, `Home-Assistant`, `water-meter`, `utility-meter`, `lovelace`, `hacs`, `bubble-card`
- [ ] Upload **Social preview**: `images/social-banner.png`
- [ ] Confirm **MIT LICENSE**

## 📚 Documentation
- [ ] `README.md` links to **README.ro.md**, **README.en.md**, **STORY.ro.md**, **STORY.en.md**
- [ ] Real images added: `images/esp32c3-photo.jpg`, `images/bubble-card-photo.jpg`
- [ ] Verify the pin notes (GPIO) and **1 pulse = 1 L** (or update)

## 🧪 Test: ESPHome
- [ ] Update `wifi_ssid` / `wifi_password` (secrets) + `manual_ip`
- [ ] Flash `esphome/apm.yaml` and watch reed pulses in logs
- [ ] Confirm entities: `sensor.apm_*` and `binary_sensor.apm_*`

## 🏠 Test: Home Assistant
- [ ] Copy `homeassistant/packages/apometre_mini.yaml` and **restart**
- [ ] Verify corrected sensors: `*_total_corectat_m3`, `apa_total_m3`
- [ ] **utility_meter** daily/monthly accumulate properly

## 🧭 UI (Lovelace)
- [ ] Install **HACS** (if not installed)
- [ ] Install **Bubble Card**
- [ ] Add `homeassistant/lovelace/bubble_card.yaml` + the pop-ups
- [ ] The **Apply setting** script works

## 🎯 Calibration
- [ ] Enter **mechanical odometers** in `input_number.apa_*_setare_odometru_m3`
- [ ] Run calibration scripts (no spikes in utility_meter)

## 📣 Publish & promote
- [ ] Post on **Home Assistant Community → Share your Projects** (RO + EN). Use `POST-HA-RO.md` / `POST-HA-EN.md`
- [ ] Include images: wiring + dashboard (and optional ESP32‑C3 photo)
- [ ] Add repo link: `https://github.com/nagualul/esp32-water-meters-esphome-ha`

## 💡 Optional
- [ ] Open a **Discussions → Show and tell** with pics and links
- [ ] Record a short GIF/clip of the UI flow (usage + calibration)
- [ ] Add a **Good first issue** for contributors (e.g., debounce tuning, guides for other boards)

---

> Once all boxes are checked, close this issue with `Closed as launched 🚀`.
