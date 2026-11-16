# Changelog

All test versions of LSapp. Installers are on the [Releases](https://github.com/Lupson665/LSapp/releases) page.

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
