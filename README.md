# Potato

OpenSource inline USB-PD Power meter.

...WIP...

## Desired features

- Easy to assemble (No QFN)
- Read device PD capabilities
- Capture USB-PD messages
- Read USB D- / D+ voltages for QC
- Pull resistors for QC control
- UART or USB for datalogging
- Either buttons or encoder for input
- Small LCD display
- DC In/Out port

- Accelerometer or tilt switch for rotation?

## Ideas to explore

- As LVGL is a goal for the UI, consider [prototyping](https://docs.lvgl.io/latest/en/html/get-started/pc-simulator.html) on "real" computer or talking to the PineTime team about their experience about developing [UI in NaCL](https://github.com/AppKaki/lvgl-wasm), allowing feedback from web users. If realized, this may allow more explorative development in a less painful environment as you can skip the slow upload/reboot cycle.
