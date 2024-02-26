---
title: "Raspberry Pi Pico Arduino Core"
date: 2024-02-24T10:49:34-03:00
draft: false
weight: 3
---

En este tutorial veremos cómo configurar el IDE de Arduino para poder programar las placas de Raspberry Pi **Pico** y **Pico W**, y otras tantas basadas en el microcontrolador RP2040.
<!--more-->
> Este tutorial está realizado con la versión 2.3.2 de Arduino IDE, aunque el procedimiento es similar para versiones anteriores.

Para poder instalar el Raspberry Pi Pico Core debemos seguir los mismos pasos explicados en el tutorial [Expressif ESP8266 Arduino Core](../esp8266/) con una diferencia: en la ventana `URLs adicionales de gestor de placas` debemos agregar la siguiente línea:

```sh
https://github.com/earlephilhower/arduino-pico/releases/download/global/package_rp2040_index.json
```

Luego, en el `Gestor de placas` buscaremos el Raspberry Pi Pico Arduino core como `pico` para instalarlo.

![](../img/pico.gif#center)

Una vez finalizado el proceso, desde el menú `Herramientas » Placa » Raspberry Pi Pico/RP2040` podremos acceder al listado de placas soportado.

## Recursos

- [Documentation for the Raspberry Pi Pico Arduino core](https://arduino-pico.readthedocs.io/en/latest/)
- [Raspberry Pi Pico Arduino core, for all RP2040 boards](https://github.com/earlephilhower/arduino-pico/)
- [Unofficial list of 3rd party boards support urls](https://github.com/arduino/Arduino/wiki/Unofficial-list-of-3rd-party-boards-support-urls)