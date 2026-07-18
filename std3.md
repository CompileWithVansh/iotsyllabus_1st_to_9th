# 🔦 Standard 3 — Enhanced
## Theme: "Add Features, Add Power"
### 36 Sessions × 1 hr | 9 Months

---

## What You'll Build This Year

- **🔗 Chain Project:** Upgrade the 2nd class RC Car — Add LED headlights (parallel LEDs + switch) and a buzzer horn (separate button). Your car now has real headlights and honks!
- **🚀 Standalone Project:** Burglar Alarm System — slide switch hidden under a "door" + buzzer + LED flash (capacitor charge makes it flash). Trigger the trip wire and the alarm goes off!

---

## Component Inventory

| Category | Components |
|----------|-----------|
| From Last Year | Your RC Car (chassis + motors + L298N + 4 buttons) |
| Light | LEDs (white × 2 for headlights, red × 2 for alarm), 220Ω resistors × 4 |
| Sound | Active buzzers × 2 |
| Switches | Push button (for horn), slide switch (for alarm trip), toggle switch (for headlights) |
| New Components | Diodes (1N4007 × 4), capacitors (10µF × 2, 100µF × 1), resistors (1kΩ × 2, 10kΩ × 1) |
| Power | 9V batteries × 2, battery clips, breadboard |
| Wiring | Jumper wires, electrical tape |
| Craft | Small cardboard box (for alarm housing) |

---

## Session Plan

| Session | Topic | Activity |
|---------|-------|----------|
| 1 | Welcome back — drive your car! | Bring out the RC Car from 2nd class. Drive it around. Observe: "What does a real car have that ours is missing?" → Headlights! Horn! |
| 2 | Review: L298N, 4-button control | Quick rebuild challenge: from a jumbled set of components, reconstruct the basic RC car circuit diagram in 10 minutes. |
| 3 | Resistors deep dive — color code | Learn the 4-band color code. Decode 10 resistors. Race: who identifies values fastest? Write values on masking tape labels. |
| 4 | Resistors in practice — protecting LEDs | Why does an LED burn out without a resistor? Calculate: 9V supply, 2V LED forward voltage → R = (9-2)/0.02 = 350Ω. Use 220Ω or 470Ω. |
| 5 | Diodes — one-way current | Connect LED forward biased → glows. Reverse biased → dead. Why? Diode = one-way gate. Demo with 1N4007. |
| 6 | Diodes in practice — protecting circuits | Wire a motor in reverse without diode → spark risk. Add flyback diode across motor terminals → protected. Understand why motor drivers use diodes internally. |
| 7 | LED headlights circuit (standalone breadboard) | Wire 2 white LEDs in parallel + toggle switch + resistors. Both LEDs light together. This is the headlight circuit. |
| 8 | Mount headlights on car — front beam effect | Hot-glue white LEDs to front of car chassis. Wire back to switch on body. Switch ON → both headlights glow! Dim the room — the effect is real! |
| 9 | Buzzer horn circuit | Push button + buzzer. Press = honk. Wire on a separate breadboard first, then plan mounting on car. |
| 10 | Mount horn button on car | Add the horn push button to the car's control panel. Wire buzzer to car body. Press → BEEP! |
| 11 | **Chain Project Session 1** — Plan the upgrade | Sketch the full upgraded car diagram: existing F/B/L/R + new headlight switch + new horn button. Where does each new component mount? |
| 12 | **Chain Project Session 2** — Headlight integration | Integrate headlight circuit into the car. Route wires cleanly along chassis. Test: drive car AND turn on headlights simultaneously. |
| 13 | **Chain Project Session 3** — Horn integration | Add buzzer horn button to control panel. Test: drive + lights + horn all work independently. |
| 14 | **Chain Project Session 4** — Full test drive | Drive the fully upgraded car in a dark corner. Lights on, honking horn — it looks like a real RC car! |
| 15 | **Chain Project Session 5** — Polish + documentation | Tidy all wires with cable ties/tape. Draw complete circuit diagram of upgraded car with ALL new additions labeled. |
| 16 | **Chain Project Complete** — Photo + diagram card | Take a photo of the car. Attach a card listing: "1st class I added: ___ . 2nd class I added: ___ . 3rd class I added: ___ ." |
| 17 | Capacitors — what they store | A capacitor stores electrical charge like a tiny bucket. Demo: charge with 9V, disconnect, it powers an LED briefly! |
| 18 | Capacitor charge/discharge timing | Different capacitor values = different discharge times. Compare 10µF vs 100µF. Larger cap = longer LED glow after disconnect. |
| 19 | Capacitor flash circuit | Wire capacitor + LED + resistor. Charge → discharge repeatedly = LED flashes at a rate. Observe timing change with different cap values. |
| 20 | Capacitor delayed horn (bonus upgrade) | Integrate into car: press button → capacitor charges → buzzer sounds for ~2 seconds → stops automatically. The car has a timed horn! |
| 21 | Electromagnet — electricity creates magnetism | Wind copper wire tightly around a steel bolt, 50+ turns. Connect to 9V. It picks up paper clips! More turns = stronger magnet. |
| 22 | Electromagnet strength experiments | Variable: number of coil turns. Test: 20 turns vs 50 vs 100 turns. Count maximum paper clips lifted. Graph the results. |
| 23 | Electromagnet switch circuit | BC547 transistor drives the electromagnet coil (transistor = amplified switch). Small button signal → transistor → electromagnet activates. |
| 24 | **Standalone Project** — Burglar alarm concept | Real problem: how do you detect if a door or window is opened without looking? A trip-wire switch under the door frame! Plan the circuit. |
| 25 | Standalone — Trip wire switch design | Slide switch wired so door OPENING breaks the circuit (or completes it). Test the switching action with a cardboard "door". |
| 26 | Standalone — Alarm circuit wiring | Capacitor-charged LED flash + buzzer. When door opens → capacitor discharges → LED flashes rapidly + buzzer sounds. |
| 27 | Standalone — Mounting in housing | Build a small cardboard alarm box. Mount LED and buzzer inside. Route trip wire through a "door frame" piece. |
| 28 | Standalone — Testing the alarm | Set the alarm, open the door → it fires. Does the LED flash? Does buzzer sound? Adjust capacitor value to change flash speed. |
| 29 | Standalone — Reset mechanism | Add a reset button that stops the alarm. Now it behaves like a real burglar alarm system (alarm → person hears it → presses reset). |
| 30 | Combined skills project challenge | Mini-challenge: build a circuit using resistor + diode + capacitor + LED that shows all three new components working together. |
| 31 | Mock Exhibition prep — Chain Project | Practice 90-second explanation of the car's journey: Bug (1st) → RC Car (2nd) → Enhanced RC Car (3rd). Show each upgrade. |
| 32 | Mock Exhibition prep — Standalone | Practice explaining the burglar alarm: what problem does it solve? How does the capacitor make the LED flash? |
| 33 | Peer review — test each other's systems | Drive a classmate's car. Trigger a classmate's burglar alarm. Give feedback: 1 thing works great, 1 thing to improve. |
| 34 | Final fixes based on peer feedback | Implement at least ONE improvement from peer review. Document what was changed and why. |
| 35 | Exhibition boards + labels | Create a title card for each project. Include: problem statement, components used, how it works (3 sentences max). |
| 36 | 🎉 Year-End Exhibition | Demo Enhanced RC Car (lights + horn) + Burglar Alarm (trip the wire!). Visitors test both. |

---

## 🔗 Chain Project Deep-Dive: RC Car with Headlights + Horn

**What You Bring from 2nd Class:** The RC Car with L298N + 4 push buttons. It drives all 4 directions.

**What You Add This Year:**
- 2 white LEDs (in parallel) + toggle switch = headlights
- Active buzzer + push button = horn (BEEP!)
- Bonus: capacitor-timed horn (honks then auto-stops)
- Diodes added to protect motor circuits from back-EMF

**The Upgrade Story:** In 2nd class the car drove but had no features. Real vehicles have lights and horns because driving in the dark is dangerous and communication matters. Now your car has both. Press the light switch in a dimmed room and the headlights actually illuminate the path ahead!

**Headlight Circuit:**
```
9V (+) → Toggle Switch → Resistor (220Ω) → LED 1 →┐
                                                     ├→ GND (-)
                                         LED 2 ───────┘
(Parallel connection: both LEDs share same resistor)
```

**Horn Circuit:**
```
9V (+) → Push Button → Buzzer (+) → GND (-)
(Active buzzer, simple series circuit)
```

**Timed Horn (Bonus):**
```
9V (+) → Push Button → 100µF Capacitor → Buzzer (+) → GND (-)
(Capacitor charges on button press, discharges through buzzer for ~2 seconds)
```

**Keep It:** Store the car with all upgrades intact. In 4th class you'll add a transistor-based automatic headlight and logic gate components!

---

## 🚀 Standalone Problem-Solving Project: Burglar Alarm System

**The Real-World Problem:** Intruders count on silence and surprise. A burglar alarm removes their advantage — the moment a door or window opens, it screams.

**Your Solution:** A physical trip-wire alarm. A slide switch hidden under a door frame completes (or breaks) a circuit when the door opens, triggering a capacitor-flash LED and a buzzer alarm.

**How It Works:**
1. Slide switch under door frame → door closed = switch OFF → no alarm
2. Door opens → switch flips ON → capacitor discharges → LED flashes + buzzer sounds
3. Reset button stops the alarm (press to acknowledge)

**Components Needed:**

| Component | Role |
|-----------|------|
| Slide switch | Trip wire — hides under door frame |
| Active buzzer | Alarm sound |
| Red LED | Flashing visual alert |
| 220Ω resistor | Protects LED |
| 100µF capacitor | Creates flash timing (charge/discharge) |
| 9V battery + holder | Power source |
| Push button | Reset (stop alarm) |
| Cardboard box | Alarm housing |

**Build Plan:**
1. Wire: 9V → slide switch → capacitor → LED (with resistor) → GND
2. Also wire: 9V → slide switch → buzzer → GND (in parallel with LED circuit)
3. Place switch under "door frame" cardboard
4. Test: open door → alarm fires. Close + reset button → alarm stops.
5. Extension: Add a second trip switch for a "window" sensor. Now it's a multi-zone alarm!

---

## Year-End Exhibition

Students demonstrate TWO projects:

1. **Enhanced RC Car** — Drive it! Lights on, horn honking. Explain the headlight parallel circuit and diode protection. Show the upgrade progression from 1st class to today.
2. **Burglar Alarm** — Invite a visitor to "open the door." The alarm fires. Explain how the capacitor creates the flash. Show the reset function.

**Connection:** Your car now drives, lights up, and honks. In 4th class you'll add transistors so the headlights turn on AUTOMATICALLY when it gets dark — no switch needed. Real smart headlights!

---

## Assessment

| Component | Weight | What's Evaluated |
|-----------|--------|-----------------|
| Session participation & challenges | 20% | Completing challenges, component identification accuracy |
| Circuit diagram — Enhanced Car (Session 15) | 10% | Complete labeled diagram with all upgrades |
| Chain Project — Enhanced RC Car | 35% | Lights + horn functional? Can student explain each addition? Upgrade progression articulated? |
| Standalone Project — Burglar Alarm | 35% | Trip switch works? LED flashes? Buzzer sounds? Reset works? Real-world connection explained? |
