# LEVEL 5 — INNOVATOR 🌐
## Standards 8th–9th | Theme: "IoT + AI — Build the Future"
### 36 Sessions × 1 hr | 9 Months

---

## Overview
This is the summit. Students connect hardware to the internet, train real AI models, and build systems that solve genuine real-world problems. Projects at this level are indistinguishable from professional prototypes. Every session delivers something students can show their family and say: "I built this, and it works from anywhere in the world."

---

## Component Inventory

| Category | Components |
|----------|-----------|
| Microcontrollers | NodeMCU ESP8266 or ESP32 (WiFi + BT), Arduino Nano (for serial bridge) |
| Sensors | DHT22 (temp + humidity), HC-SR04 ultrasonic, PIR motion sensor, Soil moisture sensor |
| Air Quality | MQ-2 gas/smoke sensor, MQ-135 air quality sensor |
| Touch + RFID | TTP223 capacitive touch sensor module, RC522 RFID module + RFID cards/tags |
| Display | OLED 0.96" I2C, 16×2 LCD I2C |
| Control | IR receiver TSOP1738, 5V relay module, servo SG90 |
| Communication | HC-05 Bluetooth module |
| Optional | SIM800L GSM module (SMS alerts), LoRa SX1278 (long-range IoT) |
| AI | Webcam or phone camera (for Google Teachable Machine) |
| Platform | Laptop with Arduino IDE, Chrome browser, Blynk app, ThingSpeak account |

---

## UNIT 1 — ESP8266/ESP32 Introduction (Sessions 1–3)
*"Your sensor just got a WiFi card"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 1 | ESP8266 vs ESP32 — what's different? NodeMCU board layout | Install ESP8266 board package in Arduino IDE. Blink the LED over USB first |
| 2 | Connect to WiFi — `WiFi.begin()` + `WiFi.status()` | Connect to school/hotspot WiFi. Print IP address to Serial Monitor. Celebrate! |
| 3 | HTTP basics — GET request | ESP8266 fetches data from a URL (`http://worldtimeapi.org/api/ip`). Print timestamp to Serial Monitor |

---

## UNIT 2 — Blynk / ThingSpeak Cloud Dashboard (Sessions 4–6)
*"Sensor data on your phone, anywhere on Earth"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 4 | ThingSpeak setup — create account, channel, API key | Send a number (e.g., `42`) to ThingSpeak from ESP8266. See it appear on the web chart |
| 5 | DHT22 → ESP8266 → ThingSpeak live chart | Real temperature + humidity data streams to cloud. Open phone → see live graph |
| 6 | Blynk setup — virtual pins, dashboard widgets | Create a Blynk dashboard with gauge (temperature) + label (humidity). Data updates every 5 seconds |

> **WOW factor:** Student holds up phone showing live temperature graph. Teacher is 50 meters away — data still updates. "It's on the internet!"

---

## UNIT 3 — Relay + IoT Home Automation (Sessions 7–9)
*"Control real appliances from your phone"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 7 | Relay module — safe switching, flyback diode, NO vs NC terminals | Demo: relay clicks when 5V signal applied. Connect LED bulb (12V safe demo) to relay output |
| 8 | Blynk button widget → ESP8266 → relay toggle | Create a "Smart Switch" in Blynk. Toggle button → relay clicks → lamp turns on/off from phone |
| 9 | **Build: Smart Home Switch** | DHT22 + relay + OLED. OLED shows local temp. Blynk shows remote temp + manual relay toggle. One device, two interfaces! |

---

## UNIT 4 — IR Remote + Relay (Sessions 10–12)
*"TV remote controls your room lights"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 10 | TSOP1738 + `IRremote.h` — decode remote buttons | Print hex codes for 10 buttons from a TV remote to Serial Monitor |
| 11 | Map IR codes to relay actions | Button "1" → Relay 1 ON. Button "2" → Relay 1 OFF. Button "3" → Relay 2 ON. Etc. |
| 12 | **Build: IR Remote-Controlled Room Lights** | 2 relays + 2 LED lamps + TSOP1738 + Nano. TV remote controls Room A and Room B lights independently. Add LCD: shows which room is on/off |

---

## UNIT 5 — RFID Access Control (Sessions 13–15)
*"Your card is your key"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 13 | RC522 RFID module — SPI wiring, MFRC522 library | Scan any RFID card → Serial Monitor prints UID |
| 14 | Authorized UID list — compare scanned vs stored | Store 2 authorized UIDs in code. Scan authorized card → Serial prints "ACCESS GRANTED". Scan unknown → "ACCESS DENIED" |
| 15 | **Build: Smart Access Control System** | RC522 + relay + servo + LCD. Authorized card → relay clicks (electric lock simulation) + servo opens gate + LCD: "ACCESS GRANTED – Welcome!" Wrong card → buzzer + LCD: "ACCESS DENIED" |

> **WOW factor:** Students build a card-based door entry system. Looks like the reader at a real office building!

---

## UNIT 6 — Google Teachable Machine — AI Training (Sessions 16–18)
*"You are now an AI engineer"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 16 | What is machine learning? Training vs inference | Sort physical objects by color → YOU are the classifier. How did you learn? You looked at examples! Teachable Machine does the same |
| 17 | Train an image classification model | Open Teachable Machine. Create 3 classes: ✋ open palm / 👍 thumbs up / ✌️ peace. Record 50+ samples each. Train. Test accuracy |
| 18 | Export + deploy model in browser (P5.js or Teachable Machine preview) | Webcam → model classifies in real time. Accuracy test: does it still work in different lighting? |

---

## UNIT 7 — AI + Hardware Integration (Sessions 19–21)
*"AI tells hardware what to do"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 19 | Python → Arduino Serial bridge | Python script runs Teachable Machine inference. When gesture detected → `serial.write('F')` → Arduino receives → LED changes color |
| 20 | Gesture-controlled LED panel | Open palm → all LEDs on. Thumbs up → green only. Peace → blue only. Fist → all off |
| 21 | **Build: Voice-Controlled Device (Sound Model)** | Train Teachable Machine audio model: "ON" / "OFF" / background. Chrome app listens → sends serial command → relay toggles |

---

## UNIT 8 — ESP32 BT + WiFi Simultaneously (Sessions 22–23)
*"Two radios, one chip"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 22 | ESP32 Bluetooth serial — `BluetoothSerial.h` | Connect phone via BT to ESP32. Send commands from phone → Serial Monitor prints them |
| 23 | Run BT + WiFi simultaneously | ESP32 uploads DHT22 data to ThingSpeak via WiFi WHILE also receiving BT commands from phone. Two-channel control in one device |

---

## 🏆 MID-YEAR PROJECT (Sessions 24–25)
*Individual or pairs — build one complete IoT or AI system*

| Project | Tech | WOW Factor |
|---------|------|-----------|
| **Personal IoT Dashboard** | ESP8266 + 3 sensors + ThingSpeak + OLED | Sensor data on phone dashboard + local OLED display. Dual display! |
| **AI Hand Sign Translator** | Teachable Machine + 5 gestures + LCD | Show gesture → LCD prints corresponding word |
| **Smart Home Prototype** | ESP8266 + relay + DHT22 + PIR + Blynk | Motion + temp + manual relay toggle all on one Blynk dashboard |
| **Voice Command Relay** | Teachable Machine audio + ESP32 + relay | Speak "ON"/"OFF" → relay toggles. No button needed! |
| **RFID Smart Safe** | RC522 + servo + LCD | Swipe authorized card → servo opens. Wrong card → locked |

**Deliverable:** Live working demo + 1-page technical report describing the problem solved

---

## UNIT 9 — Year-End Capstone Projects (Sessions 26–36)
*Teams of 2–3. These projects must genuinely solve a real-world problem.*

### Year-End Project Options:

| # | Project | Components | WOW Factor |
|---|---------|-----------|-----------|
| 1 | **Smart Parking Management System** | 3× HC-SR04 + ESP8266 + LED indicators | Ultrasonic detects parked cars. ESP8266 serves a live webpage showing available slots. Visitors open the URL → see real-time slot map! |
| 2 | **AI-Powered Waste Segregator** | Webcam + Teachable Machine + 3× servo + ESP32 | Camera classifies waste (plastic / paper / metal). Each class triggers a different servo gate → physical sorting into separate bins. No human sorting! |
| 3 | **Smart Agriculture Dashboard** | Soil moisture + DHT22 + MQ-135 + ESP32 + relay | Dry soil → auto-pump triggers via relay. All data → Blynk dashboard. Alerts when temp or air quality is bad. Full farm-in-a-box! |
| 4 | **Anti-Theft Smart Home** | PIR + RC522 RFID + relay + ESP8266 + optional SIM800L | PIR detects intruder. If no RFID authorization in 10 seconds → relay triggers alarm + ESP8266 sends IFTTT webhook → phone notification. Or SMS via SIM800L |
| 5 | **Emergency Health Monitor** | Pulse sensor + DHT22 + MQ-135 + ESP8266 | Reads BPM, temp, air quality. If any value critical → IFTTT sends WhatsApp/email alert to family. LCD shows live data locally |
| 6 | **Smart Energy Meter** | Current sensor (ACS712) + relay + ESP8266 | Measures current draw. Calculates power (W) and cost (₹/day). Displays on OLED + streams to ThingSpeak web chart. Relay cuts power on overload |
| 7 | **Voice-Controlled Home Automation** | Teachable Machine audio + ESP32 + 2× relay | Trained on "Light ON" / "Light OFF" / "Fan ON" / "Fan OFF". ESP32 runs inference OR Python bridge → relays control light and fan |
| 8 | **AI Traffic Management System** | Webcam + Teachable Machine + ESP8266 + LEDs | Camera counts vehicle density (few/many). Heavy side gets longer green. Light side gets shorter. Simulated with LED signal array. Real adaptive traffic logic! |

| Session | Activity |
|---------|----------|
| 26 | Problem research + solution proposal |
| 27 | Block diagram + tech stack decision |
| 28 | Component list + circuit schematic |
| 29 | Hardware prototype — breadboard |
| 30 | Code phase 1 — sensors + basic outputs |
| 31 | Code phase 2 — IoT / AI integration |
| 32 | Full hardware + code integration |
| 33 | AI model training / cloud pipeline setup |
| 34 | Testing + reliability (3-cycle pass/fail) |
| 35 | Documentation + presentation slides |
| 36 | **YEAR-END EXHIBITION 🎉** |

---

## Assessment Framework

| Component | Weight |
|-----------|--------|
| Unit challenges | 15% |
| Mid-year prototype + technical report | 30% |
| Year-end capstone exhibition | 55% |

---

## What a Level 5 Graduate Can Do
- Connect any sensor to the internet and view data from anywhere
- Train a machine learning model and connect it to physical hardware
- Build multi-sensor systems that respond autonomously to real-world conditions
- Present a complete engineering solution: problem → design → build → test → demo
- Write Arduino + ESP32 code confidently from scratch
