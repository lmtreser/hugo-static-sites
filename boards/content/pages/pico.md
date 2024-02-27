---
title: "Raspberry Pi Pico Arduino Core"
date: 2024-02-24T10:49:34-03:00
draft: false
ShowToC : true
weight: 3
---

En este tutorial veremos cómo configurar el IDE de Arduino para poder programar las placas de Raspberry Pi **Pico** y **Pico W**, y otras tantas basadas en el microcontrolador RP2040.
<!--more-->
El **RP2040** es un microcontrolador dual-core ARM Cortex-M0+ 32 bits de Raspberry Pi Ltd. En enero de 2021, se lanzó como parte de la placa Raspberry Pi Pico. [Más en Wikipedia](https://en.m.wikipedia.org/wiki/RP2040).

![](../img/rp2040.png#center)

## Especificaciones

- Procesador Arm Cortex-M0+ de doble núcleo
- Reloj flexible que funciona hasta 133 MHz
- SRAM 264 kB
- UART × 2, SPI × 2, I2C × 2, PWM × 16
- Controlador USB 1.1
- Programmable I/O (PIO) × 8
- Sensor de temperatura

## Instalación del Raspberry Pi Pico Arduino Core

> Este tutorial está realizado con la versión 2.3.2 de Arduino IDE, aunque el procedimiento es similar para versiones anteriores.

Para poder instalar el Raspberry Pi Pico Core de [Earle F. Philhower, III](mailto:earlephilhower@yahoo.com) debemos seguir los mismos pasos explicados en el tutorial [Expressif ESP8266 Arduino Core](../esp8266/) con una diferencia: en la ventana `URLs adicionales de gestor de placas` debemos agregar la siguiente línea:

```sh
https://github.com/earlephilhower/arduino-pico/releases/download/global/package_rp2040_index.json
```

Luego, en el `Gestor de placas` buscaremos el Raspberry Pi Pico Arduino core como `pico` para instalarlo.

![](../img/pico.gif#center)

Una vez finalizado el proceso, desde el menú `Herramientas » Placa » Raspberry Pi Pico/RP2040` podremos acceder al listado de placas soportado.

## Placas soportadas

|                               |                               |                               |
|-------------------------------|-------------------------------|-------------------------------|
| Raspberry Pi Pico             | Raspberry Pi Pico W           | 0xCB Helios                   |
| Adafruit Feather RP2040       | Adafruit Feather RP2040 SCORPIO | Adafruit ItsyBitsy RP2040  |
| Adafruit KB2040               | Adafruit Macropad RP2040      | Adafruit Metro RP2040        |
| Adafruit QTPy RP2040          | Adafruit STEMMA Friend RP2040 | Adafruit Trinkey RP2040 QT   |
| Arduino Nano RP2040 Connect   | ArtronShop RP2 Nano           | BridgeTek IDM2040-7A          |
| Cytron Maker Pi RP2040        | Cytron Maker Nano RP2040      | Cytron Maker Uno RP2040       |
| DatanoiseTV PicoADK+          | Degz Suibo RP2040            | DeRuiLab FlyBoard2040 Core   |
| DFRobot Beetle RP2040         | ElectronicCats Hunter Cat NFC | ExtremeElectronics RC2040     |
| Invector Labs Challenger RP2040 WiFi | Invector Labs Challenger RP2040 WiFi/BLE | Invector Labs Challenger RP2040 WiFi6/BLE |
| Invector Labs Challenger NB RP2040 WiFi | Invector Labs Challenger RP2040 LTE | Invector Labs Challenger RP2040 LoRa |
| Invector Labs Challenger RP2040 SubGHz | Invector Labs Challenger RP2040 SD/RTC | Invector Labs Challenger RP2040 UWB |
| Invector Labs RPICO32         | Melopero Cookie RP2040       | Melopero Shake RP2040        |
| Neko Systems BL2040 Mini      | nullbits Bit-C PRO            | Pimoroni PGA2040              |
| Pimoroni Plasma2040           | Pimoroni Tiny2040             | RAKwireless RAK11300          |
| Redscorp RP2040-Eins          | Redscorp RP2040-ProMini       | Sea-Picro                     |
| Seeed Indicator RP2040        | Seeed XIAO RP2040            | Silicognition RP2040-Shim     |
| Solder Party RP2040 Stamp     | SparkFun ProMicro RP2040     | SparkFun Thing Plus RP2040    |
| uPesy RP2040 DevKit           | VCC-GND YD-RP2040            | Viyalab Mizu RP2040           |
| Waveshare RP2040 Zero         | Waveshare RP2040 One         | Waveshare RP2040 Plus         |
| Waveshare RP2040 LCD 0.96     | Waveshare RP2040 LCD 1.28    | WIZnet W5100S-EVB-Pico        |
| WIZnet W5500-EVB-Pico         | WIZnet WizFi360-EVB-Pico     | Generic (configurable flash, I/O pins) |

## Recursos

- [Documentation for the Raspberry Pi Pico Arduino core](https://arduino-pico.readthedocs.io/en/latest/)
- [Raspberry Pi Pico Arduino core, for all RP2040 boards](https://github.com/earlephilhower/arduino-pico/)