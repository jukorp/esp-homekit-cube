# esp-homekit-cube

Based on [Apple HomeKit accessory server library](https://github.com/maximkulkin/esp-homekit).

## Setup
1. Initialize and sync all submodules (recursively):
```shell
git submodule update --init --recursive
```
2. Copy wifi.h.sample -> wifi.h and edit it with correct WiFi SSID and password.
3. Install [esp-open-sdk](https://github.com/pfalcon/esp-open-sdk), build it with `make toolchain esptool libhal STANDALONE=n`, then edit your PATH and add the generated toolchain bin directory. The path will be something like /path/to/esp-open-sdk/xtensa-lx106-elf/bin. (Despite the similar name esp-open-sdk has different maintainers - but we think it's fantastic!)

4. Install [esptool.py](https://github.com/themadinventor/esptool) and make it available on your PATH. If you used esp-open-sdk then this is done already.
5. Checkout [esp-open-rtos](https://github.com/SuperHouse/esp-open-rtos) and set SDK_PATH environment variable pointing to it.

## Hardware
- [Adafruit Huzzah Feather](https://www.adafruit.com/product/2821)
- Neopixels (with data connection attached to `RX` pin) 

## commands:
- `make -C src erase_flash`
- `make -C src test`
- `make -C src monitor`
