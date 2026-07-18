# 🤖 Standard 7 — Autonomy
## Theme: "Robots That Think"
### 36 Sessions × 1 hr | 9 Months

---

## What You'll Build This Year

- **🔗 Chain Project:** Major upgrade — swap Arduino Uno → Arduino Nano. Add a servo-mounted HC-SR04 scanner that SCANS left and right, measures distances in multiple directions, then DECIDES which way to turn. Shows status on OLED: "SCANNING… TURNING LEFT". Full autonomous obstacle avoidance with actual intelligence!
- **🚀 Standalone Project:** Smart Parking System — 3× HC-SR04 sensors (3 parking slots) + 3× LEDs (red = full, green = empty) + LCD shows "SLOTS: 2/3 AVAILABLE". A real parking management simulation.

---

## Component Inventory

| Category | Components |
|----------|-----------|
| From Last Year | RC Car chassis (motors, wheels, L298N, caster, old components removed) |
| Microcontroller | Arduino Nano, USB cable (mini-B), 9V battery + clip |
| Scanning | Servo SG90 (for ultrasonic mount), HC-SR04 × 2 (front scan + side reference) |
| Display | OLED 0.96" I2C |
| Stepper | 28BYJ-48 stepper motor + ULN2003 driver board |
| Line Following | IR sensor modules × 2 (for floor tracking) |
| RC Control | FlySky FS-i6 transmitter + FS-iA6B receiver (optional / advanced) |
| Parking Project | HC-SR04 × 3, LEDs (red × 3, green × 3), 220Ω resistors × 6, 16×2 LCD I2C |
| Output | Active buzzer, jumper wires, breadboard, screws/tape for mounting |
| Power | 9V batteries × 2, battery clips, USB for Nano |

---

## Session Plan

| Session | Topic | Activity |
|---------|-------|----------|
| 1 | Arduino Nano vs Uno — what's different? | Side by side comparison: same ATmega328 chip, smaller form factor, no USB-serial chip. Why use Nano for robots? Size + weight savings. |
| 2 | Flash Nano via Uno — the board trick | Remove Uno chip. Upload ArduinoISP sketch. Connect Nano → flash via Uno as ISP. Success! Understand why this works. |
| 3 | `millis()` — non-blocking code | Problem with `delay()`: car can't react while waiting. Use `millis()` instead. Traffic light with millis() — button press works mid-sequence. |
| 4 | Servo SG90 — `Servo.h`, `write()`, `sweep` | `servo.write(90)` = center. `servo.write(0)` = left. `servo.write(180)` = right. Sweep 0→180→0 slowly. |
| 5 | Servo + ultrasonic — the scanner | Mount HC-SR04 on servo. Write: scan left (0°) → measure distance. Scan center (90°) → measure. Scan right (180°) → measure. Print 3 values. |
| 6 | Scanning decision algorithm | Logic: `if (distRight > distLeft)` → "More space RIGHT". Else → "More space LEFT". Print decision to Serial Monitor. |
| 7 | Stepper motor 28BYJ-48 — steps and precision | Install Stepper.h. `stepper.step(512)` = 360°. Rotate exactly 90°. Then 45°. Precision position control. |
| 8 | Stepper for exact positioning | Button A → stepper rotates clockwise 90°. Button B → counterclockwise 90°. Build a pointer that points to N/E/S/W. |
| 9 | Stepper combination safe | 3 buttons = secret code sequence. Enter correct sequence (A-B-A-A) → stepper "opens" safe. Wrong → buzzer. |
| 10 | Line follower — dual IR sensors | Wire 2 IR sensors to digital pins. Both LOW → on black tape line → forward. Left HIGH → right of line → turn left. Right HIGH → left of line → turn right. |
| 11 | Line follower calibration | Calibrate sensor height (3–5mm from floor). Create black tape track on white paper. Test line following. Debug veering behavior. |
| 12 | Line follower + obstacle override | Line follow until obstacle detected (ultrasonic < 15cm) → pause line follow → avoid → resume. Real autonomous combined behavior! |
| 13 | OLED status display for robot | Display robot state: "MODE: DRIVING", "MODE: AVOIDING", "DIST: XXcm". States change in real time as robot operates. |
| 14 | FlySky FS-i6 — binding TX/RX | Bind transmitter to receiver. Connect receiver PWM output to Nano pin. `pulseIn()` reads 1000–2000µs channel values. |
| 15 | FlySky proportional control | `map(channelValue, 1000, 2000, -255, 255)` → motor speed. Joystick angle = speed + direction. Proportional, not just on/off! |
| 16 | RC car with FlySky — test drive | Full RC car control from FlySky transmitter. Smooth proportional steering. Race around a course! |
| 17 | **Chain Project Session 1** — Swap Uno → Nano | Remove Arduino Uno from car. Mount Arduino Nano in its place (smaller, lighter). Re-wire all connections (same pins, smaller board). |
| 18 | **Chain Project Session 2** — Servo scanner mount | 3D print or cut a small bracket. Mount servo on front of car. Mount HC-SR04 on top of servo. Servo can now rotate the "eyes" left/right. |
| 19 | **Chain Project Session 3** — Scanning algorithm | Upload scanning code: obstacle in front → servo scans → measures left distance + right distance → picks larger → turns that way. |
| 20 | **Chain Project Session 4** — OLED dashboard | Mount OLED on car body. Show: current state (SCANNING / TURNING LEFT / CLEAR), front distance in cm. Real-time status! |
| 21 | **Chain Project Session 5** — Autonomous behavior tuning | Test in an obstacle course. Does it always choose the right direction? Add: if BOTH sides blocked → reverse + try again. Edge case handling! |
| 22 | **Chain Project Session 6** — Speed + smoothness | Add gradual acceleration (ramp from 0 to 200 over 0.5 seconds). Adds to both speed control and reduces wheel slip on turns. |
| 23 | **Chain Project Complete** — Full test + documentation | 10-lap test in obstacle course. Document OLED messages observed. Write code comments. Create 7-year upgrade poster. |
| 24 | **Standalone Project** — Parking system concept | Real problem: people circle parking lots for minutes without knowing if any slots are free. Wasted time + fuel. Solution: sensor array at each slot. |
| 25 | Standalone — Single slot sensor | Wire HC-SR04 above a "slot" (box with 15cm ceiling). Car present → distance < 10cm. No car → distance > 10cm. LED: RED if occupied, GREEN if empty. |
| 26 | Standalone — Three slots | Repeat for 3 slots. Three HC-SR04 sensors, three LED pairs (R+G each). Test each independently. |
| 27 | Standalone — Count available slots | Count how many green LEDs are active = available slots. Print to LCD: "SLOTS: 2/3 AVAILABLE". |
| 28 | Standalone — LCD display logic | Update LCD every 500ms. Line 1: "PARKING STATUS". Line 2: "AVAILABLE: X/3". If 0 available → Line 2: "FULL — SORRY!". |
| 29 | Standalone — Physical mock parking lot | Build a cardboard parking lot with 3 bays. Place toy cars in bays. Watch LEDs and LCD update as cars are placed/removed. |
| 30 | Standalone — Testing + edge cases | What if a person walks through a slot? (false positive). Add: only count as "occupied" if reading < 10cm for 3 consecutive readings. Debounce! |
| 31 | Mock Exhibition prep — Chain Project | Practice: explain the scanning algorithm in plain English. Demonstrate obstacle course run. Say all 7 years of upgrades from memory. |
| 32 | Mock Exhibition prep — Standalone | Practice: place toy car in slot → LED changes → LCD updates. Explain real-world application (shopping malls, airports). |
| 33 | Peer review — obstacle course time trial | Teams swap robots. One team drives the OTHER team's autonomous car (put it on auto mode and let go). Fastest obstacle-free run wins. |
| 34 | Final code cleanup + commenting | Print final code. Every function, every variable, every `if` block has a comment explaining WHY (not just what). |
| 35 | Exhibition boards + 7-year upgrade visual | Create a poster showing all 7 years: Bug → RC → Lights+Horn → Auto-lights → Arduino → Sensors → Autonomous. Arrow showing progression. |
| 36 | 🎉 Year-End Exhibition | Demo Autonomous Scanning Robot (visitors set obstacles and watch it navigate!) + Smart Parking System (place toy cars, watch LCD update). |

---

## 🔗 Chain Project Deep-Dive: Full Autonomous Obstacle Avoidance Robot

**What You Bring from 6th Class:** RC Car with Arduino Uno, HC-SR04 ultrasonic, L298N, LDR headlights, LCD distance display. All functional.

**What You Change This Year:**
- Swap Arduino **Uno → Nano** (smaller, fits better on car body)
- Remove LCD from car (too heavy/large) → Replace with OLED (smaller)
- Add servo-mounted HC-SR04 for SCANNING

**What You Add This Year:**
1. **Servo Scanner** — servo sweeps HC-SR04 left (45°), center (90°), right (135°). Measures distance at each angle.
2. **Decision Algorithm** — if front blocked: scan left → note distance. Scan right → note distance. Turn toward more space.
3. **OLED Dashboard** — live display of: state + front distance
4. **Edge case handling** — if BOTH directions blocked → reverse 0.5s → scan again

**The Upgrade Story:** In 6th class the car measured one distance. Now it scans THREE directions and MAKES A CHOICE. That's the definition of autonomy — taking environmental data and deciding what to do. This is the algorithm every real self-driving car uses (at a much higher resolution)!

**Scanning Code:**
```cpp
void scanAndDecide() {
  servo.write(45);  delay(300);
  int distRight = measureDistance();
  
  servo.write(90);  delay(300);
  int distFront = measureDistance();
  
  servo.write(135); delay(300);
  int distLeft = measureDistance();
  
  servo.write(90);  // Return to center
  
  oled.clearDisplay();
  oled.println("SCANNING...");
  
  if (distFront > 30) {
    forward(180); oled.println("CLEAR");
  } else if (distRight > distLeft) {
    turnRight(); delay(400); oled.println("TURN RIGHT");
  } else if (distLeft > distRight) {
    turnLeft(); delay(400); oled.println("TURN LEFT");
  } else {
    backward(); delay(500); oled.println("REVERSING");
  }
}
```

**Keep It:** This is now a genuine autonomous robot. In 8th class it gets Bluetooth control (manual override mode) AND connects to the internet via ESP8266 to broadcast its status to a Blynk dashboard!

---

## 🚀 Standalone Problem-Solving Project: Smart Parking System

**The Real-World Problem:** In busy cities, drivers spend an average of 17 minutes searching for parking. That's wasted time, wasted fuel, and added frustration. Parking guidance systems that show availability in real time are already in large malls — but small parking lots can't afford them.

**Your Solution:** A low-cost ultrasonic sensor array at each parking slot. Red LED = slot occupied. Green LED = slot empty. LCD shows total count. Entry sign lights up green when slots are available.

**How It Works:**
- 3× HC-SR04 sensors, one above each parking bay (10cm threshold)
- Car in bay → distance < 10cm → red LED on, green LED off
- Bay empty → distance > 10cm → green LED on, red LED off
- Arduino counts available slots → LCD shows "AVAILABLE: 2/3"
- If count = 0 → LCD: "FULL — SORRY!" (entry sign turns red)

**Components Needed:**

| Component | Role |
|-----------|------|
| Arduino Nano | Reads all 3 sensors, controls LEDs, updates LCD |
| HC-SR04 × 3 | One per parking slot — detects car presence |
| Red LED × 3 + 220Ω | "Slot occupied" indicator |
| Green LED × 3 + 220Ω | "Slot empty" indicator |
| 16×2 LCD I2C | Shows available count |
| 9V battery + clip | Power source |
| Cardboard parking lot | Physical model with 3 bays |

**Scale-up Vision:** Real systems use the exact same principle but add a wireless component — each sensor reports to a central server, which updates digital signs at parking entrances. Your model is a 1:1 functional replica of that concept!

---

## Year-End Exhibition

Students demonstrate TWO projects:

1. **Autonomous Robot** — place random cardboard obstacles in a 1m² area. Start the robot. Watch it scan, decide, and navigate without hitting anything. Visitors can add/remove obstacles! Explain the scanning algorithm.
2. **Smart Parking System** — visitors place toy cars in different bays. Watch LEDs switch from green to red. Watch the LCD count update. Remove a car → slot goes green again. Explain: "This is how airport parking works!"

**Connection:** The robot is now fully autonomous. In 8th class it gets a Bluetooth module so visitors can MANUALLY control it with their phone — and you write code to switch between MANUAL and AUTO mode. Two modes, one robot!

---

## Assessment

| Component | Weight | What's Evaluated |
|-----------|--------|-----------------|
| Session challenges (servo, stepper, line follow) | 20% | Precision of servo angles, stepper steps, line follow accuracy |
| Code documentation (Session 34) | 10% | Every block commented, logic explained clearly |
| Chain Project — Autonomous Robot | 35% | Consistent obstacle avoidance? OLED updates correctly? Scanning algorithm explained? 7-year journey articulated? |
| Standalone Project — Parking System | 35% | All 3 slots detect correctly? LCD count accurate? Real-world problem explained with genuine understanding? |
