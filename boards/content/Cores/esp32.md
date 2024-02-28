---
title: "Expressif ESP32 Arduino Core"
date: 2024-02-24T10:49:32-03:00
draft: false
weight: 2
---
En este tutorial veremos cómo configurar el IDE de Arduino para poder programar placas basadas en el SoC **ESP32**.

{{< toc >}}

**ESP32** es la denominación de una familia de chips de bajo costo, con tecnología Wi-Fi y Bluetooth integrada. El ESP32 emplea un CPU Tensilica Xtensa LX6 en sus variantes de simple y doble núcleo. Fue creado y desarrollado por Espressif Systems y es fabricado por TSMC utilizando su proceso de 40 nm. [Más en Wikipedia](https://en.m.wikipedia.org/wiki/ESP32).

<p align="center">
    <img src="../img/esp32.png">
</p>

## Especificaciones

- Microprocesador de 32-bit Xtensa LX6 de doble núcleo (o de un solo núcleo), corriendo a 160 ó 240 MHz
- SRAM 520 KiB 
- Wi-Fi 802.11 b/g/n
- Bluetooth v4.2 BR/EDR y BLE
- 12-bit SAR ADC de hasta 18 canales
- 2 × 8-bit DACs
- 10 × sensores de tacto
- SPI × 4, I2S × 2, I2C × 2, UART × 3
- Controlador host SD/SDIO/CE-ATA/MMC/eMMC
- Controlador esclavo SDIO/SPI

## Instalación del Expressif ESP32 Arduino Core

> Este tutorial está realizado con la versión 2.3.2 de Arduino IDE, aunque el procedimiento es similar para versiones anteriores.

Para poder instalar el Core ESP32 debemos seguir los mismos pasos explicados en el tutorial [Expressif ESP8266 Arduino Core](../esp8266/) con una diferencia: en la ventana `URLs adicionales de gestor de placas` debemos agregar la siguiente línea:

```sh
https://espressif.github.io/arduino-esp32/package_esp32_index.json
```
Luego, en el `Gestor de placas` buscaremos el Core ESP32 como `esp32` para instalarlo.

![](../img/esp32.gif)

Una vez finalizado el proceso, desde el menú `Herramientas » Placa » esp32` podremos acceder al listado de placas soportado.

## Chips soportados

A continuación la lista de la serie ESP32 compatible con el proyecto Arduino-ESP32. Más detalles en [supported chips](https://docs.espressif.com/projects/arduino-esp32/en/latest/getting_started.html#supported-soc-s):

| **SoC**  | **Stable** | **Development** |                                           **Datasheet**                                           |
|----------|:----------:|:---------------:|:-------------------------------------------------------------------------------------------------:|
| ESP32    |     Yes    |       Yes       |    [ESP32](https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf)    |
| ESP32-S2 |     Yes    |       Yes       | [ESP32-S2](https://www.espressif.com/sites/default/files/documentation/esp32-s2_datasheet_en.pdf) |
| ESP32-C3 |     Yes    |       Yes       | [ESP32-C3](https://www.espressif.com/sites/default/files/documentation/esp32-c3_datasheet_en.pdf) |
| ESP32-S3 |     Yes    |       Yes       | [ESP32-S3](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf) |
| ESP32-C6 |     No     |       Yes       | [ESP32-C6](https://www.espressif.com/sites/default/files/documentation/esp32-c6_datasheet_en.pdf) |
| ESP32-H2 |     No     |       Yes       | [ESP32-H2](https://www.espressif.com/sites/default/files/documentation/esp32-h2_datasheet_en.pdf) |

## Placas soportadas

|  |  |   |
|--|--|---|
4D Systems gen4-ESP32 16MB Modules (ESP32-S3R8n16) | FireBeetle 2 ESP32-E | OLIMEX ESP32-EVB
Adafruit ESP32 Feather | FireBeetle-ESP32 | OLIMEX ESP32-GATEWAY
Adafruit Feather ESP32 V2 | Franzininho WiFi | OLIMEX ESP32-H2-DevKit-LiPo
Adafruit Feather ESP32-S2 | Franzininho WiFi MSC | OLIMEX ESP32-POE
Adafruit Feather ESP32-S2 Reverse TFT | Frog Board ESP32 | OLIMEX ESP32-POE-ISO
Adafruit Feather ESP32-S2 TFT | Geekble ESP32-C3 | OLIMEX ESP32-S2-DevKit-Lipo
Adafruit Feather ESP32-S3 2MB PSRAM | Heltec WiFi Kit 32 | OLIMEX ESP32-S2-DevKit-Lipo-USB
Adafruit Feather ESP32-S3 No PSRAM | Heltec WiFi Kit 32(V3) | OLIMEX ESP32-S3-DevKit-Lipo
Adafruit Feather ESP32-S3 Reverse TFT | Heltec WiFi LoRa 32 | OLIMEX ESP32-SBC-FABGL
Adafruit Feather ESP32-S3 TFT | Heltec WiFi LoRa 32(V2) | Onehorse ESP32 Dev Module
Adafruit FunHouse | Heltec WiFi LoRa 32(V3) / Wireless shell(V3) / Wireless stick lite (V3) | OROCA EduBot
Adafruit ItsyBitsy ESP32 | Heltec Wireless Stick | Piranha ESP-32
Adafruit MagTag 2.9 | Heltec Wireless Stick Lite | ProtoCentral HealthyPi 4
Adafruit MatrixPortal ESP32-S3 | Heltec Wireless Tracker | Pycom GPy
Adafruit Metro ESP32-S2 | HONEYLemon | RedPill(+) ESP32-S3
Adafruit Metro ESP32-S3 | Hornbill ESP32 Dev | RoboHeart Hercules
Adafruit pyCamera S3 | Hornbill ESP32 Minima | S.ODI Ultra v1
Adafruit QT Py ESP32 | IMBRIOS LOGSENS_V1P1 | senseBox MCU-S2 ESP32-S2
Adafruit QT Py ESP32-C3 | INEX OpenKB | Senses's WEIZEN
Adafruit QT Py ESP32-S2 | IntoRobot Fig | Silicognition wESP32
Adafruit QT Py ESP32-S3 (4M Flash 2M PSRAM) | IOXESP32 | Sonoff DUALR3
Adafruit QT Py ESP32-S3 No PSRAM | IOXESP32PS | SparkFun ESP32 IoT RedBoard
Adafruit Qualia ESP32-S3 RGB666 | KB32-FT | SparkFun ESP32 MicroMod
AI Thinker ESP32-CAM | KITS ESP32 EDU | SparkFun ESP32 Thing
AirM2M_CORE_ESP32C3 | Labplus mPython | SparkFun ESP32 Thing Plus
ALKS ESP32 | LilyGo T-Display | SparkFun ESP32 Thing Plus C
Arduino Nano ESP32 | LilyGo T-Display-S3 | SparkFun ESP32-C6 Qwiic Pocket
Arduino on Nano ESP32 | Lion:Bit Dev Board | SparkFun ESP32-C6 Thing Plus
ATD1.47-S3 | Lion:Bit S3 STEM Dev Board | SparkFun ESP32-S2 Thing Plus
ATMegaZero ESP32-S2 | LOLIN C3 Mini | SparkFun LoRa Gateway 1-Channel
Aventen S3 Sync | LOLIN D32 | SparkFun Pro Micro - ESP32C3
Bee Data Logger | LOLIN D32 PRO | T-Beam
Bee Motion | LOLIN S2 Mini | TAMC Termod S3
Bee Motion Mini | LOLIN S2 PICO | ThaiEasyElec's ESPino32
Bee Motion S3 | LOLIN S3 | ThingPulse ePulse Feather
Bee S3 | LOLIN S3 Mini | Trueverit ESP32 Universal IoT Driver
BPI-BIT | LOLIN S3 Pro | Trueverit ESP32 Universal IoT Driver MK II
BPI-Leaf-S3 | LoPy | TTGO LoRa32-OLED
CNRS AW2ETH | LoPy4 | TTGO T-OI PLUS RISC-V ESP32-C3
Connaxio's Espoir | M5Atom | TTGO T-Watch
Crabik Slot ESP32-S3 | M5AtomS3 | TTGO T1
Cytron Maker Feather AIoT S3 | M5Capsule | TTGO T7 V1.3 Mini32
D-duino-32 | M5Cardputer | TTGO T7 V1.4 Mini32
Deneyap Kart | M5Core | Turta IoT Node
Deneyap Kart 1A | M5Core2 | u-blox NINA-W10 series (ESP32)
Deneyap Kart 1A v2 | M5CoreInk | u-blox NORA-W10 series (ESP32-S3)
Deneyap Kart G | M5CoreS3 | UM BLING
Deneyap Mini | M5Dial | UM FeatherS2
Deneyap Mini v2 | M5Fire | UM FeatherS2 Neo
Denky | M5Paper | UM FeatherS3
Department of Alchemy MiniMain ESP32-S2 | M5PoECAM | UM NanoS3
DFRobot Beetle ESP32-C3 | M5StampC3 | UM PROS3
DFRobot Beetle ESP32-C6 | M5StampPico | UM RMP
DFRobot FireBeetle 2 ESP32-C6 | M5StampS3 | UM TinyC6
DFRobot Firebeetle 2 ESP32-S3 | M5Station | UM TinyPICO
DFRobot Romeo ESP32-S3 | M5StickC | UM TinyS2
DOIT ESP32 DEVKIT V1 | M5StickCPlus | UM TinyS3
DOIT ESPduino32 | M5StickCPlus2 | unPhone 7
Dongsen Tech Pocket 32 | M5TimerCAM | unPhone 8
DPU ESP32 | M5Tough | unPhone 9
Edgebox-ESP-100 | M5UnitCAM | uPesy EDU ESP32
Electronic SweetPeas - ESP320 | M5UnitCAMS3 | uPesy ESP32 Wroom DevKit
ESP-C3-M1-I-Kit | MagicBit | uPesy ESP32 Wrover DevKit
ESP32 Dev Module | MakerGO ESP32 C3 SuperMini | uPesy ESP32C3 Basic
ESP32 FM DevKit | Metro ESP-32 | uPesy ESP32C3 Mini
ESP32 PICO-D4 | MGBOT IOTIK 32A | uPesy ESP32S3 Basic
ESP32 Wrover Kit (all versions) | MGBOT IOTIK 32B | VALTRACK_V4_MFW_ESP32_C3
ESP32 Wrover Module | MH ET LIVE ESP32DevKIT | VALTRACK_V4_VTS_ESP32_C3
ESP32-S3 PowerFeather | MH ET LIVE ESP32MiniKit | VintLabs ESP32 Devkit
ESP32-S3-Box | Microduino-CoreESP32 | Watchy
ESP32-S3-USB-OTG | microS2 | WEMOS D1 MINI ESP32
ESP32-WROOM-DA Module | Namino Arancio | WEMOS D1 R32
ESP32C2 Dev Module | Namino Bianco | WEMOS LOLIN32
ESP32C3 Dev Module | Namino Rosso | WEMOS LOLIN32 Lite
ESP32C6 Dev Module | Nano32 | WeMos WiFi&Bluetooth Battery
ESP32H2 Dev Module | Nebula S3 | Widora AIR
ESP32S2 Dev Module | Node32s | WiFiduino32
ESP32S2 Native USB | NodeMCU-32S | WiFiduino32S3
ESP32S3 CAM LCD | Noduino Quantum | WiFiduinoV2
ESP32S3 Dev Module | Nologo ESP32C3 Super Mini | WiPy 3.0
ESP32S3 Dev Module Octal (WROOM2) | Nologo ESP32S3 Pico | WT32-ETH01 Ethernet Module
ESP32vn IoT Uno | ODROID ESP32 | WT32-SC01 PLUS
ESPea32 | OLIMEX ESP32-C3-DevKit-Lipo | XIAO_ESP32C3
ESPectro32 | OLIMEX ESP32-C6-EVB | XIAO_ESP32S3
ET-Board | OLIMEX ESP32-DevKit-LiPo | XinaBox CW02

## Recursos

- [Arduino core for the ESP32 ](https://github.com/espressif/arduino-esp32)
- [ESP32 Arduino Core’s documentation](https://docs.espressif.com/projects/arduino-esp32/en/latest/index.html)