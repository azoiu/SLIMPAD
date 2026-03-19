# SlimPad 🎮

A compact 12-key macropad with a rotary encoder and OLED display — designed from scratch for [Hack Club Blueprint](https://hackclub.com/blueprint/).

---

## What is SlimPad?

SlimPad is a custom mechanical macropad built to boost productivity with one-press shortcuts and a smart clipboard history system. You copy something, it saves it. Rotate the encoder to pick which copied item you want, click to paste it. Simple.

Built entirely from scratch — PCB designed in KiCad, case modeled in Fusion 360, firmware written in KMK (CircuitPython).

---

## Features

- **12 mechanical switches** in a 3×4 grid
- **Rotary encoder** — scroll through last 5 copied items, click to paste
- **OLED display** — shows clipboard preview and position in history
- **One-press shortcuts** — Save, Undo, Redo, Screenshot, Find and more
- **3D printed sandwich case** with M3 heatset inserts

---

## How clipboard history works

1. Press **COPY** → sends Ctrl+C and saves to history
2. **Rotate encoder** → scroll through last 5 copied items
3. **Click encoder** → paste the selected item
4. OLED shows live preview of selected entry

---

## Key Layout
```
┌──────────┬──────────┬──────────┐
│  COPY    │  PASTE   │  UNDO    │
├──────────┼──────────┼──────────┤
│  SAVE    │ SAVE AS  │  REDO    │
├──────────┼──────────┼──────────┤
│ SEL ALL  │  CUT     │  FIND    │
├──────────┼──────────┼──────────┤
│  NEW     │  CLOSE   │  PSCR    │
└──────────┴──────────┴──────────┘
     Encoder: scroll clipboard / click to paste
```

---

## Bill of Materials

| Component | Qty | Notes |
|-----------|-----|-------|
| Seeed XIAO RP2040 | 1 | Microcontroller |
| MX-style switches | 12 | Any MX-compatible |
| 1N4148 diodes | 12 | Through-hole |
| EC11 rotary encoder | 1 | 5-pin, with click |
| 0.91" OLED SSD1306 | 1 | I2C, GND-VCC-SCL-SDA |
| DSA keycaps blank white | 12 | |
| M3×16mm screws | 4 | |
| M3×5mm×4mm heatset inserts | 4 | |

---

## Project Structure
```
SLIMPAD/
  CAD/          — STL files for 3D printed case
  FIRWARE/      — KMK firmware (main.py)
  PCB/          — KiCad schematic and PCB layout
  README.md     — this file
```

---

## Screenshots

![PCB](PCB/pcb.jpg)
![Schematic](PCB/sch.jpg)
![Case](CAD/cad1.jpg)

---

## Built with

- [KiCad 9](https://www.kicad.org/) — PCB design
- [Fusion 360](https://www.autodesk.com/products/fusion-360) — case design
- [KMK Firmware](https://github.com/KMKfw/kmk_firmware) — keyboard firmware
- [CircuitPython](https://circuitpython.org/) — runtime

---

## License

MIT — feel free to remix and build your own!

Built with ❤️ for Hack Club Blueprint. This is my first ever hardware project — PCB, case and firmware all made from scratch.
