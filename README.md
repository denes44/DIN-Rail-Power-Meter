# DIN Rail Power Meter (9 channels)

![Based on ESP32-S3 board](https://img.shields.io/badge/hardware-ESP32--S3-blue?logo=espressif)
![With ESPHome as a firmare](https://img.shields.io/badge/firmware-esphome-blue?logo=esphome)
![Home Assistant Compatible](https://img.shields.io/badge/homassistant-compatible-blue?logo=homeassistant)

<img src="images/D2MG.png" align="left" alt="D2MG Box">

This is a **9 channel**, 3 phase power meter designed to fit in a 2 module wide
DIN enclosure.

The device can be used on 3-phase systems, there are 3 current channels for
every phase (a total of 9 channels).
It can also be used on a 1-phase system as well.

On the front there is a small OLED display that can display the metering
information.

The project is inspired from: https://github.com/CircuitSetup/Expandable-6-Channel-ESP32-Energy-Meter

> [!NOTE]
> If you are looking for the easiest way to **start using your display
> under Home Assistant:** ***[Home Assistant Quick Start Guide](HomeAssistant.md)***

> [!CAUTION]
> The circuit is not isolated from the mains, so it is not safe to tuch any
> part of the board during use, nor connecting the device with
> other electrical interfaces without proper isolation!
> The AC neutral is connected to DC ground, so treat the circuit as you would
> with any live circuit!

## Hardware

The hardware uses two PCBs, one for the measurement and one for power,
that fits into a D2MG 2 module width DIN rail enclosure.

More information about the hardware can be found in the
**[hardware](hardware/README.md)** folder.

<img src="images/meter_board_top.png" alt="Meter Board PCB Top Side">

<img src="images/meter_board_bottom.png" alt="Meter Board PCB Bottom Side">

## ESPHome
<img src="https://esphome.io/_static/made-for-esphome-black-on-white.png" align="left" alt="Made for ESPHome logo" width="200">

The meter uses an ESP32-S3 controller and ESPHome as it's firmware.

More information about the ESPHome firmware can be found in the
**[esphome](esphome/README.md)** folder.