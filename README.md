# RFID-Based Access Control System

## Overview
This project is an RFID-based access control system using an Arduino, an MFRC522 RFID module, a servo motor, LEDs, and a buzzer. The system grants or denies access based on the unique ID (UID) of an RFID card.

## Features
- Reads RFID card/tag UID using the MFRC522 module.
- Compares UID with a predefined authorized UID.
- Grants access by activating a green LED, sounding a buzzer, and rotating a servo motor.
- Denies access by activating a red LED and sounding a buzzer.

## Components Required
- Arduino board (e.g., Uno, Mega, Nano)
- MFRC522 RFID module
- Servo motor
- LEDs (Green & Red)
- Buzzer
- Jumper wires
- 3.3V & 5V power source

## Wiring Diagram
```plaintext
| Component  | Arduino Pin |
|------------|------------|
| MFRC522 SS | 10         |
| MFRC522 RST| 9          |
| MFRC522 SDA| 10         |
| MFRC522 SCK| 13         |
| MFRC522 MOSI| 11        |
| MFRC522 MISO| 12        |
| Servo Motor| 3          |
| Green LED  | 4          |
| Red LED    | 5          |
| Buzzer     | 2          |
```

## Installation and Setup
1. Connect the components as per the wiring diagram.
2. Install the required Arduino libraries:
   - `SPI.h`
   - `MFRC522.h`
   - `Servo.h`
3. Upload the provided Arduino code to your board.
4. Modify the UID in the code to match your authorized RFID card.
5. Open the Serial Monitor (9600 baud) to check UID readings.
6. Place an RFID card near the reader to test access.

## Usage
- **Authorized card detected:**
  - Green LED lights up.
  - Buzzer sounds briefly.
  - Servo motor rotates, granting access.
  - After 5 seconds, the servo resets to its original position.
- **Unauthorized card detected:**
  - Red LED lights up.
  - Buzzer produces a different tone.
  - Access is denied.

## Future Enhancements
- Store multiple UIDs for multi-user access.
- Implement EEPROM storage for saved UIDs.
- Use WiFi or Bluetooth for remote access control.
- Log access attempts to an SD card or cloud database.

## License
This project is open-source and free to use. Feel free to modify and improve it as needed!

## Author
[Your Name]

