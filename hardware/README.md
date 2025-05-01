# DIN Rail Power Meter (9 channels) - Hardware

![Latest version](https://img.shields.io/badge/latest%20version-AAA-orange)

## PCB Size

<img src="../images/D2MG_PCB.png" align="left" alt="D2MG Box">
The D2MG box can house PCBs on three levels.

The green board is the main metering board (32.7mm x 86.5mm) with the
ATM90E32 ICs and the voltage and CT input terminals.

The orange board is the power supply board (32.7mm x 58.3mm), with the 3.3V
DC power supply, and the protection varistors for the high-voltage AC input.

The purple board is a 3D printed plastic part that holds the OLED display.

## Schematics



[schematics.pdf](schematics.pdf)

## WiFi Controller

<img align="left" src="../images/esp32-s3.png" alt="Photo of the ESP32 controller">
The PCB is designed to accomodate an ESP32-S3 SuperMini controller.


<img src="https://esphome.io/_static/made-for-esphome-black-on-white.png" align="left" alt="Made for ESPHome logo" width="150">

The default firmware is ESPHome, you can find the configuration to it in the
[esphome](../esphome/README.md) folder.


### GPIO Pinout

| Pin    | Function             |
| ------ | -------------------- |
| GPIO9  | SPI MOSI             |
| GPIO10 | SPI MISO             |
| GPIO12 | SPI SCLK             |
| GPIO11 | SPI CS IC1           |
| GPIO2  | SPI CS IC2           |
| GPIO4  | SPI CS IC3           |
| GPIO5  | I2C SCL              |
| GPIO6  | I2C SDA              |
| GPIO13 | IC1 IRQ              |
| GPIO1  | IC2 IRQ              |
| GPIO3  | IC3 IRQ              |
| GPIO48 | Status Led           |

### Status LED

| Color           | State |
| --------------- | ----- |
| Red Blinking    | Errored state |
| Red             | Powered, not connected to WiFi |
| Blue            | Connected to WiFi |
| Green           | Native API connected |
