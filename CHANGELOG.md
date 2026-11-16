# Changelog

All test versions of LSapp. Installers are on the [Releases](https://github.com/Lupson665/LSapp/releases) page.

## 0.000.5 (test version)

- Portless USB connection (HID), test version, Pro Micro / Leonardo only: option "Portless USB (HID)" in "Flash LSboard firmware". LSapp then talks to the board without a COM port ("Port: USB (HID)"). The COM port stays for the board configurator and flashing.
- USB joystick buttons are now optional ("Joystick buttons (1-32)", off by default). With no axes and no buttons the board is not a joystick at all.
- PCF8575 expanders are now optional in the firmware ("PCF8575 (I2C expander)" in "Flash LSboard firmware"). Without PCF8575 and OLED the firmware is about 3.7 KB smaller.
- Board configurator shows what the firmware has: joystick axes and buttons, portless connection, and which parts were left out (OLED, 7-segment, motors, PCF8575).

## 0.000.4 (test version)

- USB joystick axes: choose 1-8 axes when flashing the firmware (Pro Micro / Leonardo). Axis 1 = potentiometer 1, axis 2 = potentiometer 2...
- Board package import: new column "Into your rule" - names can be imported into the rule of another aircraft (e.g. Fenix names into a Boeing rule).

## 0.000.3 (test version)

- Automatic updates from GitHub (only versions approved by the author).
- Import of MobiFlight boards (.mfmc) and MobiFlight profiles (.mfproj).
- Board packages (.lspack): export / import boards with their assignments.
- Save / load board layout to a file (.lsboard) in the board configurator.
- New aircraft rule can start with row names copied from another rule.
