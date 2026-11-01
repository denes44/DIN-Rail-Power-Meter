# DIN Rail Power Meter - ESPHome Firmware

<img src="https://esphome.io/_static/made-for-esphome-black-on-white.png" alt="Made for ESPHome logo" width="400">

![Latest version](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2Fdenes44%2FDIN-Rail-Power-Meter%2Frefs%2Fheads%2Fmain%2Fesphome%2Ffirmware%2Fmanifest.json&query=%24.version&logo=esphome&label=latest%20version&color=orange&logo=esphome)

## Firmware

The default firmware to use is [firmware/power-meter-esp32s3.factory.bin](firmware/power-meter-esp32s3.factory.bin).
With this firmware you can use [Improv via BLE](https://esphome.io/components/esp32_improv)
or [Improv via Serial](https://esphome.io/components/improv_serial)
to provision your device.

## Configuration

### Factory

The factory firmware uses the [power-meter.factory.yaml](power-meter.factory.yaml)
configuration file.

### ESPHome Dashboard

To import the configuration to your ESPHome Dashboard, use the [power-meter.yaml](power-meter.yaml)
file.

By default this file imports the core configuration from GitHub dynamically.

### Core functions

Both of these config files import the following files which contains specific
functionality for the device:

- [power-meter-metering.yaml](power-meter-metering.yaml)
- [power-meter-display.yaml](power-meter-display.yaml)

## Firmware update

### Factory

In this configuration mode, the device uses the built-in [HTTP Update platform](https://esphome.io/components/update/http_request.html).

If an update is available, you can update the device from the Web GUI, or from
Home Assistant directly, if you added the device to Home Assistant.

### ESPHome Dashboard

In this configuration mode, a text sensor called `Remote YAML Update`
is provided, to indicate if the remote core yaml configuration is newer than
what's installed on the device.

If you do a firmware install from the dashboard, the build process will use
the new core yaml file from GitHub dynamically.
