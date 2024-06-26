---
title: "El Preprocesador de C"
date: 2024-06-06T08:00:00-03:00
draft: false
weight: 2
---
El preprocesador de C es el preprocesador para el lenguaje de programación C. Es el primer programa invocado por el compilador y procesa directivas como `#include`, `#define` e `#if`. Estas directivas no son específicas de C. En realidad pueden ser usadas con cualquier tipo de archivo.

{{< toc >}}

## Fases

El preprocesador utiliza 4 etapas denominadas **Fases de traducción**. Aunque alguna implementación puede elegir hacer alguna o todas las fases simultáneamente, debe comportarse como si fuesen ejecutadas paso a paso.

1. Tokenizado léxico. El preprocesador reemplaza la secuencia de trigrafos por los caracteres que representan.

2. Empalmado de líneas. Las líneas de código que continúan con secuencias de escape de nueva línea son unidas para formar líneas lógicas.

3. Tokenización. Reemplaza los comentarios por espacios en blanco. Divide cada uno de los elementos a preprocesar por un carácter de separación.

4. Expansión de macros y gestión de directivas. Ejecuta las líneas con directivas de preprocesado incluyendo las que incluye otros archivos y las de compilación condicional. Además expande las macros. Desde la versión de C de 1999 también gestiona los operadores `#Pragma`.

## Instrucciones Básicas del Preprocesador

Inclusión de archivos:

- `#include <file>`: Incluye un archivo de cabecera estándar.
- `#include "file"`: Incluye un archivo de cabecera del proyecto.

Definición de macros:

- `#define NAME value`: Define una macro.
- `#define NAME(args) code`: Define una macro con argumentos.

Eliminación de definiciones:

- `#undef NAME`: Elimina la definición de una macro.

Control condicional de compilación:

- `#ifdef NAME`: Compila el código si la macro NAME está definida.
- `#ifndef NAME`: Compila el código si la macro NAME no está definida.
- `#if expression`: Compila el código si la expresión es verdadera.
- `#elif expression`: "Else if" para `#if`.
- `#else`: Compila el código si ninguna de las condiciones anteriores se cumple.
- `#endif`: Finaliza una estructura condicional.

Macros predefinidas:

- `__DATE__`: Fecha de compilación (en formato "MMM DD YYYY").
- `__TIME__`: Hora de compilación (en formato "HH:MM:SS").
- `__FILE__`: Nombre del archivo fuente actual.
- `__LINE__`: Número de línea en el archivo fuente actual.
- `__func__`: Nombre de la función actual (C99 y C++11 en adelante).
- `__cplusplus`: Definido cuando el código se compila como C++.

Directivas de línea:

- `#line number`: Cambia el número de línea del código.
- `#line number "filename"`: Cambia el número de línea y el nombre del archivo.

Otros:

- `#error message`: Genera un mensaje de error durante la compilación.
- `#pragma directive`: Emite directivas específicas del compilador.

## Pragmas

Los **pragmas** son directivas especiales que controlan el comportamiento del compilador. Tienen esta forma estándar:

```c
pragma Nombre (lista_de_argumentos);
```

`#pragma` es una directiva que se utiliza en C y C++ para ofrecer información adicional al compilador, más allá de lo que está disponible en el lenguaje estándar. Los pragmas son específicos del compilador. Es decir, un pragma diseñado para un compilador puede no funcionar en otro. El uso de #pragma puede hacer que el código sea menos portátil, ya que los pragmas son específicos del compilador.

Por ejemplo, *pragma once* se utiliza para asegurar que un archivo de encabezado se incluya una sola vez durante la compilación. Esto ayuda a prevenir la duplicación de definiciones.

```c
#pragma once
// Código de encabezado aquí
```

## Ejemplos

Inclusión de archivos:

```c
#include <stdio.h>    // Archivo de cabecera estándar
#include "miarchivo.h" // Archivo de cabecera del proyecto
```

Definición y uso de macros:

```c
#define PI 3.14159
#define CIRCUNFERENCIA(r) (2 * PI * (r))

double circunferencia = CIRCUNFERENCIA(5); // Usa la macro
```

Control condicional de compilación:

```c
#ifdef DEBUG
    printf("Modo de depuración activado\n");
#endif

#ifndef VERSION
    #define VERSION "1.0"
#endif

#if __STDC_VERSION__ >= 199901L
    // Código específico para C99 o posterior
#else
    // Código para versiones anteriores de C
#endif
```

Directivas de línea:

```c
#line 100 "nuevo_archivo.c"
printf("Esto está en la línea 100 de nuevo_archivo.c\n");
```

Mensajes de error y pragma:
```c
#error "Este es un error de prueba"

#pragma once // Previene inclusiones múltiples en algunos compiladores
```

## Ejemplos Arduino

Incluir una biblioteca u otra dependiendo del hardware a compilar:

```c
#ifndef ESPWEBCFG_H
#define ESPWEBCFG_H

#ifdef ESP8266
    #include <ESP8266WebServer.h>
    #include <ESP8266WiFi.h>
#elif defined(ESP32)
    #include <WiFi.h>
    #include <WebServer.h>
#endif
```

Añadir instrucciones específicas para un modelo de placa u otro:

```c
#if defined(ARDUINO_AVR_UNO)
  // Código específico para Arduino Uno
  pinMode(13, OUTPUT);
#elif defined(ARDUINO_AVR_MEGA2560)
  // Código específico para Arduino Mega
  pinMode(53, OUTPUT);
#endif
```

Si existe la definición, añadir instrucciones específicas:

```c
#define ENABLE_DEBUG 1  // DEBUG por Serial, 1=activado
#if ENABLE_DEBUG
  Serial.println("Mensaje");
#endif
```

## Manuales

- [The C Preprocessor](../pdf/pre/The_C_Preprocessor.pdf)

## Recursos

- [Preprocesador de C](https://es.wikipedia.org/wiki/Preprocesador_de_C)
