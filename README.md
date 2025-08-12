# Automatic Pet Feeder using Arduino

[![Arduino](https://img.shields.io/badge/Arduino-Uno-blue?style=for-the-badge)](https://circuitdigest.com/microcontroller-projects/automatic-pet-feeder-using-arduino) [![Language](https://img.shields.io/badge/Language-EmbeddedC-orange?style=for-the-badge)]() [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

This project demonstrates how to build an **Arduino-based Automatic Pet Feeder** that can serve food to your pet at preset times using a **DS3231 RTC module** for accurate scheduling. It uses a **servo motor** to dispense food, a **4×4 matrix keypad** for setting feeding time, and a **16×2 LCD** to display the date and time. The device automatically dispenses the correct amount of food based on the set schedule, making it ideal for small to medium-sized pets.

![Automatic Pet Feeder Circuit](https://circuitdigest.com/sites/default/files/circuitdiagram_mic/Automatic-Pet-Feeder-circuit-diagram-using-Arduino.png)

---

## 🚀 Features

- Automatic feeding schedule using **DS3231 Real-Time Clock Module**
- 4×4 matrix keypad for manually setting feeding time
- Servo motor control for precise portion dispensing
- LCD display for current date and time
- 3D-printable feeder container with servo-driven gate
- Backup battery in RTC ensures timekeeping during power outages

---

## 🛠️ Hardware Requirements

| Component            | Description                                        |
|----------------------|----------------------------------------------------|
| Arduino UNO          | Main microcontroller                               |
| DS3231 RTC Module    | Real-time clock for precise scheduling             |
| 4×4 Matrix Keypad    | For entering feeding time                          |
| 16×2 LCD              | To display date and time                           |
| Push Button          | To initiate feeding time setup                     |
| Servo Motor          | To control container gate opening                  |
| Resistors            | For pull-up/pull-down as required                  |
| Connecting Wires     | For circuit connections                            |
| Breadboard           | For prototyping                                    |

---

## ⚙️ How It Works

1. **Timekeeping**: DS3231 RTC maintains accurate time even without power.
2. **User Input**: Feeding time is entered via the 4×4 matrix keypad and stored in memory.
3. **Display**: The 16×2 LCD shows the current time and date in real-time.
4. **Dispensing**: When the current time matches the feeding schedule, the servo motor rotates from its initial position (55°) to 100°, opening the container gate for food to drop into the bowl, then returns to its initial position after 0.4 seconds.

---

## 🔌 Circuit Connection

- **RTC Module**: SDA → A5, SCL → A4 on Arduino UNO
- **Keypad**: Connected to digital pins 2–9
- **LCD**: RS → A0, Enable → A1, D4–D7 → A2, 11, 12, 13
- **Servo Motor**: Signal pin → D10
- **Push Button**: One side → A3, other side → GND (with pull-up configuration)

---

## 🖨️ 3D-Printed Container

The feeder container is a **four-part PLA 3D-printed assembly** with a servo mount.  
Download STL files from [Thingiverse](https://www.thingiverse.com/thing:2847872).

![3D-printed Pet Feeder Parts](https://circuitdigest.com/sites/default/files/inlineimages/u/3D-printed-Pet%20-Feeder-model-Parts.jpg)  
![Assembled Pet Feeder](https://circuitdigest.com/sites/default/files/inlineimages/u/3D-printed-Pet%20-Feeder-model.jpg)

---

## 🧠 Troubleshooting

| Issue                               | Cause / Solution                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Servo not rotating                  | Check pin 10 connections, power supply, and angle values in code                 |
| LCD not displaying                  | Check RS/Enable/D4-D7 connections and contrast adjustment                        |
| Time not updating                   | Ensure RTC is initialized and battery is installed                               |
| Incorrect feeding schedule          | Verify keypad wiring and input sequence                                          |
| Over/under portion dispensing       | Adjust servo angle range and delay duration                                      |

---

## 📱 Applications

- Feeding small to medium pets (cats, small dogs, birds)
- Maintaining consistent feeding schedules during owner absence
- Customizable portion control for dietary needs

---

## 🔮 Future Enhancements

- Wi-Fi or Bluetooth integration for remote feeding control
- Mobile app interface for schedule setup
- Multiple feeding schedules per day
- Weight sensor for portion measurement
- Voice alerts for pets

---

## 🧪 Technical Specifications

| Parameter             | Value                                          |
|-----------------------|------------------------------------------------|
| MCU                   | Arduino UNO                                    |
| RTC Module            | DS3231 (±2ppm accuracy)                        |
| Display               | 16×2 LCD                                       |
| Keypad                | 4×4 matrix keypad                              |
| Motor Type            | SG90 / similar servo motor                     |
| Servo Angles          | Default: 55° (closed), Feeding: 100° (open)    |
| Supply Voltage        | 5V DC                                          |
| Container Material    | PLA (3D printed)                               |
| Feeding Accuracy      | ±1 second (RTC dependent)                      |

---

## 🔗 Links

- 📖 [Complete Tutorial on Circuit Digest](https://circuitdigest.com/microcontroller-projects/automatic-pet-feeder-using-arduino)
- 🖨️ [3D Model STL Files](https://www.thingiverse.com/thing:2847872)
- 📚 [DS3231 RTC Module Library](http://www.rinkydinkelectronics.com/library.php?id=73)
- ⌨️ [4×4 Matrix Keypad Library](https://www.arduinolibraries.info/libraries/keypad)
- 🧠 [More Arduino Projects](https://circuitdigest.com/microcontroller-projects)

---

## ⭐ Support

If you found this helpful, please ⭐ star this repository and share it with others!

---

**Built with 💡 by [Circuit Digest](https://circuitdigest.com/)**  
_Making Electronics Simple_

---

### 🔖 Keywords

`Arduino pet feeder` `DS3231 RTC` `automatic feeding system` `servo motor dispensing`  
`4x4 keypad input` `16x2 LCD interface` `3D printed feeder` `embedded C Arduino project`  
`animal care automation` `IoT pet feeder`
