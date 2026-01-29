# Smart Home Automation System (AVR Microcontroller)

This project is a **Master-Slave** embedded system for smart home control using AVR microcontrollers (likely ATmega family) programmed with **CodeVisionAVR**.

- **Master MCU** → manages LCD display, keypad input, menu system, SPI communication  
- **Slave MCU** → handles sensors (ADC), LEDs, timers, actuators via SPI

## Project Features
- Keypad for user input
- LCD for displaying status and menu
- LED control
- ADC sensor reading
- Timer-based operations
- SPI communication between Master and Slave
- EEPROM usage (on master)

## Folder Structure
smart-home-system/
├── docs/
│   └── proteus/                → Proteus simulation files (.pdsprj, backups, etc.)
├── firmware/
│   ├── master/
│   │   ├── src/                → .c source files
│   │   ├── inc/                → .h header files
│   │   └── Master code.cproj   → CodeVisionAVR project file for master
│   └── slave/
│       ├── src/                → .c source files
│       ├── inc/                → .h header files
│       └── Slave code.cproj    → CodeVisionAVR project file for slave
├── .gitignore
└── README.md
text## Tools Used
- **CodeVisionAVR** (IDE + compiler for AVR)
- **Proteus** (circuit simulation & debugging)

## How to Open & Build
1. Install **CodeVisionAVR**
2. Open the master project:  
   `firmware/master/Master code.cproj` (or similar name)
3. Open the slave project:  
   `firmware/slave/Slave code.cproj`
4. Build each project separately → it will generate `.hex` files
5. Flash the `.hex` files to your AVR chips using your programmer
6. For simulation: open the Proteus file in `docs/proteus/`

## Hardware Requirements (typical setup)
- 2× AVR microcontrollers (e.g. ATmega16, ATmega32, ATmega328...)
- LCD (16×2 or similar)
- 4×4 Keypad
- LEDs
- ADC sensors (temperature, light, etc.)
- SPI connection between Master & Slave

## Future Improvements (ideas)
- Add UART for debugging
- Implement password protection on keypad
- Add more sensors / relays
- Improve menu system
- Power saving modes

