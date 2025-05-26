𝙋𝙍𝙊𝙓𝘼𝙍𝘾: The Proxmark ESP32 Interface

Serious Tools for Wireless Signals

🔧 What is PROXARC?

PROXARC is a hybrid firmware + web-based interface that transforms the powerful Proxmark3 (Iceman fork) into a portable, wireless, ESP32-S3-driven tool — accessible via any browser.

This is not a replacement for Iceman. This is a bridge, a framework, and a way forward for RFID/NFC experimentation, red-teaming, and field ops without relying on clunky desktops or outdated GUI tools.

Using USB-OTG via UART and served from the ESP32 itself, PROXARC provides a slick, powerful web UI to command your Proxmark directly, no software install needed.

🧠 Project Vision

Empower hackers, researchers, and developers with zero-setup wireless control of their Proxmark3.

Remove friction from field work: scan, clone, emulate, and run scripts directly from your phone.

Elevate Proxmark's usability into a new era of modular, mobile-first tooling.

✒️ Interface Style & UX Philosophy

Dark cyberpunk aesthetic — designed for serious professionals.

Mobile-first layout with touch-friendly controls.

Live console, real-time logs, and animated feedback.

Module-based layout: Cards, Attack, Emulation, Dump Viewer, Scripts, OTA updates.

⚙️ Core Architecture

ESP32-S3 Layer

USB OTG Host mode to communicate with Proxmark via serial.

Async web server (ESPAsyncWebServer) serving a modern web UI.

REST and WebSocket interfaces for full duplex communication.

Proxmark3 (Iceman Fork)

Plugged into ESP32-S3 via micro USB (UART-based OTG).

Controlled via custom ESP32 shell wrappers for key Iceman CLI commands.

Web Interface

Hosted entirely on ESP32 flash memory.

Pure HTML/CSS/JS + lightweight framework (like Alpine.js or VanillaJS).

Terminal view for raw command input.

🔥 What Can It Do? (Initial Feature Set)

Card Scanning

ISO14443A/B, HID, 125kHz, 13.56MHz detection.

View UID, ATQA, SAK, and type instantly.

Cloning & Emulation

Dump tag memory in common formats (binary, hex, TLV).

Emulate Mifare Classic, NFC Type 2, HID, etc.

Attacks

Integrate with Iceman attack scripts: nested, static nonce, hardnested (beta).

Live Console

Type pm3 commands directly from browser.

Full console history + autocomplete.

Storage

Save dumps in internal flash or upload/export.

Manage tags, logs, and dumps via browser UI.

🔐 Use Cases

On-Site Physical Testing: Clone or sniff badges from a phone, no laptop.

Workshops & Demos: Show live attacks in training scenarios.

DIY Smartcard Projects: Build access control systems & clone test cards.

Pentesting Toolkit: Throw it in a bag, plug and play anywhere.

⚡ Getting Started

Hardware You Need:

ESP32-S3 dev board with USB-OTG support.

Proxmark3 (RDV4 or Proxmark3 Easy).

USB OTG cable (ESP32-S3 Host -> Proxmark Client).

Install:

git clone https://github.com/youruser/proxarc
cd proxarc
idf.py set-target esp32s3
idf.py build flash monitor

Usage:

Connect to ESP32 Wi-Fi AP or join your network.

Open browser to http://prox.local or IP.

Plug in Proxmark to ESP32 USB.

Run commands or use modules from UI.

🧪 Roadmap & Expansion Ideas

🔋 Battery-powered mobile version w/ OLED status screen

🧱 Plugin framework for attack modules (via JS + REST)

📶 BLE control via ESP32 BLE HID interface

🌐 Cloud dashboard to sync and backup tags

🔒 Authentication layer + encrypted local storage

🤝 Contributing

If you're serious about embedded RF tools, we want your help. Open issues, fork and PR, or hit us up with ideas. This is a tool built for the field, by those who actually use it.

📜 License

MIT License — use, remix, and make it yours.

Made by hackers, for hackers.

PROXARC is where embedded engineering meets elite RFID tooling.

