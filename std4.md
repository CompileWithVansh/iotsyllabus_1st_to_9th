# 🔬 Standard 4 — Electronics
## Theme: "Logic Control, Transistors & System Reflexes"
### 36 Sessions × 1 hr | 9 Months

---

## What You'll Build This Year

- **🔗 Chain Project:** Upgrade the 3rd class RC Car — Add automatic headlights using an LDR + BC547 transistor (lights come on in the dark automatically!) and a capacitor-delayed horn (press button → buzzer sounds for 2 seconds then stops). Plus a 555-timer warning blink light on top!
- **🚀 Standalone Project:** Logic Gate Combination Lock — 3 switches + AND gate + NOT gate → only the correct switch combination unlocks the "door" (LED turns green). Wrong combo = red LED + buzzer.

---

## Component Inventory

| Category | Components |
|----------|-----------|
| From Last Year | Your Enhanced RC Car (headlights + horn already installed) |
| Transistors | BC547 NPN × 3 |
| Sensors | LDR (light dependent resistor) × 1 |
| Logic Gate ICs | 7408 AND gate IC, 7432 OR gate IC, 7404 NOT gate IC |
| Timer IC | NE555 × 1 |
| Capacitors | 10µF × 2, 100µF × 2, 0.01µF (ceramic) × 1 |
| Resistors | 220Ω × 4, 1kΩ × 4, 10kΩ × 2, 100kΩ × 1 |
| LEDs | Red × 2, Green × 2, Yellow × 1 |
| Buzzers | Active buzzer × 1 |
| Switches | Toggle × 3 (for combination lock), push button × 1 |
| Power | 9V batteries × 2, battery clips, breadboard |
| Measurement | Multimeter (shared class set of 4–6) |
| Wiring | Jumper wires, IC socket strips |

---

## Session Plan

| Session | Topic | Activity |
|---------|-------|----------|
| 1 | Welcome back — measure circuit voltages! | Use multimeter to measure the voltage at different points in the RC car circuit. Where does 9V enter? Where does it drop? |
| 2 | Multimeter basics — voltage, resistance, continuity | Measure: 9V battery, voltage across LED (should be ~2V), resistance of resistors. Compare measured vs color-code values. |
| 3 | Series vs parallel pathways | Build series and parallel circuits. Use a multimeter to see how electricity divides along paths. Verify how parts share the power. |
| 4 | Meet the Transistor — The Faucet Valve | Identify the transistor's three legs: Base (the handle), Collector (the water inlet), and Emitter (the water outlet). Draw the symbol. |
| 5 | Transistor as an Automatic Switch | Wire LDR sensor to control the transistor base. When base gets a tiny signal, it opens the main gate from collector to emitter. Cover LDR = LED ON! (No math or formulas). |
| 6 | Automatic night light (no Arduino, no code!) | LDR + BC547 + LED. Dark = high LDR resistance → transistor triggered → LED glows. It just works. Add pot to adjust sensitivity threshold. |
| 7 | Touch-activated circuit | Expose two bare wires. Touch both with finger → skin resistance activates BC547 base → buzzer sounds. YOU are part of the circuit! |
| 8 | BC547 driving a buzzer (relay-like) | Small current at base drives buzzer on collector circuit. Demonstrates transistor as current amplifier — tiny signal, big result. |
| 9 | LDR auto-headlight circuit — standalone test | Wire full headlight auto-circuit: LDR + BC547 + 2 white LEDs in parallel. Cover LDR → lights come on. Uncover → lights off. |
| 10 | Planning car headlight upgrade | Sketch: how does the LDR auto-circuit replace the manual toggle switch on the car? What stays the same? What changes? |
| 11 | **Chain Project Session 1** — Remove manual headlight switch | On the car, disconnect the manual toggle switch from the headlight circuit. Replace with LDR + BC547 auto-circuit. Test in dim lighting. |
| 12 | **Chain Project Session 2** — Capacitor-delayed horn | Upgrade the horn: 9V → button → 100µF capacitor → buzzer → GND. Press button → buzzer honks for ~2 seconds → auto-stops. Time it! |
| 13 | **Chain Project Session 3** — NE555 warning blink | Wire 555 in astable mode: two resistors + capacitor → LED blinks automatically. Mount a yellow blinking LED on car roof. It blinks constantly while the car is on! |
| 14 | **Chain Project Session 4** — Full system test | Test all systems: auto-headlights (cover LDR → lights on), timed horn (button → 2-second honk), blink light (constant flash). All simultaneously! |
| 15 | **Chain Project Session 5** — Documentation | Draw complete circuit diagram with ALL 3 years of upgrades. Annotate what was added in 1st, 2nd, 3rd, 4th class. |
| 16 | Logic games — Yes and No signals | Play the Yes/No game. Red light = No, Green light = Yes. Practice passing signals through the class using rules. |
| 17 | AND gate — "Both switches must say YES" | Connect 2 switches to a 7408 AND gate. Observe: the LED turns on only when BOTH Switch A AND Switch B are closed. |
| 18 | OR gate — "Either switch can say YES" | Connect 2 switches to a 7432 OR gate. Observe: the LED turns on if Switch A OR Switch B is closed. |
| 19 | NOT gate — "The opposite / flip game" | Connect a switch to a 7404 NOT gate. Observe: when the switch is OFF, the LED is ON. It flips the signal! |
| 20 | Combining gates — "Secret Code games" | Wire a NOT gate into an AND gate. Figure out the secret switch positions to make the light shine. |
| 21 | **Standalone Project** — Logic lock concept | Real problem: security systems need a "correct code." A combination of switches = a code. Only the right pattern unlocks the door. Design your lock. |
| 22 | Standalone — Plan the 3-switch combination | Choose your secret combination: e.g., SW1=ON, SW2=OFF, SW3=ON. Design using AND + NOT gates so only this combo triggers output. |
| 23 | Standalone — Wire the gate circuit | Implement the logic: SW1 → AND gate (input A), SW2 → NOT gate → AND gate (input B), SW3 feeds into second AND gate. Only correct pattern = HIGH output. |
| 24 | Standalone — Add the unlock output | Correct combo → HIGH signal → green LED + servo (if available) OR just green LED (simulating door open). Wrong combo → always LOW → red LED + buzzer. |
| 25 | Standalone — Mount in housing | Build a "security panel" on cardboard. 3 labeled toggle switches, green/red LED display, buzzer. Make it look official! |
| 26 | Standalone — Test all combinations | Test ALL 8 possible combinations (2³ = 8). Only the correct one should open. Fill in a truth table and verify. |
| 27 | 555 Timer as a Heartbeat | Build an automatic blinking warning light using a 555 timer. Change the resistor and capacitor sizes to see how speed changes. |
| 28 | 555 Timer as a Timer Switch | Press a button -> the light stays on for a few seconds and then goes off. Change capacitor size to control timing. |
| 29 | 555 police siren (bonus build) | Two 555 timers chained: first modulates the second → speaker produces rising/falling siren. No Arduino needed! |
| 30 | Component review sprint | Blindfold challenge: identify components by touch/shape. OR speed quiz: teacher holds up component, first to name it + describe use wins a point. |
| 31 | Mock Exhibition prep — Chain Project | Practice demonstrating all 4 years of the car. Cover the LDR → lights come on. Press horn → 2-second honk. Point to blinking roof light. |
| 32 | Mock Exhibition prep — Standalone | Practice explaining the logic lock. Demonstrate correct combo (green!) and wrong combo (red + buzz!). Explain what AND and NOT gates do. |
| 33 | Peer review session | Swap projects. Try to crack each other's combination lock! Can you figure out the secret code by testing all 8 combos? |
| 34 | Final fixes based on review | Tighten any loose IC connections. Ensure toggle switches are labeled. Re-test all functions. |
| 35 | Exhibition boards + component journey card | Create a visual showing every component learned from 1st–4th class. Circle which ones are in each project. |
| 36 | 🎉 Year-End Exhibition | Demo Smart RC Car (auto-lights + timed horn + blinking roof!) + Logic Gate Combination Lock (visitors try to crack the code). |

---

## 🔗 Chain Project Deep-Dive: RC Car with Smart Auto-Features

**What You Bring from 3rd Class:** RC Car with headlights (manual toggle), horn (buzzer button), and wired LED decorations.

**What You Add This Year:**
1. **Auto-Headlights** — LDR + BC547 transistor replaces manual switch. Dark → lights ON. Light → lights OFF. Just like real car headlights!
2. **Timed Horn** — Capacitor-based circuit. Press button → buzzer sounds for exactly ~2 seconds → stops automatically.
3. **555 Blink Light** — NE555 in astable mode → yellow LED on car roof blinks steadily. Looks like a work vehicle warning light!

**The Upgrade Story:** In 3rd class you manually switched headlights. In 4th class the car is SMARTER — it detects darkness and responds. No Arduino. No code. Just a transistor that responds to light resistance changes. This is the foundation of all automatic systems!

**Auto-Headlight Circuit:**
```
9V (+) ──→ 1kΩ Resistor ──→ Collector of BC547
                              Emitter → GND
LDR + 10kΩ resistor divider → Base of BC547
White LEDs (parallel) across Collector/Emitter output
```

**555 Astable (Blink) Circuit Configuration:**
- Resistors: R1 = 1kΩ, R2 = 47kΩ
- Capacitor: C = 10µF
- Note: Changing the capacitor to a larger value (like 47µF) makes it blink slower, while a smaller one makes it blink faster.

**Keep It:** The car now has 4 years of history. In 5th class the entire brain is replaced with an Arduino Uno — and suddenly it can be programmed to do all these things AND much more!

---

## 🚀 Standalone Problem-Solving Project: Logic Gate Combination Lock

**The Real-World Problem:** Physical key locks can be copied. PIN locks can be shoulder-surfed. A logic gate lock is harder to crack — you need to know WHICH switches to flip in the right pattern.

**Your Solution:** 3 toggle switches wired through AND and NOT gates. Only the exact combination (e.g., SW1=ON, SW2=OFF, SW3=ON) produces a HIGH output, which lights the green LED. Everything else lights red + buzzer.

**How It Works:**
- SW1 → directly to AND gate input A
- SW2 → through NOT gate (inverted) → AND gate input B  
- SW3 → directly to second AND gate input
- All AND gates chain together: only correct combo = HIGH output
- HIGH output → green LED (unlocked)
- Inverted output → red LED + buzzer (wrong combo)

**The Math:** With 3 switches, there are 2³ = 8 possible combinations. Only 1 is correct. That's a 12.5% chance of guessing — make it harder by adding a 4th switch!

**Components Needed:**

| Component | Role |
|-----------|------|
| Toggle switches × 3 | The "code" input |
| 7408 AND gate IC | Logic gate — requires both inputs HIGH |
| 7404 NOT gate IC | Inverts one switch signal |
| Red LED + 220Ω | Wrong combo indicator |
| Green LED + 220Ω | Correct combo indicator |
| Active buzzer | Wrong combo alarm |
| 9V battery + holder | Power source |
| Cardboard panel | Security panel housing |

**Secret Combination:** Choose your own! Just design the gate logic to match.

---

## Year-End Exhibition

Students demonstrate TWO projects:

1. **Smart RC Car** — Demo in a dimmed area. Headlights come on automatically. Press horn → 2-second honk. Point out the blinking yellow roof light. Walk visitors through the 4-year upgrade history!
2. **Logic Gate Combination Lock** — Invite visitors to "crack the code." Most fail (8 combinations). Then reveal the secret and show how the gates make it work.

**Connection:** Your car now responds to its environment without any programming. In 5th class, an Arduino Uno replaces the transistor logic and can do the SAME things — PLUS infrared sensors, PLUS display screens, PLUS internet connectivity in later years.

---

## Assessment

| Component | Weight | What's Evaluated |
|-----------|--------|-----------------|
| Session participation & challenges | 20% | Multimeter accuracy, gate truth tables, circuit debugging |
| Component identification quiz (Session 30) | 10% | Correctly identify and describe 10 components |
| Chain Project — Smart RC Car | 35% | Auto-lights work? Timed horn works? 555 blink works? 4-year journey explained? |
| Standalone Project — Logic Lock | 35% | Only correct combo unlocks? Truth table verified for all 8 combos? Gate logic explained clearly? |
