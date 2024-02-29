---
title: "Instalación de Bibliotecas"
date: 2024-02-24T10:49:34-03:00
draft: false
weight: 1
---
Instalar una biblioteca es un proceso rápido y fácil, en este tutorial repasaremos las formas de hacerlo.

{{< toc >}}

## Instalación desde Arduino IDE

> Esta documentación es una traducción parcial de la documentación oficial de Arduino, disponible en [GitHub](https://github.com/arduino/docs-content/). La versión del IDE es la 2, aunque el proceso es similar en versiones anteriores.

El primer paso es abrir Arduino IDE v2. Con el editor abierto, hay que hacer clic en el icono `Biblioteca` que se encuentra en la columna izquierda para acceder al `GESTOR DE BIBLIOTECAS`.

<p align="center">
    <img src="../img/installing-a-library-img01.png">
</p>

Aparecerá una lista de todas las bibliotecas disponibles, donde podremos buscar la biblioteca que queremos utilizar. En este ejemplo, instalaremos la biblioteca **RTCZero**. Para esto, hay que hacer clic en el botón `INSTALAR` para descargar e instalar la biblioteca.

<p align="center">
    <img src="../img/installing-a-library-img02.png">
</p>

El proceso no debería llevar demasiado tiempo, pero permite hasta un minuto para realizarlo.

<p align="center">
    <img src="../img/installing-a-library-img03.png">
</p>

Una vez finalizado el proceso, podemos corroborar el estado viendo la leyenda `instalado` junto a la versión de la biblioteca.

<p align="center">
    <img src="../img/installing-a-library-img04.png">
</p>

## Instalación Manual

En el caso de descargar una biblioteca de forma externa al Arduino IDE, la forma de instalación difiere a de los pasos anteriores. 

Por ejemplo, si accedemos a una biblioteca que esta alojada en GitHub, podremos descargar el código en un archivo ZIP. En este ejemplo instalaremos la biblioteca Robotec: accedemos al [repositorio](https://github.com/lmtreser/Robotec), luego descargamos el código haciendo clic en el botón `<> Code`, opción `Download ZIP`.

<p align="center">
    <img src="../img/gh_descarga.png">
</p>

Una vez que el archivo se encuentra en nuestra computadora, en el Arduino IDE, hay que hacer clic en `Sketch » Incluir biblioteca » Añadir biblioteca .ZIP...`.

<p align="center">
    <img src="../img/archivo_zip.png">
</p>

## Recursos

- [Arduino Libraries](https://www.arduino.cc/reference/en/libraries/)
- [Cómo instalar una librería de Arduino en el entorno de desarrollo](https://programarfacil.com/blog/arduino-blog/instalar-una-libreria-de-arduino/)
- [Installing libraries](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-installing-a-library/)