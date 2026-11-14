# ⚡ IoTrace — IoT Circuit & Wiring CAD Workbench

🌐 **Live Web App:** [https://vercel.app](https://vercel.app)

**IoTrace** is a browser-based visual circuit diagram and hardware wiring workbench built for IoT engineers, embedded developers, and students. It replaces messy hobbyist wiring with clean, **90° Manhattan orthogonal routing**, dynamic floating pin labels, and high-resolution schematic exports—all running in a single, zero-dependency HTML5 file.

---

## ✨ Key Features

* **Infinite Pan & Zoom Canvas:** Smooth mouse-wheel zooming and middle/left-click panning over a 20px snap-to-grid coordinate matrix.
* **90° Orthogonal Wiring Engine:**
  * Click any terminal pin to start routing and click the canvas to anchor crisp 90° turns.
  * Supports **on-board 90° wire segmentation** over large Nucleo-64 boards (`F401RE` & `F410RB`) for clean inner-header routing.
  * Drag corner handles anytime to reshape existing traces.
* **Smart Floating Wire Pin Labels:** Connecting a wire to a pin automatically hides that pin's label on the board and floats it cleanly above the wire near the terminal, keeping schematics readable and clutter-free.
* **Batch Auto-Connect Queue:** Queue multiple source-to-destination pin connections with custom trace colors and route them all simultaneously outside board boundaries in one click.
* **Multi-Select & Rigid Group Movement:** Use `Shift + Click` or `Shift + Drag` marquee selection to select multiple components, copy/paste (`Ctrl+C` / `Ctrl+V`), rotate (`R`), or drag entire sub-circuits while preserving internal wire geometry.
* **Live Component Properties Inspector:** Select placed **LEDs** or **Resistors** on the canvas to dynamically change LED colors (`Red`, `Green`, `Blue`, `Yellow`, `White`) or resistance values (`220Ω` to `10kΩ` or custom) with live color-band updates.
* **Interactive Netlist & Table Export:** View all active interconnects in a slide-out Netlist drawer and download a clean, high-resolution **Wiring Netlist Table PNG**.
* **Dual Theme & 3x Retina PNG Export:** Toggle between **Dark Terminal Mode** and **Light Schematic Mode** (with automatic Black/White trace adaptation) and export crisp 3x-scaled `.png` circuit diagrams.
* **Full Undo/Redo & Auto-Save:** Up to 100 steps of `Ctrl+Z` / `Ctrl+Y` history with automatic `localStorage` persistence.

---

## 📦 Included Hardware Library

* **Microcontrollers:**
  * STM32 Blue Pill (`STM32F103C8T6`)
  * STM32 Nucleo-F401RE 
  * STM32 Nucleo-F410RB 
  * Wemos D1 Mini (`ESP8266`)
  * AT89S52 (`40-Pin DIP 8051 MCU`)
* **Sensors & Displays:**
  * GY-BME280 Pressure, Humidity & Temperature Sensor
  * 16x2 Alphanumeric LCD (`HD44780 / 1602A`)
  * 7-Segment Display (`5161AS` Common Cathode)
* **Interfaces & Actuators:**
  * USB-to-TTL Converter (`FT232RL` FTDI Breakout)
  * 4x4 Matrix Keypad (`R1–R4`, `C1–C4`)
  * 28BYJ-48 5V Unipolar Stepper Motor
* **Instruments & Discrete Passives:**
  * Digital Storage Oscilloscope (`CH1 Probe` & `GND Clip`)
  * Tactile Pushbutton (`4-Pin SPST`)
  * Configurable 5mm LED & 1/4W Axial Resistor

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| **`Shift + Drag`** | Box-select multiple components |
| **`Shift + Click`** | Add or remove a component from selection |
| **`Ctrl + A`** | Select all components on canvas |
| **`Ctrl + C` / `Ctrl + V`** | Copy and paste selected components & internal wires |
| **`R`** | Rotate selected component(s) 90° |
| **`Ctrl + Z` / `Ctrl + Y`** | Undo / Redo changes |
| **`Delete` / `Backspace`** | Delete selected component(s) or wire |
| **`Right-Click` / `Esc`** | Step back a wire corner or cancel active wiring |

---

## 🚀 Getting Started

* **Use Online:** Open [https://vercel.app](https://vercel.app) directly in your browser.
* **Run Locally:** Clone this repository and open `index.html` in any modern web browser—no build tools, Node.js, or servers required.

---

## 🛠️ Built With

* **HTML5 & Vanilla JavaScript** (Custom SVG Coordinate Matrix & Orthogonal Router)
* **Tailwind CSS** (CDN)
* **Lucide Icons** & **JetBrains Mono / Inter** Typography

## 📄 License

Open-source under the [MIT License](LICENSE).
