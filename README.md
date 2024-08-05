# Peacock

Peacock is an RP2040 powered trackpad running QMK. It features an integrated Microchip MaxTouch sensor IC which is
connected to a 7" capacitive sensor.

This repo contains a fork of George Norton's project which I have modified to be a single PCB without the keyboard switches and encoders, I dont have the knowledge to have done this project myself hence why I have forked George's project.


## Features
- Fully PCBA, this other than switches and encoders, this board is designed to be fully factory assembled.
- Integrated RP2040 controller, no need to a separate controller.
- 7 inch 16:9 capacitive sensor.

## But how does it work?
The capacitive sensing IC is wired to a grid of diamond shaped electrodes. The diamonds are connected to form rows and columns. The IC scans the matrix by
applying a small voltage to the rows in turn, and then measuring voltage on the columns. Any conductive objects nearby (like your finger) will distrupt the
electrical field and can be detected.

## Software limitations
QMK currently supports pointing devices, but it reports them as USB hid mice. This means we only report a single pointer movement, a pair of scroll wheels and
a set of buttons to the host. For now, this prevents us from supporting some multitouch gestures such as pinch to zoom.

## Firmware
Peacock support has not yet been merged back to QMK. You can find a branch [here](https://github.com/george-norton/qmk_firmware/tree/peacock).
