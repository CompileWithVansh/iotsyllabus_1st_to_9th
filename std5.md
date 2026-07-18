# 💻 Standard 5 — Code Begins
## Theme: "Arduino Enters the Lab"
### 36 Sessions × 1 hr | 9 Months

---

## What You'll Build This Year

- **🔗 Chain Project:** Take the 4th class RC Car chassis, remove old wiring, and install an Arduino Uno as the brain. Write code: IR sensor on front → if obstacle detected → motors stop. Headlights now controlled by Arduino + LDR sensor. The car THINKS — it stops itself before crashing!
- **🚀 Standalone Project:** Smart Health Monitor — Pulse sensor + DHT22 temperature sensor + OLED display → shows live BPM + Temperature + Status (Normal / High). Like a wearable medical device!

---

## Component Inventory

| Category | Components |
|----------|-----------|
| From Last Year | RC Car chassis (motors, wheels, L298N, caster) — old wiring removed |
| Microcontroller | Arduino Uno, USB A-B cable |
| Sensors — Car | IR sensor module (obstacle detection), LDR (auto-headlights) |
| Sensors — Health | DHT22 temperature + humidity sensor, pulse sensor module |
| Sensors — Bonus | PIR motion sensor, soil moisture sensor |
| Display | OLED 0.96" I2C display |
| Output | Active buzzer, white LEDs × 2, 220Ω resistors × 4 |
| Power | 9V battery + clip (for Arduino), 9V battery + clip (for L298N), USB cable for programming |
| Wiring | Breadboard, jumper wires |
| Platform | Laptop with Arduino IDE installed |

---

## Session Plan

| Session | Topic | Activity |
|---------|-------|----------|
| 1 | What is Arduino? Microcontroller vs old transistor circuits | Hold up the BC547 (from 4th class) vs the Arduino Uno. "This transistor does ONE thing. Arduino does THOUSANDS of things — and YOU tell it what." |
| 2 | Arduino IDE — install, configure, first upload | Install Arduino IDE. Select board: Uno. Select port. Upload the built-in Blink example. Onboard LED blinks. "You just gave instructions to a chip!" |
| 3 | Anatomy of a sketch — setup() and loop() | What runs once vs what runs forever? Change the blink delay. Upload again. Change 1000 → 100 → it blinks faster. You control time! |
| 4 | Serial Monitor — Arduino talks to your laptop | `Serial.begin(9600)` and `Serial.println("Hello!")`. Print your name. Print a counting loop. The chip is communicating! |
| 5 | `digitalWrite()` — control external LED | Wire LED + resistor to pin 13. Control it from code. Blink pattern: SOS (... --- ...). |
| 6 | `digitalRead()` — button input | Wire push button to pin 2 with pull-down resistor. Press button → Serial Monitor prints "PRESSED". Release → "RELEASED". |
| 7 | `if / else` — decision making in code | Button press → if (buttonState == HIGH) → LED on, buzz "alarm". Else → LED off. Your first code logic! |
| 8 | Buzzer with `tone()` | `tone(pin, frequency, duration)`. Play musical notes: 262Hz = C, 294Hz = D. Write a 4-note melody. |
| 9 | `analogRead()` — sensors that give more than ON/OFF | Potentiometer on A0 → `analogRead()` → Serial Monitor: watch values 0–1023 as you turn the knob. |
| 10 | LDR with `analogRead()` + `map()` | LDR on A1. Map raw value (0–1023) to brightness (0–255). Use `analogWrite()` to control LED brightness automatically. |
| 11 | PIR motion sensor — digital trigger | Wire PIR to pin 3. Walk past → `digitalRead()` = HIGH → buzzer alert. Stand still → LOW → silence. |
| 12 | DHT22 — temperature + humidity | Install DHT library. Wire DHT22 to pin 4. Print: "Temp: 28°C | Humidity: 65%". Add: if temp > 35 → print "FEVER ALERT!". |
| 13 | OLED display — I2C setup | Install SSD1306 + GFX library. Wire SDA→A4, SCL→A5. Display your name. Display temperature reading from DHT22. |
| 14 | OLED display — multiple values + shapes | Show temp AND humidity together. Draw a box around the values. Show a small icon (heart shape for health monitor preview). |
| 15 | IR obstacle sensor — how it works | Wire IR sensor to pin 5. Wave hand in front → Serial Monitor: "OBSTACLE!". No hand → "CLEAR". |
| 16 | L298N wiring with Arduino | Connect L298N: IN1→pin6, IN2→pin7, IN3→pin8, IN4→pin9, ENA→pin10(PWM), ENB→pin11(PWM). Write motor functions: `forward()`, `backward()`, `stopMotors()`. |
| 17 | Car drive code — functions | Write clean functions: `void forward(int speed)`, `void turnLeft()`, `void stopAll()`. Test each with Serial Monitor commands. |
| 18 | Auto-stop with IR sensor — the car thinks! | Combine: if (`irSensor == LOW`) → `forward()`. Else if (`irSensor == HIGH`) → `stopAll()`. Drive toward a wall → car stops by itself! |
| 19 | LDR auto-headlights in code | `int lightLevel = analogRead(A1)`. If lightLevel < 400 → `digitalWrite(headlightPin, HIGH)`. Else → LOW. Dim room → car lights up! |
| 20 | **Chain Project Session 1** — Strip old car wiring | Remove all 4th-class components (BC547, 555, manual switches). Keep: chassis, motors, L298N, wheels. Plan new Arduino wiring. |
| 21 | **Chain Project Session 2** — Arduino Uno mounting + wiring | Mount Arduino on chassis. Wire: Uno → L298N (motor control). Wire: Uno → IR sensor (front obstacle). Wire: Uno → LDR (headlight). |
| 22 | **Chain Project Session 3** — Upload obstacle-stop code | Upload complete code: IR detects obstacle → stop motors. LDR dark → headlights on. Test on the floor — does it stop before hitting the wall? |
| 23 | **Chain Project Session 4** — Calibration + tuning | Adjust IR sensitivity knob. Test at different speeds. Does it stop in time at max speed? Add `delay()` for brake smoothness. |
| 24 | **Chain Project Session 5** — Final car tests + documentation | Run 5 test drives — must auto-stop every time. Document: upload code to GitHub or print it. Write a comment on every line of the code. |
| 25 | **Chain Project Complete** — 5-year upgrade card | Create the upgrade card: "1st: Motor bug. 2nd: RC car. 3rd: Lights + horn. 4th: Auto-headlights (transistors). 5th: Arduino — sensor-controlled car!" |
| 26 | Soil moisture sensor — analog reading | Wire soil sensor to A2. Print moisture %. Stick in dry soil → value. Wet soil → value changes. Add: if moisture < 30% → LED warns "WATER PLANT!" |
| 27 | Pulse sensor — detecting heartbeat | Install PulseSensor library. Place finger on sensor → Serial Monitor shows raw waveform. Observe peaks (each peak = one heartbeat). |
| 28 | Pulse sensor — calculate BPM | Library gives `getBPM()` value. Print: "Heart Rate: 72 BPM". If BPM > 100 → print "HIGH — REST NOW". |
| 29 | **Standalone Project** — Smart Health Monitor assembly | Combine: pulse sensor (A0) + DHT22 (pin4) + OLED. Display screen shows BPM, Temp, Status. One device, three readings! |
| 30 | Standalone — Threshold logic + alerts | Add buzzer alert: if BPM > 100 OR temp > 38 → buzzer beeps + OLED shows "ALERT!". Like a real medical monitor. |
| 31 | Standalone — Housing design | Mount all components on a flat cardboard panel. Finger rests on pulse sensor. OLED faces user. Buzzer on the side. Label it "HEALTH STATION". |
| 32 | Standalone — Full test and refinement | Test with 5 different students. Does it read everyone? Adjust sensitivity. Make sure all values display correctly. |
| 33 | Mock Exhibition prep — Chain Project | Practice 2-minute explanation: show the car driving, show it stopping automatically, explain the code logic in plain words. |
| 34 | Mock Exhibition prep — Standalone | Practice health monitor demo: place finger, watch BPM update, point to temp, explain what Normal vs High means. |
| 35 | Exhibition boards + code printout | Print the code for both projects. Highlight key lines. Prepare title cards with problem statement + solution. |
| 36 | 🎉 Year-End Exhibition | Demo Sensor-Controlled RC Car (drives + auto-stops!) + Smart Health Monitor (live BPM on screen!). Visitors test the monitor by placing their finger on the sensor. |

---

## 🔗 Chain Project Deep-Dive: Sensor-Controlled RC Car (Arduino Uno)

**What You Bring from 4th Class:** The RC Car chassis with motors, wheels, L298N driver, and caster — but the old transistor/IC wiring is REMOVED. The chassis is the foundation.

**What You Add This Year:**
- Arduino Uno as the central brain
- IR obstacle sensor on the front bumper
- LDR for auto-headlights (now controlled by code, not transistors)
- Full Arduino code for motor control + sensor responses

**The Upgrade Story:** In 4th class, you used a transistor to make lights automatic. Now Arduino does that AND obstacle detection AND speed control AND can do a hundred more things — in code. The jump from hardware-only to programmed intelligence is the biggest leap of the whole 9-year journey!

**Key Code Concepts Used:**
```cpp
// Auto-stop with IR sensor
void loop() {
  int obstacle = digitalRead(IR_PIN);    // Read IR sensor
  int light = analogRead(LDR_PIN);       // Read LDR
  
  if (obstacle == LOW) {                 // No obstacle
    forward(150);                         // Drive at medium speed
  } else {
    stopMotors();                         // STOP! Obstacle detected
  }
  
  if (light < 400) {                     // Dark enough
    digitalWrite(HEADLIGHT_PIN, HIGH);   // Headlights ON
  } else {
    digitalWrite(HEADLIGHT_PIN, LOW);    // Headlights OFF
  }
}
```

**Keep It:** The car is now an Arduino-powered robot. In 6th class, an ultrasonic sensor goes on the front (longer range), and an LCD displays real-time distance readings. The robot gets eyes!

---

## 🚀 Standalone Problem-Solving Project: Smart Health Monitor

**The Real-World Problem:** Hospitals use multi-parameter monitors costing thousands of dollars. But people at home — especially elderly people — have no easy way to check their vitals. A simple, affordable monitor could save lives.

**Your Solution:** A portable health station that reads heart rate (BPM) and body temperature simultaneously, displays them on an OLED screen, and alerts with a buzzer if values are dangerous.

**How It Works:**
1. Place finger on pulse sensor → BPM is calculated and displayed
2. DHT22 reads room/body temperature → displayed alongside BPM
3. OLED shows: "BPM: 72 | Temp: 36.8°C | Status: NORMAL"
4. If BPM > 100 or Temp > 38°C → buzzer beeps + screen shows "ALERT!"

**Components Needed:**

| Component | Role |
|-----------|------|
| Arduino Uno | Brain — reads sensors, calculates, displays |
| Pulse sensor module | Detects heartbeat via light reflection on fingertip |
| DHT22 | Temperature + humidity sensor |
| OLED 0.96" I2C | Display screen (128×64 pixels) |
| Active buzzer | Alert sound |
| 9V battery + clip | Power source |
| Cardboard panel | Mounting |

**WOW Factor:** When a student puts their finger on the sensor and their actual BPM appears on the OLED screen — the room goes quiet. It looks and acts like hospital equipment. This is the moment students realize: "I can build anything."

---

## Year-End Exhibition

Students demonstrate TWO projects:

1. **Sensor-Controlled RC Car** — drive it toward a wall and watch it stop by itself! Dim the lights → headlights come on. Explain the Arduino code in plain language.
2. **Smart Health Monitor** — visitors place their finger on the sensor and see their own BPM. Compare to jumping jacks → BPM rises. Point out the temperature reading. Explain: what makes the buzzer sound?

**Connection:** The car now has an Arduino brain. In 6th class, the sensors get more capable — ultrasonic distance sensing, gas detection, and a real LCD dashboard. The robot is getting smarter year by year!

---

## Assessment

| Component | Weight | What's Evaluated |
|-----------|--------|-----------------|
| Session participation & challenges | 20% | Code uploads successful, debugging attempts, engagement |
| Code comments printout (Session 35) | 10% | Every line commented — student understands what code does |
| Chain Project — Sensor RC Car | 35% | Auto-stop works (5/5 tests)? LDR headlights work? Code structure clean? 5-year journey explained? |
| Standalone Project — Health Monitor | 35% | BPM displays live? Temperature correct? Alert logic triggers? Real-world problem articulated? |
