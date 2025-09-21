---
name: "📦 Lansare proiect — checklist (RO)"
about: Pașii finali pentru publicare + promovare (GitHub + Home Assistant Community)
title: "Lansare proiect: ESP32‑C3 Apometre — checklist"
labels: ["project-launch", "documentation", "enhancement"]
assignees: []
---

## 🎯 Obiectiv
Finalizează repo-ul și publică proiectul pe Home Assistant Community (RO/EN).

## 🗂️ Repo housekeeping
- [ ] **Description** setat (scurt, 1-2 fraze)
- [ ] **Topics** adăugate: `ESP32-C3`, `ESPHome`, `Home-Assistant`, `water-meter`, `utility-meter`, `lovelace`, `hacs`, `bubble-card`
- [ ] **Social preview** încărcat: `images/social-banner.png`
- [ ] **LICENSE** MIT confirmat

## 📚 Documentație
- [ ] `README.md` linkează la **README.ro.md**, **README.en.md**, **STORY.ro.md**, **STORY.en.md**
- [ ] Imagini reale adăugate: `images/esp32c3-photo.jpg`, `images/bubble-card-photo.jpg`
- [ ] Verifică notele despre pini (GPIO) și **1 puls = 1 L** (sau actualizează)

## 🧪 Test: ESPHome
- [ ] Actualizează `wifi_ssid` și `wifi_password` (secrets) + `manual_ip`
- [ ] Flash `esphome/apm.yaml` și verifică în log-uri impulsurile (reed)
- [ ] Confirmă entități: `sensor.apm_*` și `binary_sensor.apm_*`

## 🏠 Test: Home Assistant
- [ ] Copiază `homeassistant/packages/apometre_mini.yaml` și **restart**
- [ ] Verifică senzori corectați: `*_total_corectat_m3`, `apa_total_m3`
- [ ] **utility_meter** zilnic/lunar populate

## 🧭 UI (Lovelace)
- [ ] Instalează **HACS** (dacă nu e instalat)
- [ ] Instalează **Bubble Card**
- [ ] Adaugă `homeassistant/lovelace/bubble_card.yaml` + pop-up-uri
- [ ] Butonul **Aplică setarea** (script) funcționează

## 🎯 Calibrare
- [ ] Introdu **odometrele mecanice** în `input_number.apa_*_setare_odometru_m3`
- [ ] Rulează scripturile de calibrare (fără spike-uri în utility_meter)

## 📣 Publicare & promovare
- [ ] Creează postarea pe **Home Assistant Community → Share your Projects** (RO + EN). Folosește șabloanele `POST-HA-RO.md` / `POST-HA-EN.md`
- [ ] Include imagini: wiring + dashboard (și, opțional, foto ESP32‑C3)
- [ ] Adaugă link către repo: `https://github.com/nagualul/esp32-water-meters-esphome-ha`

## 💡 Opțional
- [ ] Deschide **Discussions → Show and tell** cu imagini și linkuri
- [ ] Înregistrează un GIF/clip scurt cu fluxul de UI (consum + calibrare)
- [ ] Adaugă **Issue** „Good first issue” pentru contribuții (ex: refinat debounce, ghiduri pentru alte plăci)

---

> Dacă ai bifat tot, poți închide issue-ul cu `Closed as launched 🚀`.
