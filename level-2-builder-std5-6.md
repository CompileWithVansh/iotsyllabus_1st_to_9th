# LEVEL 2 — BUILDER 🔧
## Standards 5th–6th | Theme: "Arduino + Every Sensor You Can Find"
### 36 Sessions × 1 hr | 9 Months

---

## Overview
Arduino Uno enters the picture. Students go from zero coding knowledge to building a health monitor, gas leak detector, earthquake simulator, and more — using nearly every major sensor in the Arduino ecosystem. Real-world, impressive, and genuinely functional.

---

## Component Inventory

| Category | Components |
|----------|-----------|
| Microcontroller | Arduino Uno, USB A-B cable, 9V battery + clip |
| Input — Light/Motion | LDR (light dependent resistor), IR sensor module, PIR motion sensor |
| Input — Environment | DHT22 (temperature + humidity), Soil moisture sensor, MQ-2 gas/smoke sensor, MQ-135 air quality sensor |
| Input — Motion/Tilt | MPU-6050 gyroscope + accelerometer module |
| Input — Distance | HC-SR04 ultrasonic sensor |
| Input — Health | Pulse sensor (heart rate) |
| Input — User | Push buttons, potentiometer (10kΩ) |
| Output — Display | OLED 0.96" I2C display, 16×2 LCD with I2C module, 7-segment display (single digit), 8-LED bar graph module |
| Output — Sound/Light | Active buzzer, LEDs (multi-color), 220Ω resistors |
| Output — Actuators | Servo motor SG90, DC motor with L298N motor driver |
| Wiring | Breadboard, jumper wires |
| Platform | Laptop with Arduino IDE installed |

---

## UNIT 1 — Arduino Uno Introduction (Sessions 1–3)
*"Hello, Arduino — my new best tool"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 1 | What is Arduino? Microcontroller vs computer | Label every part: pins, USB, power, reset. Compare to the circuits from Level 1 |
| 2 | Arduino IDE — install, boards, ports, upload | First program: Blink the onboard LED. Change delay. See the difference |
| 3 | Serial Monitor — Arduino talks to the laptop | Print "Hello World!", print numbers, print sensor placeholder values |

---

## UNIT 2 — Digital I/O (Sessions 4–8)
*"Control things. Read things."*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 4 | `digitalWrite()` — multiple LEDs | Traffic light sequence: Red → Yellow → Green with delays |
| 5 | `digitalRead()` — push button input | Button press → LED on. Release → LED off. |
| 6 | `if/else` in code | Press → Green LED. No press → Red LED. |
| 7 | Buzzer with `tone()` — playing notes | Play a 4-note melody. Police siren pattern |
| 8 | **Challenge: Intruder Alarm Panel** | 3 buttons trigger different buzzer tones + LED colors. "Zone 1 / Zone 2 / Zone 3 breached!" |

---

## UNIT 3 — Analog Sensors (Sessions 9–13)
*"The world isn't just ON/OFF"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 9 | `analogRead()` — 0 to 1023 explained | Potentiometer → Serial Monitor: watch values change as you turn the knob |
| 10 | LDR — light detection | Serial Monitor: cover LDR, watch values drop. Print BRIGHT / DARK |
| 11 | `map()` function — scaling values | LDR value → `map()` to 0–255 → `analogWrite()` LED brightness (auto-dimming lamp) |
| 12 | Potentiometer as volume/speed control | Pot controls LED brightness. Pot controls servo angle |
| 13 | **Challenge: Smart Night Lamp** | LDR detects darkness → LED brightens automatically using `map()` + PWM |

---

## UNIT 4 — Environmental Sensors (Sessions 14–17)
*"Read the room — literally"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 14 | DHT22 — temperature + humidity | Serial Monitor displays: Temp: 28°C, Humidity: 65%. Add DHT.h library |
| 15 | DHT22 + threshold logic | LED turns red if temp > 35°C (fever alert). Green if normal |
| 16 | Soil moisture sensor — analog read | Monitor: values change when soil is wet vs dry. Map to percentage |
| 17 | MQ-2 gas/smoke sensor + MQ-135 air quality | Serial Monitor: watch values spike when you wave smoke near it. Set threshold → buzzer alert |

---

## UNIT 5 — Motion Detection (Sessions 18–20)
*"Something moved!"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 18 | PIR motion sensor — how passive infrared works | Walk past sensor → LED triggers. Stand still → LED off |
| 19 | MPU-6050 — gyroscope + accelerometer module | I2C library setup. Serial Monitor: print X, Y, Z acceleration values. Tilt the module → values change |
| 20 | **Challenge: Earthquake Simulator** | MPU-6050 reads vibration. Shake the table → if acceleration exceeds threshold → buzzer + LED alert. Print "EARTHQUAKE DETECTED!" on Serial Monitor |

---

## UNIT 6 — Display Output (Sessions 21–23)
*"Show what you know"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 21 | OLED 0.96" display — I2C, library, draw text + shapes | Display your name + draw a smiley face. Show live temperature reading from DHT22 |
| 22 | 16×2 LCD with I2C — setup, scroll text | Display "SMART LAB" on LCD. Show distance value from ultrasonic in real-time |
| 23 | 7-segment display (single digit) + bar graph | Display countdown 9→0 on 7-segment. Bar graph fills as LDR reading increases |

---

## UNIT 7 — Pulse Sensor & Health Monitoring (Sessions 24–25)
*"Your heartbeat on a screen"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 24 | Pulse sensor — how it detects heartbeat (light reflection) | Place finger on sensor → Serial Monitor shows raw signal waveform. Add PulseSensor library |
| 25 | **Build: Smart Health Monitor** | Pulse sensor + DHT22 + OLED display. OLED shows: Heart Rate: 72 BPM / Temp: 37.2°C / Status: NORMAL. Exceeds threshold → buzzer + LED alert |

> **WOW factor:** Student puts finger on sensor, BPM appears on OLED in real time. Looks like a hospital monitor!

---

## UNIT 8 — Servo & Motor Control (Sessions 26–27)
*"Make things move with precision"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 26 | Servo SG90 — `Servo.h`, `write()`, sweep | Sweep 0°→180°→0°. Pot controls servo position in real-time |
| 27 | DC motor with L298N — forward/backward/speed | `analogWrite()` to ENA pin = variable speed. Button = direction toggle |

---

## 🏆 MID-YEAR PROJECT (Session 28)
*Individual or pairs — build one complete system*

| Project | Sensors Used | Output | WOW Factor |
|---------|-------------|--------|-----------|
| **Gas Leak Detector** | MQ-2 + buzzer + LEDs | LCD shows "DANGER!" | Red flashing LED + alarm when gas detected |
| **Smart Plant Monitor** | Soil moisture + DHT22 | LCD shows moisture % + temp | Alerts when plant needs water |
| **Motion Security System** | PIR + buzzer + LCD | "INTRUDER DETECTED!" on LCD | Alarm + LED when someone walks in |
| **Personal Health Check** | Pulse sensor + DHT22 + OLED | Live BPM + Temp on OLED | Looks like a wearable health gadget |

**Evaluation:** Live demo + explain every component's role + explain one key line of code

---

## UNIT 9 — Year-End Complex Project (Sessions 29–36)
*Teams of 2–3. Must be genuinely impressive.*

### Year-End Project Options:

| # | Project | Components | WOW Factor |
|---|---------|-----------|-----------|
| 1 | **Smart Health Station** | Pulse + DHT22 + MQ-135 + OLED | Press finger → OLED shows BPM, Temp, Air Quality all at once. Like a kiosk! |
| 2 | **Earthquake Early Warning System** | MPU-6050 + buzzer + LCD + LED | Shake table → LCD shows "EARTHQUAKE!" + buzzer alarm + LED flash. Fully autonomous |
| 3 | **Smart Classroom Monitor** | PIR + DHT22 + MQ-135 + LCD | Monitors occupancy, temperature, and air quality. LCD auto-updates. Perfect demo for school display |
| 4 | **Blind Person Navigation Aid** | HC-SR04 + buzzer | Beep frequency increases as obstacle gets closer. Mount on a stick model — beeps fast when near wall |
| 5 | **Fire & Gas Safety System** | MQ-2 + DHT22 + PIR + relay + buzzer | Detects gas/smoke AND motion AND high temp → triggers relay (simulates sprinkler). Full multi-sensor safety system |
| 6 | **Tilt-Controlled LED Game** | MPU-6050 + 8-LED bar graph | Tilt the board left/right → bar graph LEDs shift. Balance challenge: keep the center LED lit! |

| Session | Activity |
|---------|----------|
| 29 | Project selection, problem statement, component list |
| 30 | Circuit schematic drawn on paper |
| 31 | Hardware assembly — breadboard prototype |
| 32 | Code — basic sensor reading working |
| 33 | Code — full logic + outputs integrated |
| 34 | Integration testing + debugging |
| 35 | Model casing + presentation preparation |
| 36 | **YEAR-END EXHIBITION 🎉** |

---

## Assessment Framework

| Component | Weight |
|-----------|--------|
| Session challenges (weekly) | 20% |
| Mid-year project demo + explanation | 30% |
| Year-end exhibition | 50% |
