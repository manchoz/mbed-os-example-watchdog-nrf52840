# mbed-os-example-watchdog-nrf52840
Example repo for testing the Mbed OS [nRF52840 Watchdog implementation](https://github.com/ARMmbed/mbed-os/pull/11684)

This has been tested both on [Makerdiary nRF52840-MDK](https://wiki.makerdiary.com/nrf52840-mdk/) and [Arduino Nano 33 BLE](https://www.arduino.cc/en/Guide/NANO33BLE) (via Arduino Platform).

The `main.cpp` file contains the example code from the [Mbed OS Watchdog API](https://os.mbed.com/docs/mbed-os/v5.14/apis/watchdog.html) documentation.

## Steps to reproduce

### Clone this repo

_(Please, note that this repo will checkout a branch with Makerdiary nRF52840-MDK support too)_.

```shell
git clone https://github.com/manchoz/mbed-os-example-watchdog-nrf52840
cd mbed-os-example-watchdog-nrf52840
mbed deploy
mbed config root .
mbed compile --toolchain GCC_ARM --target NRF52840_MDK --flash --sterm --baudrate 115200
```

Watch your board die and restart _or_ press `BUTTON1` to reset the watchdog.

### Preliminary steps for Makerdiary nRF52840-MDK

####  Makerdiary nRF52840-MDK hookup

1. Connect the nRF52840-MDK to the [Base Dock](https://store.makerdiary.com/collections/frontpage/products/base-dock).
2. Connect a Grove Button to the Port 1 of the Base Dock.
