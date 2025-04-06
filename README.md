# OpenBook Project - README

This repository contains the hardware, manufacturing, mechanical, and documentation files for **OpenBook**, a low-cost, open-source e-book reader built around the **ESP32-C6** microcontroller.

---

## Overview

The OpenBook is a low-power, open-source e-book reader designed around the ESP32-C6 microcontroller. Featuring Wi-Fi 6 and Bluetooth LE, it uses a large 7.5-inch e-paper display to achieve excellent readability and battery performance.

This document includes the system block diagram, hardware pinout, BOM, component links, design log, and licensing.

---

## System Block Diagram

Images/BlockDiagram.png

---

## Bill of Materials (BOM)

| Name of component | Device                                       | Check Prices                                                                                                | DataSheet                                                                                                 |
|-------------------|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| U1                | W25Q512JVEIQ                                 | https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda                             | https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda                             |
| U2                | ESP32-C6-WROOM-1-N8                          | https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda                        | https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda                        |
| U3                | DS3231SN#                                    | https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda                                   | https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda                                   |
| U4                | MAX17048G+T10                                | https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda                                 | https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda                                 |
| U5                | ESP32_WROVER_SPARKFUN-IC-POWER_MCP73831      | https://eu.mouser.com/ProductDetail/Microchip-Technology/MCP73831T-2ACI-OT?qs=yUQqVecv4qvbBQBGbHx0Mw%3D%3Dcf   | https://eu.mouser.com/ProductDetail/Microchip-Technology/MCP73831T-2ACI-OT?qs=yUQqVecv4qvbBQBGbHx0Mw%3D%3Dcf   |
| BOOT_BUTTON       | BUTTON_CUSYOMV1                             | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| CHANGE_BUTTON     | BUTTON_CUSYOMV1                             | https://industry.panasonic.com/global/en/products/control/switch-light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch-light-touch/number/evqpuj02k                  |
| RESET_BUTTON      | BUTTON_CUSYOMV1                             | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| Q1                | ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_...| https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated                                  | https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated                                  |
| Q2                | ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_...| https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated                                  | https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated                                  |
| Q3                | D8                                           | https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay                                           | https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay                                           |
| PFMF.050.1        | ESP32C6_VARISTORCN1812                       | https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D              | https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D              |
| IC1               | BD5229G-TR                                   | https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor                                    | https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor                                    |
| IC4               | XC6220A331MR-G                               | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                              | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                              |
| J1                | FH34SRJ-24S-0.5SH_99_                        | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                              | https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex                                              |
| J2                | SAMACSYS_PARTS_USB4110-GF-A                  | https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY               | https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY               |
| J3                | QWIIC_CONNECTORJS-1MM                        | https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY               | https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY               |
| J4                | 112A-TAAR-R03_ATTEND                         | https://store.comet.srl.ro/Catalogue/Product/43497/                                                            | https://store.comet.srl.ro/Catalogue/Product/43497/                                                            |
| L1                | 744043680IND_4828-WE-TPC_WRE                 | https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D               | https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D               |
| SENSOR2           | ESP32_WROVER_BME680_BME680                   | https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home                                            | https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home                                            |
| SJ1              | SJ                                           | https://grabcad.com/library/solder-jumpers-1                                                                   | https://grabcad.com/library/solder-jumpers-1                                                                   |
| C1                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C1_BAT            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C1_BAT1           | EAGLE-LTSPICE_CC0402                         | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C1_BAT2           | EAGLE-LTSPICE_CC0402                         | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C2                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C2_BAT\           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C3                | RCL_CPOL-EUCT3528                            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C4                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C4_USB            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C5                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C5_USB            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C6                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C7                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C8                | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C9                | EAGLE-LTSPICE_CC0402                         | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C10               | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| C10_SUPERCAP      | CPH3225A                                     | https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda                                   | https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda                                   |
| CHG_LED           | ADAFRUIT_LEDCHIP-LED0603                     | https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603                       | https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603                       |
| C_DELAY           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| D1                | USBLC6-2SC6Y                                 | https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda                              | https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda                              |
| D2                | ESP32_WROVER_AVX---SD0805S020S1R0_AVX_...    | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D              | http://datasheets.avx.com/schottky.pdf                                                                         |
| D3                | MBR0530                                      | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D              | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D              |
| D4                | MBR0530                                      | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                                | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                                |
| D5                | MBR0530                                      | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                                | https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda                                                |
| D6                | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D7                | ESP32_WROVER_AVX---SD0805S020S1R0_AVX_...    | https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D              | http://datasheets.avx.com/schottky.pdf                                                                         |
| D8                | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D9                | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D10               | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D11               | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| D12               | PGB1010603MR                                 | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      | https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda                                      |
| EPD_C1            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C2            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C5            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C6            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C7            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C8            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C9            | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C10           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C11           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| EPD_C12           | ESP32_WROVER_EAGLE-LTSPICE_CC0402            | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  | https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k                  |
| R1                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R1-PINH           | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R1-PINH1          | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R1_BAT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R1_PWRUSB         | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R2                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R2-PINH           | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R2-PINH1          | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R2-USB            | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R2-USB1           | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R2_BAT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R3                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R4                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R5                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R6                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R7                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R8                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R9                | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R10               | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R_BOOT            | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R_CAPACITOR       | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R_CHANGE          | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R_CL1             | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| R_RESET           | ESP32_WROVER_EAGLE-LTSPICE_RR0402            | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         | https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL                         |
| TP1               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP2               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP3               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP4               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP5               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP6               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP7               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP8               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP9               | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP10              | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP11              | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP12              | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP13              | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP14              | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP15              | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP16              | TPTP20R                                      | -                                                                                                            | -                                                                                                           |
| TP17              | TPTP20R                                      | -                                                                                                            | -                                                                                                           |

---

## Main Hardware Components

# ESP32-C6 Microcontroller

- Architecture: 32-bit RISC-V core operating up to 160 MHz
- Communication: Built-in Wi-Fi 6, Bluetooth 5 LE, and USB 2.0 interface
- RAM & Storage: 512KB SRAM onboard, paired with 8MB external flash
- Power Efficiency: Equipped with advanced low-power and sleep modes
- I/O Capabilities: Supports SPI, I²C, UART, and multiple GPIOs

# SD Card Slot

- Storage Role: Enables additional memory for e-books, logs, and firmware
- Interface Options: Compatible with both SPI and native SD protocols

# External Memory

- Type: Serial NOR Flash, model W25Q512JVEIQ
- Capacity: Provides 8MB for firmware storage and high-volume data

# E-Paper Display

- Dimensions & Quality: 7.5-inch diagonal, 800×480 resolution
- Energy Profile: Consumes power only during updates; remains static otherwise
- Data Transfer: Communicates using a 4-wire SPI interface

# USB-C Interface

- Primary Roles: Allows battery charging, data transfer, and firmware updates
- Electrical Safety: Integrated ESD protection and compliant terminations
- Update Support: Enables both USB-based and OTA software upgrades

# Power Management

- Energy Source: Uses a 2500mAh 3.7V Li-Po rechargeable battery
- Monitoring Features: Battery state tracked via MAX17048 fuel gauge (I²C)
- Charging Circuitry: Based on MCP73831 controller via USB-C input
- Voltage Regulation: Supplies a clean 3.3V rail using an LDO such as XC6220

# Environmental Sensor

- Sensor Type: BME688 integrated environmental sensor
- Measured Parameters: Ambient temperature, relative humidity, atmospheric pressure, and air quality (VOC/eCO2)
- Communication: I²C protocol at 400kHz

# Input Controls

- Functional Use: Facilitates navigation, menu interaction, and device reset

---

## Communication Interfaces Overview

# USB

- Provides both power input and data communication via the USB-C port.
- Supports firmware flashing and charging through a single interface.

# I²C Bus

- Used to interface with low-speed peripherals such as:
    - Environmental sensor (BME688)
    - Battery monitoring chip (MAX17048)
    - RT Clock (DS3231)
    - Qwiic-compatible expansion modules

# General Purpose I/O (GPIO)

- Dedicated digital inputs for tactile button controls (3x)
- Additional control signals for peripherals, such as:
    - Display reset
    - E-paper busy status monitoring
    - Power control or wake signals

# SPI Interface

- Standard 4-wire SPI used for driving the e-paper display

---

## Estimated Power Consumption

This section provides an overview of the average power consumption for each hardware component in the OpenBook E-Reader during both active use and sleep modes.

| Component                   | Active Mode Consumption | Sleep / Idle Consumption     | Notes                                                                 |
|----------------------------|--------------------------|-------------------------------|-----------------------------------------------------------------------|
| **ESP32-C6 MCU**           | 80–150 mA                | < 50 µA (deep sleep)          | Includes Wi-Fi processing and peripheral control                     |
| **7.5” E-Paper Display**   | ~30–40 mA (during refresh) | ~1 µA (static image retained) | Power only consumed during screen updates                            |
| **BME688 Sensor**          | ~2.1 mA                  | < 1 µA (standby mode)         | Used for environmental data collection (temp/humidity/air quality)   |
| **DS3231 RTC**             | —                        | ~2 µA                         | Always running to keep accurate time                                 |
| **MAX17048 Fuel Gauge**    | ~50 µA                   | ~50 µA                        | Monitors battery level continuously                                  |
| **MCP73831 Charging IC**   | Up to 1A (when charging) | 0 µA (when idle)              | Controlled via USB VBUS connection                                   |
| **Buttons (3x)**           | 0 mA (passive)           | 0 mA                          | Use GPIO input pull-downs; no active consumption                     |
| **SD Card (optional)**     | 10–30 mA (read/write)    | 0 mA (unmounted)              | Used only during eBook loading or logging                            |
| **USB Peripherals**        | Varies (USB Host mode)   | 0 mA                          | Only active when data transfer is in use                             |

### Total Estimated Consumption

| Usage Scenario                | Estimated Total Current |
|------------------------------|-------------------------|
| **Full Active Reading**      | ~120–170 mA             |
| **Wi-Fi + Sensor Polling**   | ~100–130 mA             |
| **Partial Sleep (Wi-Fi Off)**| ~5–10 mA                |
| **Deep Sleep (RTC only)**    | ~100–150 µA             |

### Battery Life Estimation

Given a 2500 mAh 3.7V Li-Po battery:

- **Active Reading 2 hours/day** → ~7–10 days battery life
- **Standby Mode Only** → up to **1 month**
- **Mixed Use (Wi-Fi, sensors, display refreshes)** → 5–7 days typical

These values are estimations and will vary depending on usage patterns, Wi-Fi activity, and environmental sensor polling intervals.

---

## ESP32-C6 Pin Mapping

This table shows the actual GPIO-to-function mapping as used in the OpenBook E-Reader, based on the schematic of the ESP32-C6-WROOM-1-N8 module provided.

| GPIO      | Label in Schematic | Function Description                        | Peripheral / Role                     |
|-----------|---------------------|---------------------------------------------|---------------------------------------|
| **GPIO9** | IO0 / BOOT          | Boot select button                          | Used for entering UART download mode |
| **GPIO4** | SS_SD               | SPI Chip Select for SD card                 | microSD card                          |
| **GPIO6** | SCK                 | SPI Clock                                   | Shared SPI (e-Paper + SD)            |
| **GPIO7** | MOSI                | SPI Data Out                                | Shared SPI (e-Paper + SD)            |
| **GPIO2** | MISO                | SPI Data In                                 | SD card only                          |
| **GPIO5** | EPD_DC              | Data/Command pin for e-paper display        | e-Paper display                       |
| **GPIO10** | EPD_CS              | Chip Select for e-paper display             | e-Paper display                       |
| **GPIO3** | EPD_BUSY            | Busy pin input from e-paper display         | e-Paper display                       |
| **GPIO11** | FLASH_CS            | Flash chip select (internal flash)          | Reserved – do not use externally     |
| **GPIO13**| USB D+              | USB 2.0 Full Speed Data+                    | USB-C Interface                       |
| **GPIO12**| USB D-              | USB 2.0 Full Speed Data-                    | USB-C Interface                       |
| **GPIO16**| TX                  | UART TX (console/debug)                     | Optional serial logging               |
| **GPIO17**| RX                  | UART RX (console/debug)                     | Optional serial logging               |
| **GPIO18**| RTC_RST             | RTC reset                                   | DS3231 (RTC)                          |
| **GPIO0**| INT_RTC             | RTC interrupt/alarm                         | DS3231 optional alarm/interrupt       |
| **GPIO21**| SDA                 | I2C Data Line                                | Shared between RTC, BME688, MAX17048 |
| **GPIO22**| SCL                 | I2C Clock Line                               | Shared between RTC, BME688, MAX17048 |
| **GPIO20**| EPD_3V3_C           | Power control / enable for e-paper display  | Can be used for low-power control     |
| **GPIO23**| EPD_RST    | Redundant label for GPIO8                   | See GPIO8 (same net)                  |

---

# PCB Design and Mechanical Integration

The OpenBook PCB has been designed as a compact, two-layer board with careful attention to power integrity, signal routing, and EMI minimization. Components are placed for thermal efficiency and optimal antenna performance.
- The /Hardware directory contains the original KiCad schematic (.sch) and PCB layout (.brd) files for further modification or inspection.
- High-quality 3D renderings of the PCB and complete device are available in the /Images folder.
- 3D models of the enclosure, including exploded views and Fusion 360 assemblies, can be found in /Mechanical.
- The /Manufacturing folder includes production-ready files such as Gerbers, BOM and Pick & Place data for automated assembly.

---