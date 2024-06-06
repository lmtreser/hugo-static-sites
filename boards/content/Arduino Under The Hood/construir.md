---
title: "Construir un Arduino"
date: 2024-06-06T08:00:00-03:00
draft: false
weight: 4
---
Muchas veces iniciamos un proyecto experimentando y probando cosas con nuestra placa Arduino y una protoboard. Luego las cosas se ponen un poco más serias y es necesario dar un paso más, por ejemplo fabricando un circuito impreso o *shield* para contener todos los componentes adicionales al Arduino. En este artículo veremos como construir un Arduino Uno a medida, es decir, bajo nuestros requerimientos.

{{< toc >}}

## Arduino Breadboard

Investigando en Internet bajo los términos [Arduino Breadboard](https://docs.arduino.cc/built-in-examples/arduino-isp/ArduinoToBreadboard/) o [Arduino Standalone](https://docs.arduino.cc/retired/hacking/hardware/building-an-arduino-on-a-breadboard/) encontraremos muchos proyectos para montar una placa Arduino. El circuito mínimo se basa en un microcontrolador **ATMEGA328-PU**, un cristal de 16MHz, dos capacitores cerámicos y una resistencia.

<p align="center">
    <img src="../img/arduinocustom.png">
</p>

## Fuente de alimentación

La placa Arduino a medida funciona con 5 V de corriente continua, por lo que será necesario contar con un regulador de tensión para poder alimentarla desde una batería de 9 V o una fuente. Este montaje utiliza el [regulador lineal LM7805](../pdf/LM7805.pdf) junto a algunos componentes más:

<p align="center">
    <img src="../img/Regulador.png">
</p>

Una vez realizadas todas las conexiones de la fuente de alimentación es importante comprobar que no existan cortocircuitos o problemas de soldadura. Hay que probar con un multímetro que la polaridad y la tensión sean correctas antes de conectar el microcontrolador.

## Cargando el bootloader

Una vez que el hardware está terminado, es hora de cargar el **bootloader**. Un microcontrolador generalmente se programa a través de un dispositivo programador, a menos que tenga en su memoria un pequeño *firmware* que permita instalar un nuevo programa sin la necesidad de un programador externo. Esta es la función del bootloader o gestor de arranque.

Para cargar el bootloader se necesita una placa Arduino Uno a la que se le debe subir el sketch **ArduinoISP**. Para hacer esto, abrir el sketch desde el menú **Archivo > Ejemplos > 11. ArduinoISP > ArduinoISP**.

El siguiente paso será conectar la placa Arduino Uno a la placa Arduino «a medida».

<p align="center">
    <img src="../img/004.png">
</p>

Ahora es necesario cambiar el programador. Ir al menú **Herramientas > Programador** y elegir la opción **Arduino as ISP**. Volver al menú **Herramientas** y elegir la opción **Quemar Bootloader**. ¡Listo!

## Problemas al cargar el bootloader

Puede ocurrir que al intentar cargar el bootloader, el IDE de Arduino informe sobre un error de firma y no permita continuar con el proceso.

<p align="center">
    <img src="../img/error.png">
</p>

En este caso ocurrió debido a que el microcontrolador que se está utilizando es el ATMEGA328-PU y el que utiliza la placa Arduino Uno es el **ATMEGA328P-PU**. La gran diferencia entre uno y otro es el consumo de energía. Para poder continuar hay que engañar al IDE modificando el archivo **avrdude.conf**.

- Buscar y abrir la carpeta en la que está instalado Arduino IDE, luego navegar hasta la subcarpeta `\hardware\tools\avr\etc`.
- Hacer una copia de respaldo del archivo `avrdude.conf`.
- Abrir el archivo `avrdude.conf` en un editor de texto.
- Buscar `0x1e 0x95 0x0F`, que es la firma ATMEGA328P.
- Reemplazarla por `0x1e 0x95 0x14` (esta es la firma ATMEGA328).
- Guardar el archivo.
- Reiniciar el IDE de Arduino.
- Continuar grabando el bootloader, y una vez que se complete la carga, restaurar la copia de seguridad.

<p align="center">
    <img src="../img/003.png">
</p>

## Conexión USB-TTL

Para cargar un sketch deberemos utilizar un adaptador USB-TTL y conectarlo de la siguiente manera:

<p align="center">
    <img src="../img/005.png">
</p>

## Manuales

- [Arduino por dentro: ¿Cómo hago un Arduino?](../pdf/hacer_un_Arduino.pdf)

## Recursos

- [Arduino «a medida»](https://www.automatismos-mdq.com.ar/blog/2020/05/arduino-a-medida.html)
- [AVRDUDE - AVR Downloader/UploaDEr](https://avrdude.nongnu.org/)
- [AVRDUDE](https://github.com/avrdudes/avrdude/)
- [AVRDUDESS – A GUI for AVRDUDE](https://blog.zakkemble.net/avrdudess-a-gui-for-avrdude/)
- [Exportar binarios compilados en Arduino](https://www.youtube.com/watch?v=LLErbNB8r-A)
- [AVRdudess + USBasp](https://www.youtube.com/watch?v=PakKqgLicos)
