# IoT & Applications — PEMRT525
## Lab Experiments | Batch MR 2K24 | S5 | JECC
### Department of Mechatronics Engineering | Jyothi Engineering College (Autonomous)

---

## Experiment 1 — ESP32 LED Blink

**Aim:** To write an Arduino program to blink an LED connected to ESP32 GPIO2 at 1 Hz frequency.

**Components Required:**

| Component | Quantity |
|-----------|----------|
| ESP32 Development Board | 1 |
| LED (Red / Green) | 1 |
| Resistor 220Ω | 1 |
| Breadboard | 1 |
| Jumper Wires | 3 |
| USB Cable | 1 |

**Circuit Connections:**

| ESP32 Pin | Component |
|-----------|-----------|
| GPIO2 | LED Anode (+) via 220Ω resistor |
| GND | LED Cathode (−) |

```
ESP32 GPIO2 ──── 220Ω ──── LED(+) ──── LED(−) ──── GND
```

**Code:**
```cpp
#define LED_PIN 2

void setup() {
  pinMode(LED_PIN, OUTPUT);
}

void loop() {
  digitalWrite(LED_PIN, HIGH);  // LED ON
  delay(500);                   // Wait 500 ms
  digitalWrite(LED_PIN, LOW);   // LED OFF
  delay(500);                   // Wait 500 ms
}
```

**Procedure:**
1. Connect the LED to GPIO2 of ESP32 through a 220Ω resistor as per the circuit diagram.
2. Connect the LED cathode to GND of the ESP32.
3. Open Arduino IDE. Select Board: **ESP32 Dev Module** and the correct COM port.
4. Enter the code and click **Upload**.
5. Once uploaded, observe the LED on the breadboard.

**Result:** The LED blinks continuously at 1 Hz (500 ms ON, 500 ms OFF), confirming successful GPIO digital output control on the ESP32.
<img width="1899" height="811" alt="image" src="https://github.com/user-attachments/assets/6bfd7753-edea-412b-844c-2a27b9409c30" />

**Result:** The LED blinks continuously at 1 Hz (500 ms ON, 500 ms OFF), confirming successful GPIO digital output control on the ESP32.

---
