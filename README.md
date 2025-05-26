🧊 PROXARC: The Proxmark + ESP32 Web Interface

Serious Tools for Wireless Signals — Built for the Field

🔧 What is PROXARC?

PROXARC (Proxmark + ESP32 Architecture) is a cutting-edge hybrid firmware and web interface project that elevates the legendary Iceman Proxmark3 fork by giving it wireless life through an ESP32-S3.

Hosted entirely on the ESP32-S3 via an OTG serial connection, it creates a mobile-first, touch-ready web interface to run commands, scan cards, and launch attacks — all from your phone or laptop. No drivers. No desktop GUI. No friction.

This is not a fork of Iceman. It's the next evolution in interfacing with it.

🧠 Vision

Enable zero-install, wireless command and control of the Proxmark3.

Deliver field-ready RFID/NFC tools that run on battery, hotspot, or USB.

Build a modular browser UI for rapid access to advanced capabilities.

🖥️ Interface Style & Feel

⚫️ Cyberpunk dark theme, bold contrast for field readability

📱 Responsive and mobile-first UI

🧩 Modular tool layout: Cards, Emulation, Dumps, Scripts, Console

📟 Real-time logs, terminal input, and visual feedback animations

🛠️ Architecture

1. ESP32-S3 Layer

Acts as USB OTG Host to the Proxmark

Async Web Server (ESPAsyncWebServer)

WebSocket + REST API for full command control

2. Proxmark3 (Iceman Fork)

Communicates via USB-UART from Proxmark to ESP32

Executes pm3 CLI commands via passthrough serial

3. Web Interface

Served directly from onboard ESP32 memory

HTML/JS/CSS (Vanilla or Alpine.js)

Auto-detect and handle Proxmark responses in-browser

🔥 Core Capabilities

Scan Tags (13.56 MHz / 125 kHz)

ISO14443A/B, HID, NFC Type 2

Display UID, ATQA, SAK, card type

Clone & Emulate

Dump tag data in binary, hex, TLV

Emulate Mifare Classic, HID, T5577

Attack Scripts

Run Iceman’s attack suites like static nonce and hardnested

Live Terminal

Send raw pm3 commands

Real-time command output & history

Local Storage

Save dumps, logs, and profiles to ESP32 flash

Export/download via browser

🧪 Use Cases

🔍 On-Site Red Teaming: Clone a badge in seconds, from your phone

🎓 Training & Demos: Show RFID/NFC live in class or workshops

🛠 DIY Projects: Build emulation rigs or test your access system

🧰 Portable Toolkit: Throw it in your bug-out bag with a battery

⚙️ Setup & Getting Started

Required Hardware

ESP32-S3 board w/ USB-OTG support

Proxmark3 Easy / RDV4

USB OTG adapter cable

Flash the Firmware

git clone https://github.com/youruser/proxarc
cd proxarc
idf.py set-target esp32s3
idf.py build flash monitor

Using It

Power the ESP32

Connect Proxmark3 to ESP32 via USB

Open browser to http://prox.local (or assigned IP)

Start scanning, emulating, or running pm3 commands

🚧 Roadmap

🪫 Battery support + OLED display for standalone mode

🔌 Plugin system for 3rd-party scripts/modules

📡 BLE/WebUSB for wireless console & updates

☁️ Sync system for backing up dumps to cloud

🔐 WebAuthn-based login + encrypted local flash storage

🤝 Contributing

This project is built by field operators for real-world use. If you know embedded, web UI, or RFID/NFC hacking, join us.

Fork it

Build it

Add modules or features

File issues with field feedback

All eyes, no ego.

📄 License

MIT License — build, improve, remix, and share.

🧠 Built for hackers. Powered by open tools.

🛰 PROXARC: Your Proxmark, Untethered.


