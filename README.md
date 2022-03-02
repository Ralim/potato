# JouleCounter

OpenSource inline USB-PD Power meter

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

## Hardware requirements

- 4x ADC channels (Power supply, D+,D-,Current)
- I2C for:
- - ssd1327 display
- - FUSB302
- 3x GPIO for QC
- 2+ GPIO for buttons

## Pinenute 12S Pinout

https://pine64.com/product/pinenut-model12s-wifi-ble5-stamp/

### GPIO allocations

- GPIO 0 : QC GPIO
- GPIO 1 : Encoder A
- GPIO 2 : FUSB302 IRQ
- GPIO 3 : I2C SDA
- GPIO 4 : I2C SCL
- GPIO 5 : ADC - VBus
- GPIO 7 : UART Rx
- GPIO 8 : Boot mode + User Button on encoder
- GPIO 11 : ADC - Current
- GPIO 12 : ADC - D+
- GPIO 14 : ADC - D- OR DAC for QC signalling
- GPIO 16 : Uart Tx
- GPIO 17 : Encoder B

## Names

- JouleCounter
- Open-PFT
- Open-JOLT joule & ohm limit tester
