# 🚗 Standard 2 — Motion
## Theme: "Machines That Move"
### 36 Sessions × 1 hr | 9 Months

---

## What You'll Build This Year

- **🔗 Chain Project:** Upgrade your Vibrating Bug from 1st class → RC Car! Add an L298N motor driver + 4 push buttons + proper chassis. Now it drives: Forward, Backward, Left, Right — all with physical buttons. No code, no Arduino. Pure wiring logic.
- **🚀 Standalone Project:** Traffic Light System — 3 LEDs (Red, Yellow, Green) + toggle switch + manual timing. Build a working traffic signal!

---

## Component Inventory

| Category | Components |
|----------|-----------|
| Chassis & Motion | 2-wheel chassis kit, DC motors × 2, rubber wheels × 2, caster wheel × 1 |
| Motor Control | L298N motor driver module |
| Control | Push buttons × 4, toggle switch |
| Power | 9V battery × 2, 9V battery clips × 2, breadboard |
| Light | LEDs (red, yellow, green), 220Ω resistors × 3 |
| Wiring | Jumper wires, breadboard, electrical tape |
| From Last Year | Your Vibrating Bug (motor + decorated body) |

---

## Session Plan

| Session | Topic | Activity |
|---------|-------|----------|
| 1 | Welcome back — show your Bug! | Each student places their Vibrating Bug on the table and switches it on. Crawl race! Then the question: "What if we could STEER it?" |
| 2 | Review: circuits, switches, DC motors | Quick quiz. Rebuild a simple LED + switch circuit from memory. Refresh before we level up. |
| 3 | What is a motor driver? Why do we need it? | Problem: your fingers can't send clean F/B/L/R signals to two motors simultaneously. Solution: L298N. Intro to the chip. |
| 4 | L298N layout tour | Identify every pin: IN1, IN2, IN3, IN4, ENA, ENB, 12V, GND, 5V out. Fill in a printed blank pin diagram. |
| 5 | L298N logic table — how input pins control motor direction | IN1=HIGH, IN2=LOW → motor spins forward. IN1=LOW, IN2=HIGH → reverse. Both LOW → stop. Fill in truth table. |
| 6 | Wire ONE motor to L298N | Connect Motor A to L298N. Use jumper wires to manually pull IN1/IN2 HIGH/LOW. Watch motor respond! |
| 7 | Wire BOTH motors | Add Motor B. Now both motors can be controlled. Test: both forward, both backward, one each direction (= turn). |
| 8 | Introduce push buttons — review + new use | What happens when you wire a button directly to IN1? Press = HIGH signal! Test this concept. |
| 9 | Forward button circuit | Wire one button: press → IN1 HIGH, IN2 LOW → Motor A forward. Let go → motor stops. |
| 10 | Backward button circuit | Second button: IN1 LOW, IN2 HIGH → motor reverses. Now you have 2 buttons controlling 1 motor. |
| 11 | Left turn logic | For a left turn: right motor forward, left motor stopped (or reverse). Wire button 3 to create this. |
| 12 | Right turn logic | Mirror of left: left motor forward, right motor stopped. Wire button 4. |
| 13 | Full 4-button panel — breadboard layout | Lay out all 4 buttons neatly on breadboard. Label them F / B / L / R. Test each button individually. |
| 14 | Chassis kit — parts identification | Unbox chassis kit. Identify: base plate, motor mounts, wheels, caster. Assemble base plate with motors mounted. |
| 15 | Mount motors to chassis | Screw DC motors into motor mounts. Attach rubber wheels. Attach caster to front. It looks like a real car! |
| 16 | Connect L298N to chassis motors | Solder or crimp motor wires to L298N terminals. Secure L298N to chassis with double-sided tape. |
| 17 | Power wiring — 9V battery routing | Route 9V battery to L298N power input (12V in). Route L298N's 5V out to breadboard power rail. |
| 18 | Full system test — static (on blocks) | Lift car off table. Press each button. Wheels should spin correctly for F/B/L/R. Debug any reversed wires. |
| 19 | Floor test — does it drive? | Put car on floor. Press buttons. Does it go where expected? Fix any direction issues. |
| 20 | Steering calibration | Does "left" actually turn left? If not, swap motor wires. Drive in a square: F, R, F, R, F, R, F, R. |
| 21 | Button panel housing | Mount buttons on a flat piece of cardboard/foam as a "remote control pad". Label each button with direction arrows. |
| 22 | **Chain Project Session 1** — Upgrade plan | Take out your Vibrating Bug from 1st class. Decision: use bug's motor in new chassis OR mount bug decoration on new chassis? Plan it out. |
| 23 | **Chain Project Session 2** — Transfer motor from Bug | Remove motor from bug body. Test it still works. Mount in new chassis OR keep bug body as the "car body" with new wheels. |
| 24 | **Chain Project Session 3** — Full wiring integration | Complete the upgraded Bug → RC Car. All 4 buttons wired. Both motors connected. Battery secured. Full test. |
| 25 | **Chain Project Session 4** — Bug RC Car decoration | Keep the bug personality! Repaint the chassis to look like an upgraded robotic bug. Add antennae, LED eyes (optional). |
| 26 | **Chain Project Session 5** — Driving course | Set up a mini obstacle course. Drive the Bug RC Car through gates. Time each student. Fastest time wins! |
| 27 | **Chain Project Complete** — Labelled diagram | Draw a complete circuit diagram of the RC car. Label every component. Write one sentence about what each part does. |
| 28 | **Standalone Project** — Traffic light intro | What problem does a traffic light solve? Discussion. Then: what components would recreate it? Plan the circuit. |
| 29 | Standalone — Wire the traffic light | 3 LEDs (R/Y/G) + 3 resistors. Wire all three to a breadboard. Test each lights up separately. |
| 30 | Standalone — Toggle switch timing sequence | Use toggle switch to manually advance R → Y → G → back. Simulate a traffic light cycle. |
| 31 | Standalone — Mount in housing | Build a cardboard traffic light post. Mount LEDs at correct positions (red top, yellow middle, green bottom). |
| 32 | Standalone — Test + refinement | Does it look like a real traffic light? Fix LED spacing. Label the signal post. |
| 33 | Mock Exhibition prep | Practice 1-minute explanation for BOTH projects. Use your labelled diagrams as visual aids. |
| 34 | Peer review session | Swap seats. Drive your classmate's RC car. Test their traffic light. Give written feedback on one sticky note: "Works well:" and "Could improve:". |
| 35 | Final fixes + presentation boards | Fix any issues found in peer review. Prepare a small title card for each project: project name + problem it solves + how it works. |
| 36 | 🎉 Year-End Exhibition | Demo BOTH projects. Visitors drive the Bug RC Car and operate the traffic light. |

---

## 🔗 Chain Project Deep-Dive: Vibrating Bug → RC Car Upgrade

**What You Bring from 1st Class:** Your decorated Vibrating Bug — a DC motor with asymmetric weight and a decorated body. It crawled. Now we give it direction!

**What You Add This Year:**
- Proper 2-wheel chassis with caster
- Second DC motor (for steering)
- L298N motor driver (so you can control direction)
- 4 push buttons (Forward / Backward / Left / Right)
- 9V battery (more power for driving)

**The Upgrade Story:** In 1st class the motor just spun and the bug vibrated randomly. Now we control TWO motors with a driver chip. Press Forward → both motors spin forward. Press Left → right motor spins, left motor stops. The bug is no longer random — it obeys you!

**L298N Logic Reference:**

| Button | IN1 | IN2 | IN3 | IN4 | Result |
|--------|-----|-----|-----|-----|--------|
| Forward | HIGH | LOW | HIGH | LOW | Both motors forward |
| Backward | LOW | HIGH | LOW | HIGH | Both motors backward |
| Left | HIGH | LOW | LOW | LOW | Right motor only → turns left |
| Right | LOW | LOW | HIGH | LOW | Left motor only → turns right |
| None | LOW | LOW | LOW | LOW | Both motors stop |

**Keep It:** Put the RC Car away carefully. In 3rd class you'll add LED headlights and a buzzer horn!

---

## 🚀 Standalone Problem-Solving Project: Traffic Light System

**The Real-World Problem:** Intersections without traffic signals cause accidents. A properly sequenced Red-Yellow-Green signal tells drivers and pedestrians exactly what to do.

**Your Solution:** A working 3-LED traffic light with manual toggle control — showing the correct sequence and mounted in a realistic signal housing.

**How It Works:**
- Red LED on → Stop
- Yellow LED on → Get ready
- Green LED on → Go
- Toggle switch advances the sequence manually (simulates the timer inside a real signal controller)

**Components Needed:**

| Component | Role |
|-----------|------|
| Red LED | "Stop" signal |
| Yellow LED | "Caution / Get ready" signal |
| Green LED | "Go" signal |
| 220Ω resistors × 3 | Protect each LED |
| Toggle switch | Advance the sequence |
| 9V battery + holder | Power source |
| Cardboard post + housing | Realistic mounting |

**Build Plan:**
1. Wire 3 LEDs in parallel with individual switches (or toggle through them)
2. Mount in a tall cardboard post — red at top, yellow middle, green bottom
3. Add a control button on the base
4. Test: cycle through the sequence
5. Extension: Add a pedestrian "WALK" LED on the side!

---

## Year-End Exhibition

Students present TWO items:

1. **Bug RC Car (Chain Project)** — visitors get to drive it! Press the buttons, navigate the obstacle course. Explain: how does pressing a button make the motor spin forward vs backward?
2. **Traffic Light System (Standalone)** — demonstrate the signal sequence. Explain: why is red on top in real traffic lights? What problem does this solve?

**Connection:** The RC Car is the CHASSIS that will grow for the next 7 years. Today it runs on buttons. By 9th class it responds to hand gestures and connects to the internet. Every upgrade is built on what you built today.

---

## Assessment

| Component | Weight | What's Evaluated |
|-----------|--------|-----------------|
| Session participation & challenges | 20% | Completing mini-challenges, debugging effort |
| Circuit diagram — RC Car (Session 27) | 10% | Accuracy and completeness of labelled diagram |
| Chain Project — Bug RC Car | 35% | Does it drive all 4 directions? Can student explain L298N logic? |
| Standalone Project — Traffic Light | 35% | Does it cycle correctly? Can student explain the real-world problem solved? |
