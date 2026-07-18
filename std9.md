# 🧠 Standard 9 — Intelligence
## Theme: "A Robot's Mind — AI Meets Hardware"
### 36 Sessions × 1 hr | 9 Months

---

## What You'll Build This Year

- **🔗 Chain Project:** THE ULTIMATE UPGRADE. Train a Google Teachable Machine model to recognize 5 hand gestures: ✋ STOP / 👆 FORWARD / 👈 LEFT / 👉 RIGHT / ✌️ TURBO. Python detects the gesture via webcam → sends serial command to ESP32 → ESP32 controls the motor driver. The robot that started as a vibrating bug in 1st class now responds to human hand gestures. No buttons. No app. Pure AI.
- **🚀 Standalone Capstone Project:** Student chooses one real-world problem from 4 options (waste segregation, agriculture monitoring, traffic management, or energy monitoring) and builds a complete AI/IoT solution as their capstone project.

---

## Component Inventory

| Category | Components |
|----------|-----------|
| From Last Year | Robot chassis (motors, wheels, L298N motor driver, caster) |
| Microcontroller | ESP32 (replaces Nano — BT + WiFi simultaneously) |
| AI Platform | Webcam or phone camera, Chrome browser, Google Teachable Machine (free, browser-based) |
| Software | Python 3.x + pyserial + p5.js or TensorFlow.js |
| Actuators | Servo SG90 × 2 (for capstone options) |
| Relay | 5V relay module (for capstone options) |
| Sensors | DHT22, soil moisture sensor, ACS712 current sensor |
| Display | OLED 0.96" I2C |
| Power | 9V batteries × 2, USB-C cable for ESP32, laptop for Python |
| Capstone-specific | (See Capstone Project options below) |
| Wiring | Breadboard, jumper wires |

---

## Session Plan

| Session | Topic | Activity |
|---------|-------|----------|
| 1 | What is machine learning? | The sorting game: teacher holds up cards (animals / vehicles / food). Students sort them. How did you learn? You saw examples and found patterns. ML does the same thing! |
| 2 | Google Teachable Machine — first model | Open teachablemachine.withgoogle.com. Create 2 classes: "Open Hand" and "Fist". Record 30 samples each. Train. Test: does it recognize your hand? |
| 3 | Improving model accuracy | What affects accuracy? Lighting, background, angles. Record samples in multiple lighting conditions. Retrain. Compare accuracy. Understand: data quality = model quality. |
| 4 | 5-gesture model — train for robot control | Create 5 classes: ✋ STOP, 👆 FORWARD, 👈 LEFT, 👉 RIGHT, ✌️ TURBO. Record 60+ samples each (varied angles, lighting). Train. Accuracy test. |
| 5 | Export model + run in browser | Export Teachable Machine model (TensorFlow.js version). Load in a local HTML file. Real-time classification in browser. Check confidence percentages. |
| 6 | Python + pyserial — send to Arduino | Install Python + pyserial. Write Python script: if class == "FORWARD" → `serial.write(b'F')`. Connect Nano → test Python sends correct character. |
| 7 | P5.js bridge OR Python bridge | Two approaches: P5.js (browser → Arduino via p5.serialport) OR Python (uses TensorFlow directly). Choose the easier path for your setup. |
| 8 | Gesture → Python → Serial → LED panel | Complete pipeline test: show ✋ → Python detects → sends 'S' → Arduino turns on RED LED. Show 👆 → sends 'F' → GREEN LED. All 5 gestures mapped to 5 LEDs. |
| 9 | ESP32 introduction | ESP32 = ESP8266's bigger sibling. Has Bluetooth AND WiFi simultaneously. More GPIO pins. Better processor. Flash the Blink example. Explore pinout. |
| 10 | ESP32 Bluetooth serial | Install ESP32 board package. Use `BluetoothSerial.h`. Connect phone → send text → Serial Monitor shows it. Same interface as HC-05 but built-in. |
| 11 | ESP32 WiFi + Blynk | Connect ESP32 to Blynk. Simultaneously receive BT commands AND report to Blynk via WiFi. Two wireless protocols, one chip — the power of ESP32! |
| 12 | OTA updates — upload code without USB | Over-The-Air update: upload new code to ESP32 via WiFi. No USB cable needed. Professional engineers use this for deployed IoT devices. |
| 13 | IoT cloud pipelines — ThingSpeak | Create ThingSpeak account. Send sensor data. View charts. Set ThingSpeak alerts: if temperature > 40 → email alert. Free IoT analytics platform! |
| 14 | IFTTT webhooks — connect to anything | Create IFTTT account. ESP32 → triggers IFTTT webhook → sends WhatsApp message OR Gmail OR Google Sheets entry. Near-zero cost automation. |
| 15 | **Chain Project Session 1** — Swap Nano → ESP32 on robot | Remove Arduino Nano from robot. Mount ESP32. Rewire motor driver connections to equivalent ESP32 pins. Upload basic drive test. |
| 16 | **Chain Project Session 2** — Python gesture pipeline | Train final gesture model (60+ samples per class, good lighting). Write Python script: reads model output → sends serial command to ESP32. |
| 17 | **Chain Project Session 3** — Wire all 5 gestures | Map all 5 gestures to motor commands: STOP → `stopAll()`, FORWARD → `forward(180)`, LEFT → `turnLeft()`, RIGHT → `turnRight()`, TURBO → `forward(255)`. |
| 18 | **Chain Project Session 4** — Full pipeline test | Webcam → Python → Serial → ESP32 → motors. Show each gesture, verify robot responds. Measure latency (gesture to movement). |
| 19 | **Chain Project Session 5** — Reliability + range | Test at different distances from webcam (50cm, 1m, 2m). Does accuracy drop? Test in different lighting. Improve model if needed. |
| 20 | **Chain Project Session 6** — OLED status display | Add OLED to ESP32. Show: last detected gesture + confidence + motor action. Real-time AI feedback display! |
| 21 | **Chain Project Session 7** — Final demonstration prep | Rehearse the full 9-year story: Bug (1st) → AI Gesture Robot (9th). Run 10 consecutive gesture commands. Must work 9/10. |
| 22 | **Chain Project Complete** — 9-year upgrade poster | Create the definitive upgrade poster. All 9 years. All technologies. All components. Arrow from "vibrating motor" to "AI model". This is your story! |
| 23 | Capstone project — problem research | Research real-world versions of your chosen problem. How do companies solve it? What are limitations? What's YOUR innovation? Write a 1-page problem brief. |
| 24 | Capstone — solution design | Block diagram: inputs → processing → outputs. Components list. Cost estimate. Technical challenges anticipated. Get feedback from classmates. |
| 25 | Capstone — circuit schematic | Draw complete schematic. Identify all sensor pins, power requirements, communication protocols. Review with teacher before building. |
| 26 | Capstone — hardware build: phase 1 | Assemble physical hardware. Test each sensor/actuator individually. Don't connect everything at once — test incrementally. |
| 27 | Capstone — code: phase 1 (sensors) | Write sensor reading code. Print all values to Serial Monitor. Verify accuracy and reliability. Debug before adding more. |
| 28 | Capstone — code: phase 2 (AI or IoT integration) | Add the intelligence layer: train and integrate AI model (if AI project) OR connect cloud pipeline (if IoT project). |
| 29 | Capstone — full integration | Combine hardware + code + AI/IoT. First full end-to-end test. Identify and fix integration bugs. |
| 30 | Capstone — reliability testing | Run the system 10 times. How many failures? Fix failure modes. Real engineering requires ≥ 8/10 reliability. |
| 31 | Capstone — documentation | Write: problem statement, solution approach, component table, code explanation, test results (pass/fail table), future improvements. |
| 32 | Capstone — presentation design | Create a slide deck (5 slides max): Problem / Solution / Build / Demo / Impact. Practice 3-minute pitch. |
| 33 | Mock Exhibition — Chain Project + Capstone | Full dress rehearsal. Gesture robot demo. Capstone live demo. Time yourself. Adjust for 5 minutes total. |
| 34 | Peer review — technical challenge | Classmates ask hard questions: "What if the WiFi goes down?", "How accurate is the gesture detection?", "What would you improve?" Practice answering honestly. |
| 35 | Exhibition setup + video recording | Set up displays. Record a 1-minute demo video of each project (for portfolio / sharing). Check all power connections. |
| 36 | 🎉 Year-End Exhibition — THE FINALE | Present the 9-year story. Demo the AI Gesture Robot. Present capstone. Visitors try to control the robot with their own gestures. |

---

## 🔗 Chain Project Deep-Dive: AI Gesture-Controlled Robot

**What You Bring from 8th Class:** Robot with ESP8266/Nano, HC-05 Bluetooth, autonomous obstacle avoidance, Blynk dashboard.

**What You Replace This Year:**
- Nano/ESP8266 → **ESP32** (more powerful, BT + WiFi built in)
- Bluetooth phone app buttons → **Teachable Machine hand gestures via webcam**

**What You Add This Year:**
- Google Teachable Machine model (5 gestures)
- Python bridge (webcam → model inference → serial to ESP32)
- OLED shows last detected gesture + confidence

**The 9-Year Story:**

| Year | What Changed | Technology |
|------|-------------|------------|
| 1st | Vibrating bug crawls | DC motor + asymmetric weight |
| 2nd | RC car — 4 button control | L298N motor driver |
| 3rd | Headlights + horn | Parallel LEDs, buzzer circuits |
| 4th | Auto-headlights + timed horn | BC547 transistor, 555 timer |
| 5th | Arduino brain — obstacle stop | Arduino Uno, IR sensor |
| 6th | LCD dashboard — distance display | HC-SR04, 16×2 LCD |
| 7th | Autonomous scanning + decisions | Arduino Nano, servo scanner, OLED |
| 8th | Bluetooth + Blynk IoT | HC-05, ESP8266, Blynk |
| 9th | AI hand gesture control | ESP32, Teachable Machine, Python |

**The Gesture-to-Motor Pipeline:**
```
Webcam
  ↓
Chrome Browser (Teachable Machine model runs here)
  ↓
JavaScript/P5.js (reads class label + confidence)
  ↓
Web Serial API OR Python + pyserial
  ↓
ESP32 Serial (receives: 'F', 'B', 'L', 'R', 'S', 'T')
  ↓
L298N Motor Driver
  ↓
DC Motors → Robot moves!
```

**Sample Python Bridge:**
```python
import serial
import time
# Model inference result comes from browser via socket or is run directly in Python
# using TensorFlow Lite

ser = serial.Serial('COM3', 9600)

gesture_to_command = {
    'FORWARD':  b'F',
    'BACKWARD': b'B',
    'LEFT':     b'L',
    'RIGHT':    b'R',
    'STOP':     b'S',
    'TURBO':    b'T'
}

def send_gesture(gesture_label):
    cmd = gesture_to_command.get(gesture_label.upper(), b'S')
    ser.write(cmd)
    print(f"Sent: {cmd} for gesture: {gesture_label}")
```

**The WOW Moment:** Put the 1st-class vibrating bug on the left side of a table. Put the 9th-class gesture robot on the right. Show the progression. Then control the robot live with a hand gesture. "This started as a bug. Today it responds to your gestures. You did this in 9 years."

---

## 🚀 Standalone Capstone Project: Student Choice

Students choose ONE of the following real-world problems for their capstone:

---

### Option 1: AI Waste Segregator

**Problem:** Manual waste sorting is inefficient and exposes workers to health hazards. AI-powered sorting can classify waste in milliseconds.

**Solution:** Camera + Teachable Machine classifies waste (plastic / paper / metal / organic) → ESP32 receives classification → correct servo gate opens → waste falls into correct bin.

**Components:** ESP32, webcam, Python, servo × 4, bins/boxes (cardboard model)

**Build Plan:**
1. Train Teachable Machine: 4 classes (plastic bottle, newspaper, metal can, vegetable peel). 60+ samples each.
2. Python reads classification → sends class letter to ESP32
3. ESP32 activates corresponding servo gate
4. Waste drops into correct bin

---

### Option 2: Smart Agriculture Dashboard

**Problem:** Farmers often overwater or underwater crops. Real-time soil monitoring with automated irrigation can increase yield by 30–40%.

**Solution:** Soil moisture + DHT22 + MQ-135 air quality → ESP32 → Blynk dashboard. Dry soil → relay triggers irrigation pump (demo with small DC water pump). All data logged to ThingSpeak.

**Components:** ESP32, soil moisture sensor, DHT22, MQ-135, relay, small DC water pump, Blynk, ThingSpeak

**Build Plan:**
1. Wire all sensors to ESP32 analog/digital pins
2. Display readings on Blynk: moisture %, temp, humidity, air quality
3. Auto-relay: moisture < 30% → relay ON (pump starts) → moisture > 60% → relay OFF
4. ThingSpeak logs 24-hour data charts

---

### Option 3: AI Traffic Signal Controller

**Problem:** Fixed-timing traffic signals waste green light time when one side has no vehicles. Adaptive signals reduce wait times by up to 40%.

**Solution:** Camera at intersection → Teachable Machine classifies traffic density (EMPTY / LIGHT / HEAVY) → ESP32 adjusts LED signal timing accordingly.

**Components:** ESP32, webcam, Python, LED arrays (R/Y/G × 2 directions), Teachable Machine model

**Build Plan:**
1. Train model: 3 classes — "empty road", "1-2 cars", "3+ cars" (use printed car photos or toy cars)
2. Python reads class → sends density value to ESP32
3. ESP32 calculates: HEAVY side gets 30s green, LIGHT side gets 10s, EMPTY side gets 5s
4. Build cardboard intersection with LED signals at both ends

---

### Option 4: Smart Energy Monitor

**Problem:** Households have no real-time visibility into which appliances consume the most electricity. A live energy dashboard enables conscious consumption.

**Solution:** ACS712 current sensor measures current drawn by a device → ESP32 calculates power (W) and cost (₹/day) → OLED shows live reading + ESP32 serves a web dashboard accessible on any browser on the same WiFi.

**Components:** ESP32, ACS712 current sensor (30A module), OLED display, WiFi, HTML web server on ESP32

**Build Plan:**
1. Wire ACS712 in series with a small appliance (LED lamp, fan — safe demo voltage)
2. `analogRead()` → convert to current (A) → multiply by voltage (12V safe demo) → power in watts
3. OLED shows: Current: 0.8A | Power: 9.6W | Cost: ₹X/day
4. ESP32 web server: `server.on("/", handler)` → serves HTML page with live gauge chart

---

## Year-End Exhibition

**This is the finale of a 9-year journey. Make it count.**

Students present TWO items:

1. **AI Gesture Robot (Chain Project)** — set up the webcam. Show all 5 gestures. Robot responds to each. Visitors try controlling it with their own hand. Show the 9-year upgrade poster. End with the side-by-side: "1st class: this vibrating bug. 9th class: this AI-controlled machine."

2. **Capstone Project** — live demo. Real sensor data. Real AI classification or real IoT dashboard. Real problem addressed. 3-minute pitch: Problem → Solution → How It Works → Impact.

**The Closing Statement:** Every student in this room started with a battery and an LED. Today you've built something a professional engineer would recognize as a genuine prototype. The question isn't "Can you build technology?" — you've answered that. The question now is: "What problem will you solve next?"

---

## Assessment

| Component | Weight | What's Evaluated |
|-----------|--------|-----------------|
| Session challenges (Sessions 1–22) | 10% | AI model accuracy, Python bridge success, ESP32 configurations |
| Chain Project — AI Gesture Robot | 30% | Gesture detection accuracy (≥80%)? All 5 gestures work? Latency acceptable? 9-year story articulated beautifully? |
| Capstone — documentation (Session 31) | 15% | Problem brief, design decisions, test results, future improvements — all thoughtfully addressed |
| Capstone — Exhibition demo + pitch | 45% | Does it work reliably? Is the real-world problem clearly addressed? Is the solution genuinely useful? Can the student defend technical decisions? |
