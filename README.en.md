# Water metering project — ESP32‑C3 + ESPHome + Home Assistant

Ready files:
- `esphome/apm.yaml` — ESPHome firmware
- `homeassistant/packages/apometre_mini.yaml` — HA package (offsets, L/min, utility meters, odometers)
- `homeassistant/lovelace/*.yaml` — UI (Bubble Card + pop‑ups)

Quick instructions in `README.md`. MIT license.


🔩 Hardware (BOM) & example links (non-affiliate)

Note: the links below point to Romanian retailers and are provided as examples only.
You can use any equivalent parts available in your country/region.

ESP32-C3 SuperMini (Wi-Fi/BLE) — small, cheap, works great with ESPHome
Example: https://sigmanortec.ro/placa-dezvoltare-esp32-c3-supermini-33v-wifi-bluetooth

Home Assistant (any host) — tested with HA Green, but a Pi/mini-PC works too
Example: https://www.wifistore.ro/cumpara/home-assistant-green-84102

(Optional) ZigBee USB dongle (Sonoff ZBDongle-E) — not required for this project; Wi-Fi via ESPHome is used
Example: https://www.vonmag.ro/produse/info/zbdongle-e-6920075777659-pret-gateway-zigbee-30-usb-dongle-plus-e-sonoff

Water meters with reed switch (dry contact) — any brand/model is fine
Examples (RO):
Hot: https://www.emag.ro/contor-de-apa-zenner-etwd-apa-calda-1-2-kxg0190904/pd/D7560TMBM/

Cold: https://www.emag.ro/contor-de-apa-zenner-etkd-apa-rece-1-2-kxg0190903/pd/DD560TMBM/

Compatibility: any meter that exposes a reed contact will work.
If your meter produces 1 pulse = 10 L (or another scale), just change the on_press increment in ESPHome and the m³ conversion in the package.

