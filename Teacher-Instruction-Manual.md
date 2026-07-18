# 📘 Teacher's Playbook: Robotics & AI Curriculum
## Standards 1–9 Classroom Guide

This playbook is a plug-and-play manual designed for school tinkering teachers. It provides storytelling hooks, simplified vocabulary, visual wiring hacks, and debugging guides for each standard. Use this to run engaging, hands-on classes even if you do not have a strong background in electronics or programming.

---

# ⚡ Standard 1 — Spark Playbook
### Theme: "A Robot's Body — Electricity Wakes It Up"

#### 1. The Big Hook (1-Minute Story)
> *"Imagine a tiny robotic beetle lying completely still. It cannot move, light up, or make sound. It is sleeping. How do we wake it up? We feed it a magical fluid called electricity! But electricity is picky: it only flows if we build a complete circle pathway for it. Today, we are going to build that path and wake up our first robot body!"*

#### 2. Do's & Don't of Vocabulary
* ❌ **Do NOT Say:** Voltage, Current, Charges, Resistor calculations.
* 🟢 **DO Say:**
  * **Electricity:** Like water flowing through pipes.
  * **Circuit:** A continuous loop path. If there's a gap (open circuit), electricity stops.
  * **Battery:** The pump that pushes the electricity.
  * **Resistor:** A speed breaker that slows down the rush of electricity so components don't burn out.

#### 3. Visual & Sticker Wiring Hacks
* **LED Orientation:** Teach kids that LEDs are like one-way streets. The **Long Leg** is the positive entrance (connect to red wire), and the **Short Leg** is the exit (connect to black wire).
* **The Path Arrow:** Have students draw arrows on their breadboards showing the direction electricity flows (Battery Positive ➔ Resistor ➔ LED Long Leg ➔ LED Short Leg ➔ Battery Negative).

#### 4. Troubleshooting Cheatsheet
* **The LED doesn't glow:** Check if the LED is plugged in backward (check the long leg). Make sure all metal legs are pushed firmly into the breadboard holes.
* **The battery/wires feel hot:** **Short circuit!** Immediately disconnect the battery. This means positive and negative wires are touching directly without going through a component.
* **The bug doesn't crawl:** The motor shaft needs a visible wobbly weight (hot glue lump) on its tip. If it's too balanced, it won't vibrate. Make sure legs are bent slightly forward to catch the vibrations.

---

# 🚗 Standard 2 — Motion Playbook
### Theme: "A Robot's Muscles — Machines That Move"

#### 1. The Big Hook (1-Minute Story)
> *"Our bug crawls, but it just wanders around randomly. It has no steering muscles! Today, we are upgrading our bug into an RC Car. We are giving it two motors (left and right legs) and a helper chip called a 'muscle driver'. By opening and closing different gates on this chip with physical buttons, we will command our robot to go Forward, Backward, Left, and Right!"*

#### 2. Do's & Don'ts of Vocabulary
* ❌ **Do NOT Say:** IN1/IN2/IN3/IN4 control logic, HIGH/LOW states, H-bridge switches.
* 🟢 **DO Say:**
  * **L298N Motor Driver:** The "Muscle Helper" that sends battery power to the wheels when we open the gates.
  * **Gates (IN1 to IN4):** ON and OFF switches. When a gate is ON, power flows through a motor direction.
  * **Motor A & B:** Left Muscle and Right Muscle.

#### 3. Visual & Sticker Wiring Hacks
* **Color Sticker Gates:**
  * Place a **Green Sticker** on the driver's gate pin `IN1` (Left Wheel Forward) and a **Yellow Sticker** on `IN2` (Left Wheel Backward).
  * Place a **Blue Sticker** on `IN3` (Right Wheel Forward) and a **Red Sticker** on `IN4` (Right Wheel Backward).
  * Label the 4 buttons on the breadboard with matching stickers: Green/Blue together for Forward, Yellow/Red for Backward.

#### 4. Troubleshooting Cheatsheet
* **The car drives in circles:** One motor is wired backward. Swap the two wires plugged into the green terminal block of that motor.
* **Buttons don't do anything:** Ensure you have a **Common Ground**. Connect the battery's negative (-) terminal to the L298N board's `GND` terminal AND to the breadboard ground rail. Without this shared reference, the gates won't hear the buttons!
* **Motors click but don't spin:** The battery is weak. Motors require high current (power). Replace the 9V battery or use fresh AA batteries.

---

# 🔦 Standard 3 — Enhanced Playbook
### Theme: "A Robot's Features — Add Features, Add Power"

#### 1. The Big Hook (1-Minute Story)
> *"Real cars have horns to honk and headlights to see in the dark. Our robot has muscles, but it is deaf, mute, and blind. Today, we are adding headlights and a horn! We will also learn how a robot can 'store' energy in a tiny bucket called a capacitor, so that when we press the horn button once, it continues honking for a few seconds even after we let go!"*

#### 2. Do's & Don'ts of Vocabulary
* ❌ **Do NOT Say:** Ohm's Law math, microfarads capacitance equations, diode semiconductor junction theory.
* 🟢 **DO Say:**
  * **Capacitor:** A temporary water bucket for electricity. It takes time to fill up and time to pour out.
  * **Diode:** A one-way check valve. It lets electricity pass forward but blocks it from rushing backward.

#### 3. Visual & Sticker Wiring Hacks
* **Capacitor Stripe:** The capacitor has a grey stripe with minus (-) symbols on it. This leg *must* connect to the negative (GND) side of the circuit.
* **Diode Ring:** Diodes have a small silver ring at one end. This ring is the "gate block". Tell kids: "The arrow points towards the ring; electricity cannot go the other way."

#### 4. Troubleshooting Cheatsheet
* **The horn doesn't stay on (capacitor delay fails):** Ensure the capacitor is wired in series with the buzzer, and check its orientation. If it is backward, it will leak or not store charge correctly.
* **Headlights are dim:** If you wire them in series, they share the voltage and glow dimly. Ensure they are wired in **parallel** (both positive legs connected together, both negative legs together).
* **The diode blocks all power:** Check if the diode is flipped. If the silver ring is facing the incoming power source, it is blocking the path. Flip it around.

---

# 🔬 Standard 4 — Reflexes Playbook
### Theme: "A Robot's Reflexes — Understanding the Parts"

#### 1. The Big Hook (1-Minute Story)
> *"If you touch a hot plate, your hand pulls back instantly before your brain even thinks. That is a reflex. Robots have reflexes too, built out of smart transistors and logic gates. Today, we will build a streetlight reflex: when the sun goes down, our robot's headlights turn ON instantly, without any computer programming!"*

#### 2. Do's & Don'ts of Vocabulary
* ❌ **Do NOT Say:** NPN/PNP switching math, Boolean algebra, monostable/astable frequency formulas.
* 🟢 **DO Say:**
  * **Transistor (BC547):** An electronic faucet. A tiny touch of water (signal) on the handle (Base) opens a massive flow from the inlet (Collector) to the outlet (Emitter).
  * **AND gate:** "Both inputs must say YES."
  * **OR gate:** "Either input can say YES."
  * **NOT gate:** "The opposite/flip game."

#### 3. Visual & Sticker Wiring Hacks
* **IC Pin Counting Hook:** Logic gate chips look identical. Teach students the "U-notch rule". Point the notch to the left: Pin 1 starts at the bottom left, counts counter-clockwise around to Pin 14 (top left).
* Pin 14 is always the power entrance (5V) and Pin 7 is always the ground exit (GND). Use red/black stickers on these pins.

#### 4. Troubleshooting Cheatsheet
* **The logic gates aren't working:** Check if the chip is powered. Did you connect Pin 14 to (+) and Pin 7 to (-)? Without power, the chip is dead.
* **The chip is getting hot:** **Danger!** Turn off power immediately. An output pin is likely connected directly to power or ground, or the chip is plugged in backward.
* **The auto-light turns on in the light instead of dark:** The LDR sensor is on the wrong side of the divider. Swap the positions of the LDR and the fixed resistor to invert the trigger.

---

# 💻 Standard 5 — Brain Playbook
### Theme: "A Robot's Brain — Arduino Enters the Lab"

#### 1. The Big Hook (1-Minute Story)
> *"So far, we have built bodies, muscles, and reflexes. But our robot still cannot plan or think. Today, we are putting a computer brain on our robot: the Arduino Uno! Now, instead of moving wires, we write lines of code. We will program our robot to look out for walls and decide to stop itself before crashing!"*

#### 2. Do's & Don'ts of Vocabulary
* ❌ **Do NOT Say:** Registers, baud rate protocols, syntax compiler optimization.
* 🟢 **DO Say:**
  * **Arduino:** The robot's central brain.
  * **Setup:** The robot's morning routine (runs once).
  * **Loop:** The robot's daily heartbeat (runs over and over).
  * **Code Pin:** The brain's fingers. They can touch to feel (read) or push to control (write).

#### 3. Visual & Sticker Wiring Hacks
* **Pin Labels:** Arduino pins are tiny. Give students a printed pinout diagram. Use masking tape on the breadboard to write down what pin does what (e.g. "Pin 5 = IR Bumper", "Pin 9 = Left Motor").
* **USB Hookup Check:** Before plugging the Arduino into a laptop, check the pins to ensure no loose wires are shorting the board.

#### 4. Troubleshooting Cheatsheet
* **The code won't upload:**
  * Check the **Port** in Arduino IDE (Tools ➔ Port).
  * Unplug and re-plug the USB cable.
  * Make sure the correct board (Arduino Uno) is selected.
* **The robot doesn't stop for walls:** Open the Serial Monitor. Verify if the IR sensor reads `0` or `1` when your hand is close. If the reading doesn't change, adjust the small sensitivity screw on the IR module using a screwdriver.
* **Arduino turns off when motors start:** The motors are drawing too much current, causing the Arduino to reset. Make sure the L298N driver is powered by a separate 9V battery, and only connect the GNDs together.

---

# 🌡️ Standard 6 — Senses Playbook
### Theme: "A Robot's Senses — Every Sensor Has a Story"

#### 1. The Big Hook (1-Minute Story)
> *"How do you know where you are? You see, smell, and feel. A robot does the same! Today, we are adding new senses to our robot: ears that bounce sound waves to measure exact distance in centimeters, and noses that can smell dangerous gas. Our robot will display these readings on an LCD dashboard, just like a real dashboard!"*

#### 2. Do's & Don'ts of Vocabulary
* ❌ **Do NOT Say:** I2C address hex codes, acceleration vectors, ultrasonic sound speed velocity calculations.
* 🟢 **DO Say:**
  * **Ultrasonic Sensor (HC-SR04):** The robot's bat-ears. It sends a shout (Trigger) and listens for the echo (Echo) to measure distance.
  * **LCD Display:** The robot's dashboard.
  * **MPU-6050:** The robot's balance sensor (tells it if it's tipping over).

#### 3. Visual & Sticker Wiring Hacks
* **I2C Bus Simplicity:** LCD and Gyro share the same SDA (Data) and SCL (Clock) pins. Explain to kids: "SDA is the conversation wire, SCL is the timer wire. They can share the same line, just like passengers on a bus."
* Wire them to Arduino A4 (SDA) and A5 (SCL).

#### 4. Troubleshooting Cheatsheet
* **The LCD displays blank boxes:** Adjust the blue potentiometer on the back of the LCD I2C board with a screwdriver. This controls the display contrast. Turn it until the letters appear.
* **The distance sensor readings are stuck at 0 or 2000:** Verify the Trigger and Echo pins are not swapped in the code. Trigger goes to Pin 9, Echo to Pin 10.
* **Gas sensor gives high readings instantly:** The MQ-2 sensor has a heater inside. It requires 1–2 minutes to warm up when first plugged in before it gives accurate readings.

---

# 🤖 Standard 7 — Autonomy Playbook
### Theme: "A Robot's Autonomy — Robots That Think"

#### 1. The Big Hook (1-Minute Story)
> *"A remote-controlled car is not a robot because a human makes all the decisions. A true robot drives itself, scans its surroundings, and decides its own path. Today, we are swapping our Arduino Uno for a smaller Arduino Nano. We will mount our sensor eyes on a servo motor so the robot can look Left and Right, scan distances, and make its own decisions!"*

#### 2. Do's & Don'ts of Vocabulary
* ❌ **Do NOT Say:** Servomechanism PWM frequency, non-blocking interrupt routines, proportional control algorithms.
* 🟢 **DO Say:**
  * **Servo Motor:** A motor that can turn to an exact angle (0° to 180°).
  * **Autonomy Algorithm:** The decision-making rules: "Look Left, Look Right, go where the path is wider."

#### 3. Visual & Sticker Wiring Hacks
* **Servo Wires:** Servo wires are color-coded: Brown/Black is GND (-), Red is VCC (+), Yellow/Orange is Signal. Place a sticker key on the board to prevent kids from plugging them in backward.
* **Arduino Nano Breadboard Placement:** Ensure the Nano is plugged exactly down the center divider of the breadboard so the pins on either side don't short together.

#### 4. Troubleshooting Cheatsheet
* **The servo sweeps, but the distance readings are incorrect:** The wires connecting the HC-SR04 sensor are twisting and pulling loose during the sweep. Ensure you use flexible jumper wires with enough slack.
* **The robot resets when the servo moves:** Servos draw a lot of power when they turn. Make sure the servo's power (+) is connected to a stable 5V source, and verify that the battery is fully charged.
* **The robot steers toward the blocked wall:** Check the logic check in the code. Ensure `if (distanceLeft > distanceRight)` turns left, not right!

---

# 📡 Standard 8 — Connections Playbook
### Theme: "A Robot's Voice & Connections — Everything Goes Wireless"

#### 1. The Big Hook (1-Minute Story)
> *"How do we talk to someone far away? We use a mobile phone or the internet. Today, our robot goes wireless! We will connect a Bluetooth module so we can steer it using our phones. Then, we will connect it to the school WiFi, allowing the robot to send its status dashboard straight to a cloud panel. You can watch your robot from anywhere in the world!"*

#### 2. Do's & Don'ts of Vocabulary
* ❌ **Do NOT Say:** Blynk exclusive methods, TCP/IP stack configuration, MQTT protocol.
* 🟢 **DO Say:**
  * **Bluetooth (HC-05):** A wireless serial wire.
  * **WiFi Module (NodeMCU):** The robot's internet connector.
  * **Cloud Dashboard:** The robot's remote dashboard website.

#### 3. Visual & Sticker Wiring Hacks
* **HC-05 Voltage Divider:** The HC-05 RX pin expects 3.3V, but Arduino Nano sends 5V. Use two resistors (1kΩ and 2kΩ) to build a "speed divider" so the signal is safe.
* Mark the RX pin on the HC-05 with a warning sticker.

#### 4. Troubleshooting Cheatsheet
* **Bluetooth won't pair with the phone:** Check the pairing code (usually `1234` or `0000`). Make sure the HC-05 module's red LED is blinking rapidly (indicates it is searching for a connection).
* **WiFi NodeMCU won't connect:** Check your SSID and Password in the code. Remember that most IoT modules only support 2.4GHz WiFi networks, not 5GHz.
* **Dashboard doesn't update:** Ensure the Blynk Auth Token in your code matches the token sent to your email or generated in your dashboard app. Close the Arduino Serial Monitor if you are trying to print debug info.

---

# 🧠 Standard 9 — Intelligence Playbook
### Theme: "A Robot's Mind — AI Meets Hardware"

#### 1. The Big Hook (1-Minute Story)
> *"This is the final stage. Your robot started 8 years ago as a simple bug that just vibrated. Today, we give it a Mind. We will show examples of hand gestures to a camera, train an AI model to recognize them, and send commands to our robot. You can steer your robot by simply waving your hand! No buttons, no apps — pure AI."*

#### 2. Do's & Don'ts of Vocabulary
* ❌ **Do NOT Say:** Neural network backpropagation, learning rate weights, loss functions.
* 🟢 **DO Say:**
  * **Training:** Showing the computer examples so it learns.
  * **Testing:** Checking if the AI can identify a new example correctly.
  * **Confidence Score:** How sure the AI is about its guess (0% to 100%).

#### 3. Visual & Sticker Wiring Hacks
* **Webcam Setup:** Mount the webcam on a stable stand facing the student. Clear the background area behind the student so the AI only looks at their hand gestures.
* **Serial Port Management:** Instruct students: "Only one software can talk to the ESP32 serial port at a time. Close the Arduino Serial Monitor before running the Python AI script."

#### 4. Troubleshooting Cheatsheet
* **AI makes wrong predictions:** Make sure you record at least 60+ samples for each class in the Teachable Machine, under similar lighting. If the background changes, retrain the model.
* **Python Serial communication error:** Verify the COM port number in your Python script matches the port of the ESP32 in the Arduino IDE.
* **Robot doesn't move when gesture changes:** Verify the ESP32 is receiving the character ('F', 'B', 'S') in its serial buffer. Connect a test LED to the ESP32 to blink when any serial data is received to isolate hardware vs code issues.
