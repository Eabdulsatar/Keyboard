# Corne Keyboard Firmware and Keymaps

This repository contains the firmware, keymaps, and configuration settings for my Corne keyboard.
This uses the pandakb matrices for a shield and the promicro nrf52840 as a controller.

It includes:

- Keymaps tailored for programming and ergonomics.
- Firmware files compatible with the pandakb Corne keyboard.
- Documentation for myself so I don't forget what any of this does 3 weeks from now.

## Structure
[[Build.yaml]] - Instructions on what firmware to build and compile.
This outputs a number of firmware files for either the left or right side side of the board.
Currently this will build files for L and R sides for NiceOLED displays.

[[config/corne.keymap]] - Details the behaviour of keys on the shield. 
Defines what happens when you press what and what layers are available for use.
This includes behaviours and the likes.

[[config/corne.conf]] - This is detailed more in the [system configuration](https://zmk.dev/docs/config) page for ZMK.
This is the Kconfig file for the shield for both sides of the keyboard. This configures many settings on the board such as
- sleep times
- displays
- bluetooth settings 
- and more
Using the `left` or `right` suffixes you can configure both sides independently. If a single file is supplied, it will be 
applied to both boards.

## Building and compiling
This repo is automatically built and compiled as part of a GitHub workflow. Artefacts can be retrieved there.