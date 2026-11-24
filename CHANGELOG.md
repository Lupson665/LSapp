# Changelog

All test versions of LSapp. Installers are on the [Releases](https://github.com/Lupson665/LSapp/releases) page.

## 0.000.8 (test version)

- New boards: **WeAct RA4M1** (all pins usable, named like on the board: P100, P101…) and **Arduino UNO R4 Minima**. LSapp finds a running RA4M1 board by itself – no port needed – and installs the USB driver for the upload mode the first time (Windows asks for permission).
- **Install bootloader…** (Flash LSboard firmware, WeAct RA4M1): a new WeAct board comes without the Arduino bootloader. LSapp now installs it itself – hold BOOT, press RESET, release BOOT, click OK. No other program is needed.
- Board configurator: a **drawing of the board** next to the elements. It shows which pins are used and which are free; click a pin to put it into the pin field.
- "Read more…" for the elements now has pictures and wiring diagrams.
- **Getting started** guide for a new cockpit (opens by itself on the first start without boards), a **Help ▾** menu in the main window, and short tips in the windows (turn them off in Help ▾).
- LSapp now installs into **C:\Program Files\LSapp** ("Install for me only" is still offered). Your boards, assignments and settings are kept in **%LOCALAPPDATA%\Lupson Simulation\LSapp**; on the first start LSapp copies them there from the old program folder. New tray menu item **Open data folder**.
- Board configurator: when a board has a COM port but sends nothing, LSapp suggests unplugging its USB cable and power supply.

## 0.000.7 (test version)

- Fix: Arduino Mega 2560 clones (CH340) could not be read or written in the board configurator (`No answer to @INFO`, `@CLEAR -> no answer`). When the port opens, LSapp now ignores old data left from before the board's reset and waits until the board has really started, so commands no longer reach the bootloader.
- The serial port is opened like in Arduino IDE (DTR and RTS on).
- Board configurator: "Read board" asks the board up to 3 times.

## 0.000.6 (test version)

- PCF8575 expanders are now optional in the firmware ("PCF8575 (I2C expander)" in "Flash LSboard firmware").
- "Flash LSboard firmware": the options (OLED, 7-segment, motors, PCF8575) start unchecked - tick only what the board uses. Choices saved earlier are kept.
- "Flash LSboard firmware": USB ports are listed first, so the main-board COM1 is no longer picked by default. The empty LSboard.ino field says that the firmware built into LSapp is used.
- A freshly flashed board is announced ("New board ... on COMx"); click it to open the board configurator.
- Board configurator: shows which parts the firmware was built without, and what a board sent when it does not answer.
- Remove a board: right-click its tab in the main window -> "Remove board" (names and expressions can be deleted or moved to another board).
- New board ID in the board configurator: add it as a new board, or let it replace an existing board.
- A board connected over portless USB (HID) is no longer searched again on its COM port.

## 0.000.5 (test version)

- Portless USB connection (HID), test version, Pro Micro / Leonardo only: option "Portless USB (HID)" in "Flash LSboard firmware". LSapp then talks to the board without a COM port ("Port: USB (HID)"). The COM port stays for the board configurator and flashing.
- USB joystick buttons are now optional ("Joystick buttons (1-32)", off by default). With no axes and no buttons the board is not a joystick at all.
- Board configurator shows what the firmware has: joystick axes and buttons, portless connection.

## 0.000.4 (test version)

- USB joystick axes: choose 1-8 axes when flashing the firmware (Pro Micro / Leonardo). Axis 1 = potentiometer 1, axis 2 = potentiometer 2...
- Board package import: new column "Into your rule" - names can be imported into the rule of another aircraft (e.g. Fenix names into a Boeing rule).

## 0.000.3 (test version)

- Automatic updates from GitHub (only versions approved by the author).
- Import of MobiFlight boards (.mfmc) and MobiFlight profiles (.mfproj).
- Board packages (.lspack): export / import boards with their assignments.
- Save / load board layout to a file (.lsboard) in the board configurator.
- New aircraft rule can start with row names copied from another rule.
