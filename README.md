# PET-BOT


### The Problem statement
In today's fast-paced world, stress and boredom are common across all age groups. Traditional toys lack engagement, creating a need for smart, interactive toys that can entertain and connect with users.

### The problem Solution
To address these challenges, we introduce a smart pet bot designed to provide engaging entertainment and emotional companionship during stressful routines. The pet bot offers interactive behaviour and expressive responses, making it suitable for both children and adults as a stress-relieving and enjoyable companion.

### project objectives
1. To design and develop a microcontroller-based interactive pet bot for entertainment and stress relief.
2. To ensure a simple, user-friendly system suitable for all age groups,which can be controlled via a simple mobile application.
3. To simulate pet-like behaviour that creates a sense of companionship and reduces stress.

---

## Technical Details

### Technologies/Components Used

**For Software:**
- Languages used: C++
- Frameworks used: ARDUINO IDE
- Libraries used:
  1. BluetoothSerial.h - Used for Bluetooth communication
  2. Wire.h - Used for I2C communication(Required for devices like OLED display)
  3. Adafruit_GFX.h - Core graphics library(Provides functions like: Draw text, Draw shapes (lines, circles, etc.))
  4. Adafruit_SSD1306.h - Specifically for SSD1306 OLED display.Works along with Adafruit_GFX
- Tools used: Arduino serial monitor
### simulation software used: wokwi
#### link
https://wokwi.com/projects/459177680688141313

**For Hardware:**
1. ESP 32 - Brain of the system
2. DC Motor - Robot wheel movementS.
3. Motor Driver(L293D) - Act as an interface between the ESP32 and the DC motor.
4. Lithium-ion battery - Provides power to the system.
5. Charging module(TP4056) - To charge the battery.
6. Buck converter - To reduce the DC voltage
7. Wheels + Chassis - Mechanical body of the robot.
8. Connecting wires - For electrical connections.

---

## Features

## Key features of our project:
🔹 State Machine 
The bot uses an “Emotion State” variable 
Each command changes the state 
Based on the state → different action is executed 
🔹 Motor Control Logic 
Each motor has 2 pins: 
HIGH/LOW combinations decide direction 
Example: 
HIGH + LOW → Forward 
LOW + HIGH → Backward 
🔹 PWM Speed Control 
Speed is controlled using PWM (Pulse Width Modulation) 
Value range: 0–255 
Higher value → faster motor 
🔹 Animation System 
Uses timing (millis) for: 
Eye blinking 
Eye movement 
Makes display look dynamic 
🔹 Full System Working Flow 
Plain text 
Copy code 
Mobile App → Bluetooth → ESP32 → Decision Making→ Motor Driver 
→Motors → Movement→ OLED Display → Emotions

---

# Implementation

### For Software:

#### Installation
 No external package installation required (except standard libraries)
1. Download and install Arduino IDE from arduino.cc
2. Open Arduino IDE
3. Install required libraries via Library Manager:
  - Adafruit GFX
  - Adafruit SSD1306
4. Select Board Manager → Install ESP32 Board Package
5. Paste the project code into the Sketch Editor
#### Run
1. Connect ESP32 board via USB
2. Select Board → ESP32 Dev Module and select the correct COM Port
3. Click Upload (Ctrl + U)
4. Open Serial Monitor (Ctrl + Shift + M). (optional for debugging)
  - Turn ON Bluetooth on your phone
5. Connect to ESP32 Bluetooth device
6.Open mobile app (MIT App Inventor app)
Send commands:
    1 → Forward
    2 → Backward
    3 → Left
    4 → Right
    0 → Stop
    5–9 → Emotions

---

### For Hardware:
## Circuit setup
1. Connect ESP32 to L293D motor driver
2. Connect DC motors to motor driver outputs
3. Connect OLED display (SSD1306) using I2C:
    SDA → GPIO 21
    SCL → GPIO 22
4. Connect battery (7.4V):
5. Direct to motor driver
6. Through buck converter → 5V to ESP32
7. Ensure common ground for all components
**Final Assembly:**
<img width="1599" height="899" alt="image" src="https://github.com/user-attachments/assets/0950a77f-93b5-49ac-bdb1-d24317a9938d" />

--- 

## Project Documentation

### For Software:

#### Screenshots 
**ARDUINO IDE: code running and output on serial monitor**
https://drive.google.com/file/d/1CYCUl89IZzrr62z-IsjdJ3Kmwlyig97-/view?usp=drivesdk

#### Diagrams

**System Architecture:**
<img width="1041" height="919" alt="system arch" src="https://github.com/user-attachments/assets/ab611547-f067-4f2f-b04e-e583728db525" />


