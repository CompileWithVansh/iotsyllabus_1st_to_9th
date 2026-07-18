# 🌡️ Standard 6 — Sensors
## Theme: "A Robot's Senses — Every Sensor Has a Story"
### 36 Sessions × 1 hr | 9 Months

---

## What You'll Build This Year

- **🔗 Chain Project:** Upgrade the 5th class sensor car — Add HC-SR04 ultrasonic sensor (measures real distance), display status on a 16×2 LCD ("CLEAR" or "OBSTACLE at 23cm"), and upgrade headlights to auto-trigger via LDR + Arduino. The robot now announces how close obstacles are!
- **🚀 Standalone Project:** Gas Leak & Fire Detector — MQ-2 gas sensor + temperature threshold + buzzer + LEDs + LCD. When gas or dangerous heat is detected: "DANGER: GAS LEAK" or "HIGH TEMP!" appears on the LCD.

---

## Component Inventory

| Category | Components |
|----------|-----------|
| From Last Year | Arduino RC Car (Arduino Uno + chassis + motors + L298N + IR sensor + LDR) |
| Distance | HC-SR04 ultrasonic sensor |
| Gas/Air | MQ-2 gas and smoke sensor, MQ-135 air quality sensor |
| Motion/Tilt | MPU-6050 gyroscope + accelerometer module |
| Display | 16×2 LCD with I2C backpack module, OLED 0.96" I2C |
| Control | Relay module (5V), push buttons × 2 |
| Logic ICs | 7408 AND gate IC, 7432 OR gate IC (for integration demo) |
| Sensors | LDR (already on car), PIR motion sensor |
| Output | Active buzzer, LEDs (red × 2, green × 2, yellow × 1), 220Ω resistors |
| Power | 9V batteries × 2, Arduino Uno, USB cable |
| Wiring | Breadboard, jumper wires |

---

## Session Plan

| Session | Topic | Activity |
|---------|-------|----------|
| 1 | What makes a sensor useful? | The Story Approach: for each sensor today, answer first: "What problem does this sensor SOLVE in the real world?" Map sensor → problem → solution. |
| 2 | MQ-2 gas/smoke sensor — how it works | The sensor's resistance changes when gas particles hit it. Wire to A0 → Serial Monitor: wave lighter (unlit!) near it → value spikes. |
| 3 | MQ-2 threshold alert | Set threshold at 400. If `analogRead(MQ2_PIN) > 400` → buzzer + red LED. "Gas detected!" Display value on Serial Monitor. |
| 4 | MQ-135 air quality sensor | Similar to MQ-2 but for CO2, ammonia, benzene. Compare readings: fresh air vs near a candle. Print AQI-style category: GOOD / MODERATE / POOR. |
| 5 | MQ-2 + MQ-135 combined alert | If EITHER sensor exceeds threshold → full alert. Real air quality stations use multiple sensors for redundancy. |
| 6 | The blind spots problem — measuring distance | How does a robot know how far away a wall is? HC-SR04 ultrasonic sensor. Formula: distance = (duration × 0.034) / 2 cm. |
| 7 | Distance measurement in code | Wire Trigger to pin 9, Echo to pin 10. Print distance every 500ms. Wave hand — watch values change in real time! |
| 8 | Distance thresholds — zones | Print: if distance > 50cm → "FAR", if 20–50 → "NEAR", if < 20 → "VERY CLOSE — STOP!". |
| 9 | The Tilted Robot Problem | How does a robot know if it has fallen down or tipped over? Introduce MPU-6050 gyroscope/accelerometer. Print tilt values. |
| 10 | Fall detection trigger | If tilt value exceeds threshold → trigger alarm. "Robot has fallen down!". Make a tilt-activated LED game. |
| 11 | 16×2 LCD I2C — setup | Wire LCD: SDA→A4, SCL→A5. Install LiquidCrystal_I2C library. Display "SENSOR LAB" on line 1. Display today's date on line 2. |
| 12 | LCD + live sensor values | Display HC-SR04 distance on LCD: "DIST: 34cm". Update every 500ms. Watch LCD change as you move your hand. |
| 13 | LCD + OLED together | Show different data on each display: LCD = distance value. OLED = gas sensor status. Two displays, two information streams. |
| 14 | Relay module — safe switching | Relay closes when pin goes HIGH. Connect LED lamp to relay output contacts. Arduino → relay → lamp. One pin controls the lamp. |
| 15 | Relay with threshold logic | If MQ-2 > threshold → relay closes → "exhaust fan" (LED lamp) turns on. Auto-ventilation simulation. |
| 16 | Logic gate ICs with Arduino integration | Combine hardware AND gates with Arduino: 2 switch states → AND gate → Arduino reads gate output. "Hardware logic feeding software logic." |
| 17 | **Chain Project Session 1** — Upgrade plan | Study the 5th-class car. Identify where HC-SR04 mounts (front bumper, replaces/supplements IR sensor). Plan LCD mounting on car body. |
| 18 | **Chain Project Session 2** — Mount HC-SR04 | Replace IR sensor with HC-SR04 (or add alongside). Wire Trigger → pin 9, Echo → pin 10. Test distance reading on Serial Monitor. |
| 19 | **Chain Project Session 3** — LCD dashboard on car | Mount LCD on car body. Display: Line 1 = "DIST: XXcm", Line 2 = "STATUS: CLEAR" or "OBSTACLE!". Drive toward wall — watch the distance count down. |
| 20 | **Chain Project Session 4** — Distance-based auto-stop | Update code: if distance < 20cm → stop. If 20–40cm → slow down (lower PWM speed). If > 40cm → full speed. The car decelerates intelligently! |
| 21 | **Chain Project Session 5** — LDR headlights in code (refined) | Improve headlight code from 5th class: add hysteresis (lights come on at 400, turn off at 600) to prevent flickering in borderline light. |
| 22 | **Chain Project Complete** — Full system integration test | All features working simultaneously: drive, auto-stop, LCD distance display, auto-headlights. Run 5 test drives. Document all sensor pins in a table. |
| 23 | **Standalone Project** — Gas + fire detector concept | Real problem: kitchen gas leaks cause explosions. Electrical faults cause fires. A multi-sensor detector catches BOTH threats. Plan the circuit. |
| 24 | Standalone — MQ-2 gas detection circuit | Wire MQ-2 to A0. Set threshold. On trigger: red LED flashes + buzzer. Test with a puff of breath (CO2 spike). |
| 25 | Standalone — Temperature threshold | Wire DHT22. If temperature > 50°C (fire condition): yellow LED + different buzzer pattern. Two different alerts for two different threats. |
| 26 | Standalone — LCD alert messages | When gas detected: LCD shows "! GAS LEAK !" on line 1, "EVACUATE NOW" on line 2. When high temp: "HIGH TEMP!" and temp value. |
| 27 | Standalone — Multi-sensor logic | Wire both MQ-2 AND temperature. Combined alert: if BOTH → "DANGER: FIRE + GAS" (worst case). If only one → specific message. |
| 28 | Standalone — Housing + mounting | Build a wall-mounted alarm panel from cardboard. Mount LCD at top, LEDs below, buzzer at bottom. Label: "GAS & FIRE DETECTOR". |
| 29 | Standalone — Complete test | Test all scenarios: gas only, heat only, both, neither. Each should display correctly and trigger correct alert pattern. |
| 30 | Earthquake sensor build (MPU-6050 bonus) | Use MPU-6050: detect sudden acceleration spike (shake the table). If spike > threshold → LCD shows "SEISMIC ALERT!" + buzzer. |
| 31 | Mock Exhibition prep — Chain Project | Practice demonstrating the car: approach wall → LCD counts down → car slows → stops. Dim lights → headlights on. Name all 6 years of upgrades. |
| 32 | Mock Exhibition prep — Standalone | Practice gas/fire detector demo: wave hand near sensor, show different LCD messages for different alerts. Explain real-world application. |
| 33 | Peer review + cross-testing | One team holds a lighter (unlit) near another team's gas detector. Does it trigger? Test at 5cm, 10cm, 20cm. What's the range? |
| 34 | Final fixes + code cleanup | Refactor code: add comments to every function. Ensure no unused variables. Clean up Serial.println debug lines. |
| 35 | Exhibition boards + sensor story cards | For each sensor used, write a "sensor story" card: sensor name, how it works (1 sentence), where it's used in real life (1 example). |
| 36 | 🎉 Year-End Exhibition | Demo Smart RC Car with LCD dashboard + Gas & Fire Detector. Visitors hold up their hand near the car and watch the LCD distance count down. |

---

## 🔗 Chain Project Deep-Dive: RC Car with Ultrasonic + LCD Dashboard

**What You Bring from 5th Class:** Arduino Uno on the car chassis, IR obstacle sensor, LDR headlights, L298N motor driver. All functional.

**What You Add This Year:**
1. **HC-SR04 Ultrasonic** — replaces or supplements IR sensor. Measures actual distance in cm (not just "obstacle yes/no")
2. **16×2 LCD I2C** — mounted on car body as a dashboard. Shows: distance to obstacle + status message
3. **Speed zones** — code slows the car as it approaches, stops it close-up. Intelligent braking!
4. **Refined headlights** — hysteresis added to prevent flicker

**The Upgrade Story:** The IR sensor in 5th class only said "yes/no." The ultrasonic sensor says "34cm." That's the difference between a smoke detector and a radar. The LCD makes this information visible — like the dashboard of a real car!

**Key Code Additions:**
```cpp
// Distance-based speed control
void loop() {
  long duration, distance;
  digitalWrite(TRIG_PIN, LOW); delayMicroseconds(2);
  digitalWrite(TRIG_PIN, HIGH); delayMicroseconds(10);
  digitalWrite(TRIG_PIN, LOW);
  duration = pulseIn(ECHO_PIN, HIGH);
  distance = duration * 0.034 / 2;
  
  lcd.setCursor(0, 0);
  lcd.print("DIST: "); lcd.print(distance); lcd.print("cm ");
  
  if (distance < 15) {
    stopMotors();
    lcd.setCursor(0, 1); lcd.print("OBSTACLE!      ");
  } else if (distance < 35) {
    forward(100);  // Slow speed
    lcd.setCursor(0, 1); lcd.print("CAUTION        ");
  } else {
    forward(200);  // Full speed
    lcd.setCursor(0, 1); lcd.print("CLEAR          ");
  }
}
```

**Keep It:** The car now has a working dashboard display and smart braking. In 7th class, a servo motor mounts the ultrasonic sensor so it can SCAN left and right — turning the car into a full autonomous obstacle-avoidance robot!

---

## 🚀 Standalone Problem-Solving Project: Gas Leak & Fire Detector

**The Real-World Problem:** LPG gas leaks are invisible and odorless (the smell is added artificially). Electrical fires start silently. By the time you notice, it may be too late. Early detection = saved lives.

**Your Solution:** A wall-mounted detector with dual sensors — one for gas/smoke, one for high temperature. Different threats show different messages on the LCD, with corresponding audio-visual alerts.

**How It Works:**
- MQ-2 detects gas/smoke concentration → if above threshold → red LED + buzzer + LCD: "! GAS LEAK ! / EVACUATE NOW"
- DHT22 detects temperature → if above 50°C → yellow LED + buzzer pattern 2 + LCD: "HIGH TEMP! / CHECK FOR FIRE"
- Both triggered → LCD: "DANGER: GAS + FIRE" — maximum alert mode

**Components Needed:**

| Component | Role |
|-----------|------|
| Arduino Uno | Brain — reads sensors, controls outputs |
| MQ-2 sensor | Detects LPG, methane, smoke |
| DHT22 | Reads temperature |
| 16×2 LCD I2C | Displays alert messages |
| Active buzzer | Audio alert |
| Red LED + 220Ω | Gas alert visual |
| Yellow LED + 220Ω | Temperature alert visual |
| 9V battery + clip | Power source |
| Cardboard panel | Wall-mount housing |

**Real-World Connection:** MQ-series sensors are in every commercial gas detector. Your version, though simplified, uses the SAME sensing principle. The main difference is calibration accuracy — and that's an engineering problem even professionals spend years perfecting!

---

## Year-End Exhibition

Students demonstrate TWO projects:

1. **Smart RC Car with LCD Dashboard** — drive toward a wall, visitors watch the distance count down on the LCD. Lights come on when a student covers the LDR. Name all 6 years of upgrades since 1st class!
2. **Gas & Fire Detector** — wave a hand near the MQ-2 sensor (exhaled CO2 can trigger it). Show the different LCD messages. Explain what "threshold" means in programming.

**Connection:** The car now has a dashboard — just like a real vehicle. In 7th class, the ultrasonic sensor gets mounted on a servo motor, so it can SCAN LEFT and RIGHT, and the car autonomously chooses which way to turn. It stops reacting — and starts planning!

---

## Assessment

| Component | Weight | What's Evaluated |
|-----------|--------|-----------------|
| Session participation & sensor challenges | 20% | Sensor story cards accuracy, debugging effort |
| "Sensor Story" cards (Session 35) | 10% | 5 sensors each with real-world connection explained |
| Chain Project — RC Car with LCD dashboard | 35% | Distance shows on LCD? Speed zones work? Headlights auto-trigger? 6-year journey explained? |
| Standalone Project — Gas + Fire Detector | 35% | Both sensors trigger correctly? LCD messages accurate? Different alerts for different threats? Real-world problem explained? |
