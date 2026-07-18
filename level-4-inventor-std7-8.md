# LEVEL 4 — INVENTOR 🕹️
## Standards 7th–8th | Theme: "Autonomous Robots + RC + Wireless Control"
### 36 Sessions × 1 hr | 9 Months

---

## Overview
Every previously learned concept applies here. Students build fully autonomous robots, wire up real RC controllers, integrate Bluetooth phone control, and create multi-sensor intelligent machines. Year-end projects look like professional prototypes — not school projects.

---

## Component Inventory

| Category | Components |
|----------|-----------|
| Microcontroller | Arduino Nano (primary), Arduino Uno (for flashing Nano via Uno board trick) |
| Robot Chassis | 2-wheel + caster chassis kit, DC motors × 2, motor wheels, screws |
| Motor Driver | L298N motor driver module |
| RC Control | FlySky FS-i6 transmitter (6-channel), FlySky FS-iA6B receiver |
| Wireless | HC-05 Bluetooth module, HC-12 radio module (long-range wireless) |
| IR Control | TSOP1738 IR receiver, standard TV remote (any brand) |
| Stepper | 28BYJ-48 stepper motor + ULN2003 driver board |
| Sensors | HC-SR04 ultrasonic × 2 (front + side), IR sensors × 2, servo SG90 for scanning |
| Display | 16×2 LCD I2C, OLED 0.96" I2C |
| Power | 9V battery, 7.4V Li-ion pack (for robot), 5V USB for Nano |
| Misc | Buzzer, LEDs, 220Ω resistors, 1kΩ resistors, breadboard, jumper wires |

---

## UNIT 1 — Arduino Nano Deep Dive (Sessions 1–3)
*"Nano is the future — smaller, faster, robot-ready"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 1 | Nano pinout, power pins, digital/analog differences vs Uno | Sketch labels every pin. Upload blink via Uno board (Nano lacks USB-serial chip trick) |
| 2 | Flashing Nano via Uno as ISP — the board trick | Remove Uno's chip, upload ArduinoISP sketch, connect Nano → flash successfully. Understand why this works |
| 3 | `millis()` instead of `delay()` — non-blocking code | Traffic light using millis() — all 3 LEDs can respond to button interrupt mid-sequence |

---

## UNIT 2 — Full Robot Chassis Assembly (Sessions 4–7)
*"Wheels down. Let's drive."*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 4 | Mechanical build — chassis, motors, wheels, caster | Full assembly from kit. Measure motor shaft, confirm wheel fit |
| 5 | L298N wiring — power, motor terminals, input pins | Wire both motors to L298N. Power from battery. Test each motor manually |
| 6 | Drive code — `digitalWrite()` to IN1/IN2/IN3/IN4 + PWM to ENA/ENB | Forward, backward, turn left, turn right functions |
| 7 | **Challenge: Serial Monitor Driving** | Type F/B/L/R/S in Serial Monitor → robot responds. Calibrate turn timing |

---

## UNIT 3 — IR Remote Control (Sessions 8–10)
*"Your TV remote now controls a robot"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 8 | TSOP1738 IR receiver — how IR remote signals work | Add `IRremote.h` library. Point any TV remote → Serial Monitor prints hex code for each button |
| 9 | Map hex codes to actions | Write: if code == 0xFF18E7 → forward. Else if code == 0xFF4AB5 → backward. Etc. |
| 10 | **Build: IR Remote-Controlled Car** | Full robot + TSOP1738 + TV remote. Drive the car with standard TV remote buttons. Seriously impressive! |

> **WOW factor:** Students walk in holding a TV remote and drive a robot car they built. The reaction from visitors at exhibition is always amazing.

---

## UNIT 4 — FlySky RC Integration (Sessions 11–14)
*"Real RC racing — professional grade"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 11 | FlySky FS-i6 transmitter + FS-iA6B receiver — binding | Bind TX/RX. Connect receiver PPM/SBUS output to Nano. Serial Monitor: watch channel values change as you move joystick |
| 12 | `pulseIn()` to read PWM channel values | Channel 1 (throttle): 1000–2000µs → `map()` to motor speed -255 to 255 |
| 13 | Proportional steering — Channel 2 controls turn | Joystick angle = turn sharpness. Not just left/right toggle — smooth proportional control |
| 14 | **Build: FlySky RC Car with Obstacle Stop** | Full RC car. Add ultrasonic to front. If obstacle < 15cm → motors stop regardless of joystick position. Manual RC + auto safety |

> **WOW factor:** Students race their RC cars with professional FlySky controllers. Visitors assume it's a commercial RC car until they see the Arduino!

---

## UNIT 5 — Bluetooth Smartphone Control (Sessions 15–17)
*"Your phone IS the remote"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 15 | HC-05 Bluetooth module — AT mode, pairing | AT+NAME, AT+BAUD commands. Pair with phone via "Serial Bluetooth Terminal" app |
| 16 | Robot control via phone app (Bluetooth RC Controller or custom app) | Send F/B/L/R/S bytes from phone → robot moves |
| 17 | **Build: BT Robot with Auto Obstacle Stop** | Phone controls robot via Bluetooth. Ultrasonic sensor auto-stops if obstacle detected. Phone only drives; safety is autonomous |

---

## UNIT 6 — Stepper Motor (Sessions 18–20)
*"Precision positioning — degrees, not speed"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 18 | 28BYJ-48 + ULN2003 driver — steps, half-steps | `Stepper.h` library. Rotate exactly 90°, then 45°, then 180° |
| 19 | Stepper for position control | Button A → rotate clockwise 90°. Button B → rotate back |
| 20 | **Build: Combination Safe** | 3 buttons define a sequence code (e.g., A-B-A-A). Enter correct sequence → stepper rotates → "safe door opens". Wrong sequence → buzzer |

> **WOW factor:** A mechanical safe with a real electronic combination. Guests try to crack the code at the exhibition!

---

## UNIT 7 — Autonomous Obstacle Avoidance + Line Following (Sessions 21–23)
*"Robots that think for themselves"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 21 | Dual ultrasonic (front + side) — 3D awareness | Read front distance + left distance simultaneously. Print both on LCD |
| 22 | Obstacle avoidance with servo scanning | Servo rotates ultrasonic left/right → scan → choose direction with most space → turn that way |
| 23 | **Build: Obstacle Avoidance + Line Follow Combined** | IR sensors follow black tape. Ultrasonic overrides: if wall detected → stop line follow → avoid → resume. Real autonomous behavior! |

---

## 🏆 MID-YEAR PROJECT (Sessions 24–25)
### RC Car Race with Obstacles — Team vs Team

| Format | Details |
|--------|---------|
| **Team size** | 2–3 students per team |
| **Track** | Obstacle course set up in classroom/hall |
| **Vehicle** | Each team's FlySky RC car built in Unit 4 |
| **Scoring** | Fastest lap + bonus for not hitting obstacles |
| **Twist** | One team uses BT phone control vs another uses FlySky — which is better? |

**Evaluation:** Vehicle performance + explain how the auto-stop works + describe one code function

---

## UNIT 8 — Year-End Complex Autonomous Project (Sessions 26–36)

### Year-End Project Options (teams of 2–3):

| # | Project | Components | WOW Factor |
|---|---------|-----------|-----------|
| 1 | **Autonomous Emergency Vehicle** | FlySky RC + dual ultrasonic + buzzer + LCD + Nano | FlySky manual mode + press button → autonomous obstacle avoid mode. Siren sounds. LCD shows "EMERGENCY MODE / MANUAL MODE" |
| 2 | **Smart Parking System** | 3× HC-SR04 + 3× servo barriers + LED indicators + LCD + Nano | 3 parking slots. Ultrasonic detects if car present. LED: red = full, green = empty. LCD shows "SLOTS: 2/3 AVAILABLE". Servo barrier lifts automatically |
| 3 | **Hospital Medicine Delivery Robot** | IR line follow + HC-SR04 + LCD + BT + Nano | Follows line. LCD shows room number. Bluetooth override: send "OVERRIDE" from phone → manual control. Obstacle stop built in |
| 4 | **Search and Rescue Bot** | BT control + dual ultrasonic scan + OLED display + Nano | BT-controlled by phone. OLED shows distance readings left/right/front like a radar. Camera mount (phone holder) for "FPV" view |
| 5 | **Robotic Arm with IR Remote** | 3× servo SG90 + TSOP1738 + TV remote + Nano | 3 servo joints: base, elbow, gripper. TV remote controls each joint independently. Pick up a bottle cap and place it in a box |

| Session | Activity |
|---------|----------|
| 26 | Project selection + problem definition |
| 27 | Circuit schematic + mechanical design sketch |
| 28 | Component preparation + hardware build start |
| 29 | Hardware build + wiring |
| 30 | Code phase 1 — basic sensor reads + movement |
| 31 | Code phase 2 — full logic + integration |
| 32 | Hardware + code combined testing |
| 33 | Debugging + reliability testing (run 5 times, must work 4/5) |
| 34 | Enclosure / model casing / presentation prop |
| 35 | Presentation script + mock demo |
| 36 | **YEAR-END EXHIBITION 🎉** |

---

## Assessment Framework

| Component | Weight |
|-----------|--------|
| Unit challenges | 15% |
| Mid-year RC race + explanation | 30% |
| Year-end autonomous project | 55% |
