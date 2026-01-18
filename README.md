# Kapybara-PCB for Meshtastic
Modular PCB designed for Meshtastic projects, sized 120x70 mm, to be mounted as a standalone solar node in an outdoor enclosure (AliExpress box). Many modules are optional, at the user's discretion.

## License

This project is licensed under the **CERN Open Hardware Licence Version 2 - Strongly Permissive (CERN-OHL-S)**.

### What does this mean?
- **Sharing:** You are welcome to download, modify, and manufacture this PCB.
- **Attribution:** You must give appropriate credit to the original author (mpelli-Git).
- **Reciprocity:** If you make modifications or improvements to the design and distribute them, you **must** license your contributions under the same CERN-OHL-S license. This ensures that the entire community benefits from any improvements.

You can find the full text of the license in the [LICENSE](LICENSE) file or visit [https://ohwr.org/cern_ohl_s_v2.txt](https://ohwr.org/cern_ohl_s_v2.txt) for more details.

## Description

Modular PCB designed for Meshtastic projects, sized 120x70 mm, to be mounted as a standalone solar node in an outdoor enclosure (AliExpress box item 1005007587120013). Many modules are optional, at the user's discretion.

**Basic system**
- MCU: ProMicro Nice!nano compatible nRF52840
- LoRa module: HT-RA62 Lora SX1262
- Battery charge ctrl: CN3791 6V solar MPPT
- Battery: 18650 with PCB case holder SMD or THT opts.
- BMS, two op: a) PCB front, if the battery holder allows b) PCB back
- AliExpress box: item 1005007587120013 [AE box model grey 150x100x70](https://aliexpress.com/item/1005007587120013.html)
- Solar panel: use one of 6V and at least 1.5 W. I'm using [AE solar panel](https://es.aliexpress.com/item/1005009983374214.html)

**Optional**
- Power: SMD fuse, for power supply protection, with SMD fuse holder.
- Power percentage: R1+R2 for ADC MCU measurement of battery voltage
- Power telemetry: INA3221 3 channels
- Battery voltage superv.: TLV840 to reset MCU if undervoltage and mitigate brownouts
- Environmental telemetry, two op.: a) BME280 3.3V b) AHT20-BMP280
- GPS module: ATGM336H, for node time synchronization, with Mosfet control
- OLED display: female connector for e.g. SSD1306
