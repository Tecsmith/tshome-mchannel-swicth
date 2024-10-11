# TecsmithHome MultiCannel Switch 

> *formerly known as:* **Floor Heating Valve Contrller**

> &#128679; `Placeholder for future project` &#128679; <br>
> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &#9888;&#9888;&#9888;&#9888;&#9888;&#9888;&#9888;&#9888;&#9888;&#9888; <br>
> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &#9888; ***DO NOT BUILD*** &#9888; <br>
> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &#9888;&#9888;&#9888;&#9888;&#9888;&#9888;&#9888;&#9888;&#9888;&#9888; <br>
> &#128679; `==============================` &#128679;


This work is based on the work done by @[Voltlog](https://github.com/voltlog)

- Voltlog website entry's: [revA](https://www.voltlog.com/tasmota-esp32-floor-heating-valve-controller-voltlog-383/), [revB](https://www.voltlog.com/revb-tasmota-esp32-floor-heating-valve-controller-voltlog-395/), [revC](https://www.voltlog.com/revc-tasmota-esp32-floor-heating-valve-controller-voltlog-397/) & *revD*
- Voltlog [YouTube video](https://www.youtube.com/watch?v=Sf9gnG1iW38)
- Voltlog open hardware [Github repo](https://github.com/voltlog/Valve-Actuator)
- ***Thank you @[Voltlog](https://github.com/voltlog)!***


## Intent

A 10-channel ~~underfloor heating value~~ [switch] control module.


## Key features changed from OG

- [ ] Multi-MCU support
  - **[ESP32 SOLO-2 modules](https://www.espressif.com/en/products/modules)**
    - `ESP32-S2-SOLO-2` - WiFi 2.4GHz *(802.11 b/g/n)
    - `ESP32-S2-SOLO-2U` - " + external antennae
  - **ESP32 WROOM modules**, *see [comparison]()*
    - `ESP32-S3-WROOM-1` - WiFi 2.4GHz, BLE 5
    - `ESP32-S3-WROOM-1U` - " + external antennae
    - `ESP32-C6-WROOM-1` - WiFi, BLE 5, Zigbee, Thread
    - `ESP32-C6-WROOM-1U` - " + external antennae
  - **[Shelly X MOD1-H8](https://x.shelly.com/shelly-x-mod1/)** *(ESP-Shelly-C38F)*
    - `Shelly-X-MOD1-H8` - WiFi 2.4, BT 5
    - `Shelly-X-MOD1U-H8` - " + external antennae
    - > shares the same footprint as the `ESP32 MINI-1` form factor.  See [VROOM vs. MINI](./docs/ESP32-VROOM-vs-MINI.md) for a comparison.
- [x] PCB Footprint - change to support [Gainta D9MG](https://www.gainta.com/en/d9mg.html) DIN Rail enclosure
- [x] Triac ~~*-or-* Relay option support~~ *(insufficient space for relays in RevA.)*
- [ ] Ethernet port
- [ ] Optional PoE module add-on support
- [ ] Pull down resistors on the GPIO's
- [ ] Support for per-channel override switches on the front panel.
- [ ] Remove status LED from main-PCB, and move them to the interface-PCB
  - The D9MG case supports a second PCB mounting point about 9mm from the top of the case.  This is enough space for both the LED's and the per-channel override switches.
- [ ] Blown fuse indicator leds
- [ ] Up the max in-bound load current to 8Amp and also add 1Amp fuses to each channel.

## Possible Issues

- D9MG enclosure is smaller than the original design, there may not be enough space for 10 channels.
- ... other "feature enhancements" ***will*** constrain the footprint realestate.
- Question:  For Ethernet port, on PCB or module?
