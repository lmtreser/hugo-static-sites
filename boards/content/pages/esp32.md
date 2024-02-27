---
title: "Expressif ESP32 Arduino Core"
date: 2024-02-24T10:49:32-03:00
draft: false
ShowToC : true
weight: 2
---

En este tutorial veremos cómo configurar el IDE de Arduino para poder programar placas basadas en el SoC **ESP32**.
<!--more-->

https://en.m.wikipedia.org/wiki/ESP32

### Supported Chips

Here are the ESP32 series supported by the Arduino-ESP32 project:

| **SoC**  | **Stable** | **Development** |                                           **Datasheet**                                           |
|----------|:----------:|:---------------:|:-------------------------------------------------------------------------------------------------:|
| ESP32    |     Yes    |       Yes       |    [ESP32](https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf)    |
| ESP32-S2 |     Yes    |       Yes       | [ESP32-S2](https://www.espressif.com/sites/default/files/documentation/esp32-s2_datasheet_en.pdf) |
| ESP32-C3 |     Yes    |       Yes       | [ESP32-C3](https://www.espressif.com/sites/default/files/documentation/esp32-c3_datasheet_en.pdf) |
| ESP32-S3 |     Yes    |       Yes       | [ESP32-S3](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf) |
| ESP32-C6 |     No     |       Yes       | [ESP32-C6](https://www.espressif.com/sites/default/files/documentation/esp32-c6_datasheet_en.pdf) |
| ESP32-H2 |     No     |       Yes       | [ESP32-H2](https://www.espressif.com/sites/default/files/documentation/esp32-h2_datasheet_en.pdf) |

For more details visit the [supported chips](https://docs.espressif.com/projects/arduino-esp32/en/latest/getting_started.html#supported-soc-s) documentation page.


## Instalación 

> Este tutorial está realizado con la versión 2.3.2 de Arduino IDE, aunque el procedimiento es similar para versiones anteriores.

Para poder instalar el Core ESP32 debemos seguir los mismos pasos explicados en el tutorial [Expressif ESP8266 Arduino Core](../esp8266/) con una diferencia: en la ventana `URLs adicionales de gestor de placas` debemos agregar la siguiente línea:

```sh
https://espressif.github.io/arduino-esp32/package_esp32_index.json
```
Luego, en el `Gestor de placas` buscaremos el Core ESP32 como `esp32` para instalarlo.

![](../img/esp32.gif)

Una vez finalizado el proceso, desde el menú `Herramientas » Placa » esp32` podremos acceder al listado de placas soportado.

## Recursos

- [Arduino core for the ESP32 ](https://github.com/espressif/arduino-esp32)
- [ESP32 Arduino Core’s documentation](https://docs.espressif.com/projects/arduino-esp32/en/latest/index.html)
- [Unofficial list of 3rd party boards support urls](https://github.com/arduino/Arduino/wiki/Unofficial-list-of-3rd-party-boards-support-urls)