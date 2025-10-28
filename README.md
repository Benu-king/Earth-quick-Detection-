Earthquake Detection Simulation

Powered by Benyas Wondwosen

This project simulates an earthquake detection system using Python (Pygame) and optionally an Arduino device with a vibration sensor. It features animated characters, visual earthquake effects, and an alert sound.

Features

Real-time vibration detection via Arduino serial input.

Animated human character reacts to detected vibrations.

Ground shaking and cracking visual effects.

Particle effects for dust and debris.

Alert sound playback when vibration is detected.

Keyboard controls for testing without Arduino.

Requirements

Python 3.11+

Pygame (pip install pygame)

PySerial (pip install pyserial)

Pillow (pip install pillow) – optional, for handling GIFs or sprite sheets.

Arduino (optional) with vibration sensor connected to COM3 at 9600 baud.

Installation

Clone or download the repository.

Place quq.mp3 in the same directory as the script (this is the alert sound).

Ensure assets folder exists if you plan to add sprite images.

Connect your Arduino to COM3 or change the port in the script.

Usage

Run the main Python script:

python BenuEarthquake_Detection.py

Controls

S key – Manually trigger vibration (simulates earthquake).

G key – Stop vibration simulation.

ESC – Exit the application.

Arduino Input

Send 'S' from Arduino → Triggers vibration.

Send 'G' from Arduino → Stops vibration.

How It Works

PhysicalPerson class – Animates a humanoid character that walks and reacts to vibrations.

Emitter class – Generates particle effects for dust/debris when vibration occurs.

Visual Effects – Ground cracks and shakes when vibration is active.

Audio Alert – Plays a sound when vibration is detected.

Serial Communication – Reads data from Arduino to trigger or stop vibration effects.

Project Structure
project/
│
├── BenuEarthquake_Detection.py  # Main Python script
├── quq.mp3                      # Alert sound
├── assets/                      # Folder for sprites/images (optional)
└── README.md

Notes

If no Arduino is connected, you can still test the system using the S and G keys.

Make sure the alert sound file quq.mp3 exists in the same directory, or the alert will not play.

The system uses Pygame’s clock to update frames and particle effects in real time.

Author

Benyas Wondwosen – Ethiopian student & developer.
License

This project is free to use and modify for educational purposes.
