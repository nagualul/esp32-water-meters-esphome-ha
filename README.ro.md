# Proiect contorizare apă — ESP32‑C3 + ESPHome + Home Assistant

Vezi fișierele pregătite:
- `esphome/apm.yaml` — firmware ESPHome
- `homeassistant/packages/apometre_mini.yaml` — pachet HA (offset, L/min, utility_meter, odometre)
- `homeassistant/lovelace/*.yaml` — UI (Bubble Card + pop‑up‑uri)

Instrucțiuni rapide în `README.md`. Licență MIT.


🔩 Echipamente (BOM) & link-uri (fără afiliere)

Notă: link-urile de mai jos sunt către magazine din România și sunt doar exemple.
Poți folosi echivalente din țara/regiona ta.

ESP32-C3 SuperMini (Wi-Fi/BLE) — mic, ieftin, perfect pentru ESPHome
Exemplu: https://sigmanortec.ro/placa-dezvoltare-esp32-c3-supermini-33v-wifi-bluetooth

Home Assistant (orice host) — testat pe HA Green, dar merge și pe Pi/mini-PC
Exemplu: https://www.wifistore.ro/cumpara/home-assistant-green-84102

(Opțional) Dongle ZigBee (Sonoff ZBDongle-E) — nu e necesar pentru proiectul ăsta; folosim Wi-Fi via ESPHome
Exemplu: https://www.vonmag.ro/produse/info/zbdongle-e-6920075777659-pret-gateway-zigbee-30-usb-dongle-plus-e-sonoff

Apometre cu contact reed (contact uscat) — orice brand/model e ok
Exemple (RO):
Apă caldă: https://www.emag.ro/contor-de-apa-zenner-etwd-apa-calda-1-2-kxg0190904/pd/D7560TMBM/

Apă rece: https://www.emag.ro/contor-de-apa-zenner-etkd-apa-rece-1-2-kxg0190903/pd/DD560TMBM/

Compatibilitate: e suficient ca apometrul să aibă contact reed.
Dacă scara e 1 impuls = 10 L (sau altă valoare), ajustezi incrementul în on_press (ESPHome) și conversia în m³ în pachet.
