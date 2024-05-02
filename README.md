# Overview - Portable Hugs Microcontroller Code
The ATC Sensory Cuff is a portable, wearable, mobile-app controlled device that applies a deep pressure sensory based intervention to provide contactless relief from sensory overstimulation. The microcontroller for this device is the Heltec ESP32 WiFi Kit V3, programmed in C++. The ESP32 communicates with the Android and iOS mobile apps through Bluetooth Low Energy (BLE) to control or communicate with device peripherals (motor driver, pressure sensor, emergency stop, etc.). VSCode with the PlatformIO extension was utilized as the platform for developing on this microcontroller.

# Instructions to Clone, Build, and Run

## Prequisites

The following instructions assume the following are downloaded/added:

1. Visual Studio Code IDE
2. VSCode PlatformIO extension
3. VSCode GitHub Codespaces extension

## Cloning a Project

1. In VSCode, type `CTRL+SHIFT+P` and find `Git: Clone
2. Enter the following url <https://github.com/UTDallasEPICS/ATC-Sensory-Device.git> and press `ENTER` to clone the project

## Build and Run

1. Open the PlatformIO extension from the Activity Bar in VSCode
2. Under quick access > micellaneous click on New Terminal
3. To build the project enter `pio run` in the command line
4. To build and run the project enter `pio run --target upload`in the command line
5. If issues with port connection occur, ensure appropriate drivers are downloaded from this link: https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads 

### Credits

Updated on: 10/13/2023 by VT_c0des
