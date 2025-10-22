# ATTiny88 Breakout Board

A compact breakout board for the Microchip/Atmel ATtiny88 microcontroller. This repository contains the KiCad source, PCB/gerber exports, BOM, assembly notes, and example firmware to help you build and use the board.

Status
- Board design: Prototype (update to "Verified" or "Production" as appropriate)
- KiCad project: Hardware/ (KiCad project files)
- Example firmware: /firmware/examples

![Breakout Board](Hardware/Breakout_for_attiny88.jpg)

Quick links
- Hardware (KiCad project & schematics): Hardware/
- BOM: bom/bom.csv
- License: LICENSE (Mozilla Public License 2.0)

Features
- ATtiny88 (28-pin package) breakout to 0.1" headers
- 6-pin AVR ISP programming header
- Power supply decoupling and filter footprints
- Mounting holes for mechanical support

Repository layout
- Hardware/ — KiCad project files, schematics, PCB layouts
- hardware/gerbers/ — Exported Gerber/Drill files
- images/ — photos and pinout image(s)

Quick start (build & test)
1. Inspect schematic: open Hardware/ in KiCad and review the schematic
2. Program & test:
   - Connect a 6-pin AVR ISP to the ISP header.
   - Arduino as ISP (Arduino UNO example):
     - Upload ArduinoISP sketch to UNO.
     - Wire UNO to the board ISP header.
     - In Arduino IDE select correct ATTiny core/board and use "Upload Using Programmer".
   - avrdude example (update programmer type and port):
     - avrdude -c usbtiny -p t88 -P usb -U flash:w:firmware.hex
3. Basic verification:
   - Power the board and run any example assembly

License
This project is released under the Mozilla Public License 2.0 — see LICENSE for full text.

Maintainer
- mail4johnv (GitHub)
