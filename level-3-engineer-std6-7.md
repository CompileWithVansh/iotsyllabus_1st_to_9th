# LEVEL 3 — ENGINEER ⚙️
## Standards 6th–7th | Theme: "Pure Electronics — ICs, Gates & Transistors"
### 36 Sessions × 1 hr | 9 Months

---

## Overview
This level bridges hardware fundamentals with smart systems. Students learn how circuits "think" WITHOUT any microcontroller — using transistors, logic gate ICs, timers, comparators, and voltage regulators. By the end, they introduce Arduino Nano for autonomous projects that combine IC knowledge with programming.

> **Core principle:** Understand the silicon. Most students go their whole career without knowing why a circuit works. At this level, they will.

---

## Component Inventory

| Category | Components |
|----------|-----------|
| Transistors | BC547 NPN transistor, BC557 PNP transistor |
| Logic Gate ICs | 7408 (AND), 7432 (OR), 7404 (NOT), 7486 (XOR), 7400 (NAND) |
| Timer IC | NE555 (used in astable + monostable modes) |
| Op-Amp IC | LM358 (used as comparator) |
| Voltage Regulator | 7805 (5V from 9V input) |
| Counter IC | CD4026 (7-segment counter — no Arduino needed) |
| Motor Driver IC | L293D / L298N (used and understood internally) |
| Display | 7-segment display (common cathode), 16×2 LCD I2C |
| Relay | 5V relay module |
| Sensors | LDR, BC547-connected sensors, PIR (for Nano projects) |
| Microcontroller (late level) | Arduino Nano (Sessions 26–36 only) |
| Passive Components | Resistors (220Ω, 1kΩ, 10kΩ), capacitors (10µF, 100µF, 0.01µF), LEDs, buzzer, speaker (8Ω) |
| Power | 9V battery + clip, 5V USB supply, breadboard, jumper wires |

---

## UNIT 1 — BC547 NPN Transistor (Sessions 1–3)
*"The world's most important tiny switch"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 1 | Transistor anatomy — Base, Collector, Emitter | Identify legs using datasheet. Wrong leg → doesn't work. Right leg → LED controlled by finger touch |
| 2 | BC547 as a switch — base resistor math | Small signal at base (from LDR) → controls large current at collector → LED ON/OFF without switch |
| 3 | BC547 as amplifier concept + BC557 PNP | Compare NPN vs PNP: which pin is the "trigger"? Build complementary pair circuit |

---

## UNIT 2 — Transistor Applications (Sessions 4–5)
*"Real circuits, no Arduino"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 4 | **Automatic Night Light (no Arduino!)** | LDR → base of BC547 via resistor. Dark = high resistance = transistor OFF → LED OFF. Light = low resistance = transistor ON → LED ON. Wire it up. It just works. |
| 5 | **Touch-Activated Buzzer** | No button. Just touch two exposed wires with finger. Skin resistance activates BC547 base → buzzer sounds. Scary-simple, surprisingly effective |

> **WOW factor:** Session 5 project works because human skin has resistance. Students literally become part of the circuit!

---

## UNIT 3 — Logic Gates (Sessions 6–9)
*"How computers really think — one gate at a time"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 6 | Binary thinking + AND gate (7408 IC) | 2 switches → AND gate → LED only if BOTH are ON. Truth table exercise with physical circuit |
| 7 | OR gate (7432) + NOT gate (7404) | Build a home alarm: buzz if door OR window is opened. NOT gate inverts signal — add inverted output LED |
| 8 | XOR gate (7486) + NAND gate (7400) | XOR: "different inputs = output". NAND: everything inverted AND. Truth table race: which team finishes first? |
| 9 | **Challenge: Logic Gate Combination Lock** | 3 switches. Only specific combination (e.g., SW1=ON, SW2=OFF, SW3=ON) using AND + NOT gates → LED unlocks. Wrong combo = buzzer |

> **WOW factor:** A real working 3-switch combination lock — no Arduino, no code. Pure logic gate circuits!

---

## UNIT 4 — 555 Timer IC (Sessions 10–13)
*"The most used IC in history"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 10 | 555 timer — 8 pins explained, internal block diagram | Why does it have 8 pins? What is a trigger, threshold, output? Walk through with printed diagram |
| 11 | Astable mode — automatic oscillator (blink without code) | 555 + 2 resistors + capacitor → LED blinks automatically! Change capacitor → change speed |
| 12 | Monostable mode — one-shot timer | Press button → 555 triggers → LED stays on for exactly N seconds → turns off. Change RC = change duration |
| 13 | **Project: 555 Police Siren** | Two 555 timers chained: first modulates frequency of second → speaker produces rising/falling siren tone. No Arduino. Purely analog! |

> **WOW factor:** Two 555 chips + resistors + capacitors + speaker = a siren that sounds genuinely realistic. Students wire it from scratch!

---

## UNIT 5 — LM358 Op-Amp as Comparator (Sessions 14–15)
*"Automatic decision-making in a chip"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 14 | LM358 — what is an op-amp? Comparator mode | Compare two voltages: if pin 2 > pin 3 → output HIGH. Wire LDR as voltage divider on one input, pot on the other |
| 15 | **Project: Automatic Light (LM358 version)** | LDR + LM358 comparator → LED auto-triggers at darkness threshold set by pot. No Arduino. No code. Adjust pot to set sensitivity |

---

## UNIT 6 — 7805 Voltage Regulator (Sessions 16–17)
*"Build your own 5V power supply"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 16 | Why do we need voltage regulation? Measure 9V → unstable. 5V → stable | 7805 datasheet: 3 pins (Input, Ground, Output). Measure input with multimeter |
| 17 | **Build: 5V Regulated Power Supply** | 9V battery → 7805 → filter capacitors → 5V output. Measure with multimeter. Power a 5V LED from it. Students now have a bench power supply they built! |

---

## UNIT 7 — CD4026 Counter + 7-Segment (Sessions 18–20)
*"Count goals, score points — no Arduino"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 18 | 7-segment display — how it works, segment mapping | Manually connect segment pins → show digits 0–9 by hand |
| 19 | CD4026 IC — clock input counts up automatically | Press button → CD4026 counts → digit increments on 7-segment. Wire reset button |
| 20 | **Project: Automatic Score Counter** | Push button = "goal scored". CD4026 + 7-segment shows score 0–9. Reset button. Mount on cardboard football goal. Count goals in a game! |

> **WOW factor:** Every press of a button increments the score on the display. No microcontroller anywhere!

---

## UNIT 8 — Relay Module (Sessions 21–22)
*"Control the real world safely"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 21 | Relay — what it is, why we need it | A relay is a switch controlled by a small signal. Open relay module, see coil + contacts. NEVER connect 230V — demo only with LED bulb |
| 22 | Relay with transistor drive | BC547 drives relay coil (transistor amplifies signal). Connect 9V lamp to relay contacts. Small Arduino signal → relay → lamp ON |

---

## UNIT 9 — IC-Only Combination Projects (Sessions 23–25)
*"Build real machines with just chips"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 23 | Combine: 555 timer + transistor + relay | 555 timer fires after N seconds → transistor drives relay → relay clicks lamp ON. Programmable timer without Arduino! |
| 24 | **MID-YEAR PROJECT** | Individual: choose one from the table below. 45-minute build |
| 25 | MID-YEAR PROJECT continued + presentations | Each student presents circuit, explains every component's role |

### Mid-Year Project Options (IC-only, no Arduino):

| Project | Components | WOW Factor |
|---------|-----------|-----------|
| **Automatic Night Light** | LDR + BC547 + LED | Light auto-triggers with zero code |
| **Logic Lock** | 7408 + 7404 + 7432 + 3 switches | Correct combo = green LED. Wrong = red + buzzer |
| **Police Siren** | 2× NE555 + speaker + capacitors | Realistic rising/falling siren tone |
| **Score Counter** | CD4026 + 7-segment + push button | Count anything: goals, jumps, points |
| **Touch Buzzer** | BC547 + exposed contacts + buzzer | Touch wires → buzzer fires |

---

## UNIT 10 — Arduino Nano Introduction (Sessions 26–27)
*"Same power, smaller package"*

| Session | Topic | Activity / Challenge |
|---------|-------|---------------------|
| 26 | Nano pinout vs Uno — differences and similarities | Flash blink sketch using Nano. Understand Nano's smaller form factor — why useful for robots |
| 27 | Power the Nano from 7805 supply (built in Unit 6!) | Students power Nano from their own 5V regulator build. Satisfying! |

---

## UNIT 11 — Nano Autonomous Projects (Sessions 28–36)

### Year-End Project Options (Arduino Nano + IC knowledge combined):

| # | Project | Components | WOW Factor |
|---|---------|-----------|-----------|
| 1 | **Smart Dustbin** | HC-SR04 + servo + 16×2 LCD + Nano | Ultrasonic detects hand → servo lifts lid. LCD shows "EMPTY" / "FULL" based on inner sensor |
| 2 | **Automatic Street Light with Override** | LDR + PIR + relay + Nano | LDR controls auto-on at dusk. PIR overrides: motion → light on regardless. Relay switches load |
| 3 | **Soil Moisture Irrigation Controller** | Soil sensor + relay + water pump (small DC) + LCD + Nano | Dry soil → relay triggers pump. Wet → pump off. LCD shows moisture % |
| 4 | **Blind-Stick Ultrasonic Alert** | HC-SR04 + BC547 + buzzer + Nano | Ultrasonic measures distance → Nano calculates → BC547 drives buzzer harder as object gets closer. Vibration alert |
| 5 | **Logic Gate Security Door** | 7408 AND gate + 3 switches + servo + Nano | 3 switches in AND combination → Nano reads output → servo opens door. Wrong combo = locked + buzzer |

| Session | Activity |
|---------|----------|
| 28 | Project selection + problem statement |
| 29 | Circuit design + component assignment |
| 30 | Hardware build — breadboard |
| 31 | Code development — sensor reading |
| 32 | Full code + outputs |
| 33 | Integration + initial testing |
| 34 | Debugging + enclosure |
| 35 | Presentation preparation + mock run |
| 36 | **YEAR-END EXHIBITION 🎉** |

---

## Assessment Framework

| Component | Weight |
|-----------|--------|
| Unit challenges (hands-on) | 20% |
| Mid-year IC-only project | 30% |
| Year-end Nano autonomous project | 50% |
