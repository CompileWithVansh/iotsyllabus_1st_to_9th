# 📡 Standard 8 — Connect
## Theme: "Everything Goes Wireless"
### 36 Sessions × 1 hr | 9 Months

---

## What You'll Build This Year

- **🔗 Chain Project:** Upgrade the 7th class autonomous robot with Bluetooth control. The robot now has TWO modes: AUTO (autonomous obstacle avoidance from 7th class) and MANUAL (phone controls it via Bluetooth). Press a button on the phone to toggle modes. PLUS: connect via ESP8266 to a Blynk dashboard that shows robot status live (distance reading, current mode, speed).
- **🚀 Standalone Project:** Smart Home Control Panel — ESP8266 NodeMCU + 2× relay + DHT22 temperature sensor + PIR motion sensor + Blynk app. Phone controls two "lights/fans" remotely, gets auto-alerts if temperature is too high or motion is detected at home.

---

## Component Inventory

| Category | Components |
|----------|-----------|
| From Last Year | Autonomous Robot (Nano + servo-scanner + HC-SR04 + L298N + OLED + chassis) |
| Bluetooth | HC-05 Bluetooth module |
| WiFi/IoT | NodeMCU ESP8266 |
| Access Control | RC522 RFID module + RFID cards × 2 |
| IR Control | TSOP1738 IR receiver module |
| Relay | 5V relay module × 2 |
| Sensors | DHT22, PIR motion sensor |
| Display | OLED 0.96" I2C, 16×2 LCD I2C |
| Output | Active buzzer, LEDs (multi-color), 220Ω resistors |
| Power | 9V batteries × 2, USB cables × 2, NodeMCU USB (micro-B) |
| Platform | Laptop with Arduino IDE, Blynk app on phone, school WiFi or mobile hotspot |
| Wiring | Breadboard, jumper wires |

---

## Session Plan

| Session | Topic | Activity |
|---------|-------|----------|
| 1 | HC-05 Bluetooth module — what it does | HC-05 creates a virtual serial port over Bluetooth. Pair with phone using "Serial Bluetooth Terminal" app. Type "hello" on phone → Serial Monitor on laptop shows it! |
| 2 | HC-05 AT mode — configure name + baud | Hold EN pin HIGH at power-on → AT mode. Send: `AT+NAME=ROBOT8`. `AT+BAUD4` (9600 baud). Now phone sees "ROBOT8" when scanning Bluetooth. |
| 3 | Bluetooth command parsing | Robot receives 'F' → forward. 'B' → backward. 'L' → left. 'R' → right. 'S' → stop. Use `Serial.read()` and `switch/case`. |
| 4 | Bluetooth RC car (standalone test) | Wire HC-05 to a test Nano + L298N. Control 2 motors from phone. This becomes the phone-control layer for the chain project. |
| 5 | MODE system — AUTO vs MANUAL | Wire a button. Press → toggle `mode` variable between AUTO and MANUAL. In AUTO: run obstacle avoidance. In MANUAL: run BT control. One button, two personalities! |
| 6 | **Chain Project Session 1** — Add HC-05 to robot | Wire HC-05 to Nano (TX→RX, RX→TX via voltage divider). Upload updated code with dual-mode logic. Test: 'A' command from phone → switches to AUTO mode. 'M' → MANUAL. |
| 7 | **Chain Project Session 2** — MANUAL mode test | Drive robot manually from phone. All 4 directions work. Then send 'A' → robot goes autonomous. Send 'M' → manual again. Seamless mode switching! |
| 8 | TSOP1738 IR receiver — remote control | Install IRremote.h. Point any TV remote at TSOP1738 → Serial Monitor prints hex code per button. Map codes to actions. |
| 9 | IR remote robot control (bonus) | Optional: Add IR control as a third mode. Now robot can be controlled by TV remote, phone BT, OR autonomous. Three control channels! |
| 10 | ESP8266 NodeMCU — WiFi module intro | Install ESP8266 board in Arduino IDE. Blink the built-in LED. Connect to WiFi: `WiFi.begin(ssid, password)`. Print IP address. It's online! |
| 11 | ESP8266 → Blynk cloud | Install Blynk library. Create Blynk project. Add a gauge widget (Virtual Pin V0). Upload code: send DHT22 temperature to V0. Phone shows live temperature! |
| 12 | Blynk button widget → relay control | Add Button widget on V1. Button press → ESP8266 → relay pin HIGH → relay clicks. You just turned a lamp on from your phone! |
| 13 | **Chain Project Session 3** — ESP8266 robot status reporter | Add ESP8266 alongside Nano on robot. Nano → sends distance + mode to Serial. ESP8266 reads Serial → sends to Blynk. Phone dashboard shows: Distance, Mode (AUTO/MANUAL). |
| 14 | **Chain Project Session 4** — Blynk dashboard for robot | On Blynk: add Gauge (distance), Label (mode: AUTO/MANUAL), Chart (distance over time). Now you can watch the robot "live" on your phone from across the room! |
| 15 | **Chain Project Session 5** — Full integration test | All three layers working: Bluetooth manual control from phone + autonomous mode + Blynk dashboard reporting status. The ultimate robot! |
| 16 | **Chain Project Complete** — 8-year upgrade card | Update the upgrade poster. Add: "8th: Bluetooth phone control + Blynk IoT dashboard." Document all connections in a wiring table. |
| 17 | Relay module — understanding the contacts | NO (Normally Open) vs NC (Normally Closed). Inductive kickback — why you need a flyback diode. Never connect 230V — only safe low-voltage demo. |
| 18 | Relay with two channels | Independent control of Relay 1 and Relay 2 from two different Blynk button widgets. Toggle each independently. |
| 19 | DHT22 + threshold alert on Blynk | If temperature > 35°C → Blynk sends a push notification to phone: "⚠️ Temperature too high!" No polling needed — Blynk's event system handles it. |
| 20 | PIR + Blynk motion alert | PIR detects motion → NodeMCU → Blynk event notification: "🚨 Motion detected at home!" This is a real intruder alert system! |
| 21 | **Standalone Project** — Smart Home concept | Real problem: you're not home. Is it too hot? Did someone break in? Can you control your lights remotely? Smart home systems answer all three. Plan the panel. |
| 22 | Standalone — Wire relays + DHT22 + PIR | Connect both relays to NodeMCU. Wire DHT22 on D2. PIR on D5. Test each component individually first. |
| 23 | Standalone — Blynk dashboard design | Create: Button 1 (relay 1 = "living room light"), Button 2 (relay 2 = "fan"). Gauge for temperature. LED indicator for motion detection. |
| 24 | Standalone — Upload and test | Upload code. Open Blynk on phone. Toggle button 1 → relay 1 clicks. Toggle button 2 → relay 2 clicks. Watch temperature update. Wave hand at PIR → motion LED blinks on phone. |
| 25 | RFID RC522 — access control | Install MFRC522 library. Wire via SPI. Scan RFID card → Serial Monitor shows UID. Store one "authorized" UID. Scan authorized card → "WELCOME!". Other card → "DENIED!". |
| 26 | RFID + relay = smart door lock | Authorized RFID scan → relay activates (simulates electric lock) + LCD: "ACCESS GRANTED". Unauthorized → buzzer + LCD: "ACCESS DENIED". |
| 27 | RFID + Blynk log | Every RFID scan (authorized or not) logs to Blynk event stream with timestamp. Now you have an access log on your phone! |
| 28 | Standalone — Complete + refine | Add RFID as a physical unlock to the smart home panel (authorized RFID unlocks the panel itself). Full system: remote control + sensors + physical security. |
| 29 | HC-12 long-range radio (bonus) | HC-12 radio modules: 433MHz, up to 100m range. Wire TX/RX like serial. Send temperature from one Arduino to another across the building. Range test! |
| 30 | IoT mini-challenge | Team challenge: using only NodeMCU + 1 sensor + Blynk, build a useful IoT device in 45 minutes. Present to class: what does it do? What problem does it solve? |
| 31 | Mock Exhibition prep — Chain Project | Demo all three modes: AUTO driving → 'M' for manual → BT phone control → 'A' back to auto. Show Blynk dashboard updating in real time. List all 8 years of upgrades. |
| 32 | Mock Exhibition prep — Standalone | Demo Smart Home: toggle lights from phone, trigger temperature alert, wave at PIR. Explain Blynk architecture in plain language. |
| 33 | Peer review + stress test | Peers try to "break" each other's systems: What happens if WiFi goes down? What happens if Bluetooth disconnects? Test resilience. |
| 34 | Final code cleanup + architecture diagram | Draw a system architecture diagram: phone → Blynk server → ESP8266 → robot. Arrow for each data flow. Label protocols (HTTP, MQTT, Bluetooth, Serial). |
| 35 | Exhibition boards + tech story | Write a "tech stack" card: what hardware + what software + what communication protocols. This is how professional engineers document systems. |
| 36 | 🎉 Year-End Exhibition | Demo Dual-Mode Robot (Bluetooth + Autonomous + Blynk live) + Smart Home Panel (remote control + real-time alerts). Visitors control the robot from their own phones! |

---

## 🔗 Chain Project Deep-Dive: IoT Dual-Mode Robot

**What You Bring from 7th Class:** Fully autonomous robot with servo-scanner, HC-SR04, Arduino Nano, OLED display, L298N motor driver.

**What You Add This Year:**
1. **HC-05 Bluetooth module** — phone can send F/B/L/R/S commands and mode toggle commands
2. **Dual-mode logic** — 'A' = autonomous mode (obstacle avoidance from 7th class), 'M' = manual Bluetooth mode
3. **ESP8266 co-processor** — reads robot status from Nano via Serial, uploads to Blynk cloud
4. **Blynk dashboard** — phone shows: current distance, current mode, connection status

**The Upgrade Story:** The 7th class robot was fully autonomous. But sometimes you want to OVERRIDE automation — the same way modern cars have autopilot AND manual mode. The HC-05 adds the manual layer. The Blynk dashboard makes the robot visible from anywhere. You've built a remote-observable, dual-mode autonomous system!

**Communication Architecture:**
```
Phone → Bluetooth (HC-05) → Arduino Nano → Motor Driver → Wheels
         (MANUAL mode commands)

Phone → Blynk App → Blynk Cloud → ESP8266 → Serial → Nano
         (dashboard / status viewing)

Nano → Serial → ESP8266 → WiFi → Blynk Cloud → Phone
         (distance + mode reporting)
```

**Mode Toggle Code:**
```cpp
char btCmd = bluetooth.read();
if (btCmd == 'A') { mode = AUTO; oled.println("AUTO MODE"); }
if (btCmd == 'M') { mode = MANUAL; oled.println("MANUAL"); }

void loop() {
  if (mode == AUTO)   { autonomousAvoid(); }
  if (mode == MANUAL) { bluetoothControl(); }
  updateBlynkStatus();
}
```

**Keep It:** In 9th class, the Bluetooth is supplemented with a Teachable Machine AI model — hand gestures from a webcam replace button presses. The robot responds to ✋ STOP / 👆 FORWARD / 👈 LEFT / 👉 RIGHT / ✌️ TURBO. Same robot, from a bug in 1st class to an AI-gesture-controlled machine in 9th!

---

## 🚀 Standalone Problem-Solving Project: Smart Home Control Panel

**The Real-World Problem:** Modern homes need remote control + remote monitoring. You leave home and forget to turn off the fan. Your elderly parent's room gets too hot. Someone enters the house while you're away. All three problems need one solution: a connected home panel.

**Your Solution:** An ESP8266-based smart panel with:
- 2 relay-controlled outlets (lights, fan) — toggle from phone anywhere
- DHT22 temperature monitoring — auto-alert if above threshold
- PIR motion detection — auto-notification if motion detected
- RFID physical lock — only authorized card activates the panel locally

**Blynk Dashboard Design:**

| Widget | Type | Function |
|--------|------|----------|
| "Light" | Button | Controls Relay 1 — toggles living room light |
| "Fan" | Button | Controls Relay 2 — toggles fan |
| "Temperature" | Gauge | Shows live temperature reading |
| "Motion" | LED Indicator | Blinks when PIR detects movement |
| "Alerts" | Event Stream | Log of all alerts with timestamps |

**The Scale-Up Vision:** Add 6 more relays → control every room. Add cameras → video surveillance. Add energy metering → track electricity use. This is what every smart home company does — but your version costs under ₹500!

---

## Year-End Exhibition

Students demonstrate TWO projects:

1. **Dual-Mode Robot** — show AUTO mode (autonomous driving), then send 'M' on phone and take manual control. Visitors can control it from their own phone (after joining your Bluetooth). Show the Blynk dashboard live on a projected screen.
2. **Smart Home Panel** — visitors toggle lights/fan from the teacher's phone across the room. Trigger temperature alert. Wave at PIR — notification appears on phone instantly. Visitors are genuinely surprised: "You made this?!"

**Connection:** The robot now lives on two networks: Bluetooth (local) and internet (Blynk). In 9th class, the Bluetooth remote is replaced with something more futuristic: a computer vision AI model that reads your hand gestures and turns them into commands. Zero buttons needed.

---

## Assessment

| Component | Weight | What's Evaluated |
|-----------|--------|-----------------|
| Session challenges (BT, RFID, Blynk) | 20% | Successfully completing each wireless challenge |
| System architecture diagram (Session 34) | 10% | Correct data flow, protocols labeled, all nodes shown |
| Chain Project — Dual-Mode IoT Robot | 35% | Both modes work? Blynk dashboard updates live? Smooth mode switching? 8-year journey explained? |
| Standalone Project — Smart Home Panel | 35% | Remote relay control works? Alerts trigger correctly? RFID access works? Real-world use case explained convincingly? |
