🌀 TCL Air Conditioner Integration for Home Assistant

Translated with ChatGPT – successfully tested with TCL TAC-12CHDA
Simple DIY project using ESP32 + USB cable. No cloud required.

---

🛠️ What You Need
	•	ESP32 (e.g., ESP32-C3, WROOM32, NodeMCU)
	•	USB-A plug or cable
👉 I used this one: AliExpress Link
	•	Home Assistant with ESPHome (version 2023.3.0 or later)


---

## 🔌 Wiring

| USB-A Pin | Wire Color | → ESP32 Pin |
|-----------|------------|--------------|
| GND       | Black    | VIN/VCC      |
| D+        | Green       | GND          |
| D-        | Gray       | RXD          |
| VBUS      | Red        | TXD          |

### 🔍 Example Images
(Note: I didn’t follow wire colors in the photos. The colors in the table typically match common USB-A cables you can cut open.)

<img src="https://github.com/user-attachments/assets/9b674e06-41ca-4bcf-b09b-691a5fbd8545" width="400"/>
<br/>

![Wiring Example 2](https://github.com/user-attachments/assets/e30fadd9-19cd-47ec-baab-86f8a80410f6)

![7480a856c7839044d7a04292d352b709a2155c07_2_296x500](https://github.com/user-attachments/assets/5b3ccbb8-eb62-4743-8d05-f88a9b986743)

---

This solution is based on ESPHome and works only with Home Assistant.

1. Install ESPHome
	•	In Home Assistant go to Settings → Add-ons → ESPHome and install

2. Create a New Device
	•	In the ESPHome Dashboard → “New Device”
	•	Choose your ESP32 type, e.g. esp32-c3-devkitm-1 or nodemcu-32s

3. Add Configuration

Option A: Simple Configuration

📄 Sample_conf.yaml

Option B: Advanced Configuration

📄 TCL-Conditioner.yaml

📝 Important:
	•	Customize Wi-Fi credentials, device name, etc.
	•	Comments in the YAML file help guide you through setup

4. Flash to ESP32
	•	Connect via USB cable or use OTA (Over-the-Air)

⸻

✅ Compatible Air Conditioners

These models have been successfully tested:
	•	TCL: TAC-07CHSA / TAC-09CHSA / TAC-12CHSA / TAC-12CHDA
	•	Daichi: AIR20AVQ1, AIR25AVQS1R-1, DA35EVQ1-1
	•	Axioma: ASX09H1 / ASB09H1
	•	Dantex: RK-12SATI / RK-12SATIE
	•	…and similar models

⚠️ Note:
Even if the model number matches, differences may exist (e.g., no USB port, no UART on the circuit board, etc.).


---
