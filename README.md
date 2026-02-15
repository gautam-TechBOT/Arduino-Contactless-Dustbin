# Arduino Contactless Dustbin (Ultrasonic + Servo)

This project is a contactless smart dustbin that automatically opens and closes the lid using an ultrasonic sensor and a servo motor.

When a hand or object comes within a set distance, the lid opens automatically and closes after a delay — no touch required.

---

## 🔧 Hardware Used

- Arduino UNO / Nano
- HC-SR04 Ultrasonic Sensor
- Servo Motor (lid control)
- LED (status indicator – optional)
- Jumper Wires
- Dustbin with servo-mounted lid
- 5V Supply / Battery

---

## 📦 Required Library

- **Servo** (built-in Arduino library)

No external library required besides Servo.

---

## 🔌 Pin Connections (As per Code)

### 🎯 Ultrasonic Sensor (HC-SR04)

| Sensor Pin | Arduino Pin |
|-------------|-------------|
| TRIG | D5 |
| ECHO | D6 |
| VCC | 5V |
| GND | GND |

---

### 🎯 Servo Motor

| Servo Pin | Arduino Pin |
|------------|-------------|
| Signal | D7 |
| VCC | 5V |
| GND | GND |

---

### 💡 LED (Optional)

| LED | Arduino |
|------|----------|
| + | D10 |
| – | GND (via resistor) |

---

## ⚙️ Working Logic

- Ultrasonic sensor measures distance continuously
- 3 readings are averaged for stability
- If object detected within **50 cm**
  - Servo attaches
  - Lid opens
  - Waits for a few seconds
  - Lid closes
  - Servo detaches to reduce jitter

---

## ▶️ How to Run

1. Connect components as per wiring table
2. Upload the code to Arduino
3. Power the board
4. Move your hand near the sensor
5. Lid opens automatically

---

## 📏 Key Parameters (From Code)
Distance trigger = 50 cm
Open angle = 30°
Close angle = 180°
Open delay = 3 sec
Close delay = 1 sec


You can adjust these values as per lid design.

---

## 📷 Circuit Diagram

Circuit diagram image will be added soon. Pin wiring table is provided above.

---

## 🎥 Working Video

https://www.youtube.com/shorts/7VBMUI2QAqM

---

## ⚠️ Notes

- Mount ultrasonic sensor facing outward
- Fix servo firmly to lid hinge
- Use external 5V supply if servo is large
- Make sure servo GND and Arduino GND are common
- Adjust servo angles based on lid mechanics

---

## 👨‍💻 Author

Gautam — Robotics & Embedded Projects
