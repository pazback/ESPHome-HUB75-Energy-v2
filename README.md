# ESPHome-HUB75-Energy-v2

**Die nächste Generation des [ESP32-HUB75-Display](https://github.com/pazback/ESP32-HUB75-Display) Projekts.**

ESPHome-HUB75-Energy-v2 ist ein hochperformantes Energie-Dashboard für 64x32 RGB-LED-Matrizen. Es basiert auf ESPHome und visualisiert Live-Daten deiner Photovoltaik-Anlage (SMA), deines Speichers (BYD) und deines Hausverbrauchs direkt aus Home Assistant.

## 🚀 Die Evolution
Dieses Projekt ist die konsequente Weiterentwicklung der ursprünglichen C++ Version. Durch den Wechsel auf **ESPHome** bietet Version 2:
* **Native Home Assistant Integration:** Direkte Kommunikation über die API.
* **OTA-Updates:** Drahtlose Konfiguration und Updates ohne USB-Kabel.
* **Optimiertes UI:** Überarbeitete Symbole und eine Farbauswahl, die speziell auf Nachtlesbarkeit ausgelegt ist.

## 📊 Display-Layout & Icons (64x32)
Die Anzeige ist auf maximale Klarheit optimiert. Alle Werte sind rechtsbündig auf **X=42** verankert, während Icons links als visuelle Orientierung dienen.

| Sektion | Icon-Beschreibung | Farbe |
| :--- | :--- | :--- |
| **PV-Leistung** | 5-zeiliges diagonales Fluss-Muster | Gelb |
| **Netz-Leistung** | Blitz-Symbol (Bezug/Einspeisung) | Dynamisch Rot/Grün |
| **Hausverbrauch** | Herz-Symbol (Puls des Hauses) | Cyan |
| **Speicher (SOC)** | BYD-Block mit Balkenanzeige | Ampel-Logik |
| **Uhrzeit** | Große zentrierte Zeitanzeige | Amber |

## 🛠 Technische Details
### Nacht-Modus & Farbwahl
Um das typische "Ausbluten" (Blooming) von LED-Matrizen bei Nacht zu verhindern, nutzt dieses Projekt **Amber** (Bernstein) für die Uhr und ein gedimmtes **Grau** (60%) für statische Rahmen. Die Symbole wurden pixelgenau auf die Höhe der Text-Baselines optimiert.

## 📝 Einrichtung
1. Erstelle ein neues ESPHome-Device in deinem Dashboard.
2. Definiere die Farben in deiner YAML (Nutze die im Projekt hinterlegten Farbcodes).
3. Verknüpfe die Sensoren `pv_power`, `grid_power`, `house_power` und `soc` aus deiner Home Assistant Instanz.
4. Nutze das im Repo hinterlegte Lambda für die Display-Ausgabe.
5. Achte darauf, dass die IDs der Sensoren im Code exakt mit denen in deiner Konfiguration übereinstimmen.

## 📜 Lizenz

Dieses Projekt ist für den **privaten Gebrauch** freigegeben.  
Eine **kommerzielle Nutzung** (Verkauf, Integration in Produkte etc.) ist nur nach vorheriger Zustimmung des Autors erlaubt.  

Kontakt für Anfragen: bitte über GitHub oder die im Repository hinterlegte E-Mail.
