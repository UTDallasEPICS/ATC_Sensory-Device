# Portable Hugs - Microcontroller Code
The ATC Sensory Cuff is a portable, wearable, mobile-app controlled device that applies a deep pressure sensory based intervention (SBI)to provide contactless relief from sensory overstimulation. The microcontroller for this device is the Heltec ESP32 WiFi Kit V3, programmed in C++. The ESP32 communicates with the Android and iOS mobile apps through Bluetooth Low Energy (BLE) to control or communicate with device peripherals (motor driver, pressure sensor, emergency stop, etc.). VSCode with the PlatformIO extension was utilized as the platform for developing on this microcontroller.

# Functional Requirements
Overall device requirements:
1. The bladder shall inflate and deflate when initiated by the iOS and Android mobile applications, or by the manual pushbuttons on the side of the enclosure.  
2. The minimum and maximum pressure inside the bladder shall be 14.7 PSI and 15.7 PSI, respectively.  
3. The device shall include an emergency stop button. 
4. The device shall be able to operate for at least 15 minutes of continuous use without requiring a change of batteries. 
5. The device shall include a 3D printed enclosure to house all electrical components.  
6. The electronics enclosure shall be enclosed in a fabric pouch. 
7. The enclosure pouch shall remain secure on the off-the-shelf adult-size bladder with minimal slippage during the recommended use period of 15 minutes.  
8. The device shall be accompanied by a user guide to explain device operation, iOS and Android application operation, and device maintenance and troubleshooting. 

ESP code requirements: 
1. ESP32 should establish a stable, secure Bluetooth connection to the mobile device.
2. User should be able to initiate inflate or deflate in free or cycle run on the mobile application and initiate the respective routine via Bluetooth on the ESP32. 
3. ESP32 should arrest inflate and start deflate in any operation mode when the e-stop is activated. 

# Tech Stack 
- update for any external libraries that we used or other packages

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
Updated on: 05/02/2024 by hardonom
Updated on: 05/07/2024 by tr0han