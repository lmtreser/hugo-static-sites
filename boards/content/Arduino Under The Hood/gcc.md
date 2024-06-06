---
title: "GNU Compiler Collection"
date: 2024-06-06T08:00:00-03:00
draft: false
weight: 1
---
El GNU Compiler Collection (colección de compiladores GNU) es un conjunto de compiladores creados por el proyecto GNU. GCC es software libre y lo distribuye la Free Software Foundation (FSF) bajo la licencia general pública GPL.

{{< toc >}}

Estos compiladores se consideran estándar para los sistemas operativos derivados de UNIX, de código abierto y también de propietarios, como Mac OS X. GCC requiere el conjunto de aplicaciones conocido como *binutils* para realizar tareas como identificar archivos objeto u obtener su tamaño para copiarlos, traducirlos o crear listas, enlazarlos, o quitarles símbolos innecesarios.

Originalmente GCC significaba GNU C Compiler (compilador GNU de C), porque solo compilaba el lenguaje C. Posteriormente se extendió para compilar C++, Fortran, Ada y otros.

<p align="center">
    <img src="../img/Gcc-4.2.0.png">
</p>

## Proceso de compilación de GCC

GCC compila un programa C/C++ en un ejecutable en 4 pasos como se muestra en el siguiente diagrama.

<p align="center">
    <img src="../img/GCC_CompilationProcess.png">
</p>

Por ejemplo, un «gcc -o hello.exe hello.c» se realiza de la siguiente manera:

Preprocesamiento: a través del preprocesador GNU C (`cpp.exe`), que incluye las cabeceras `#include` y expande las macros `#define`. El archivo intermedio resultante `hello.i` contiene el código fuente expandido.

```c
cpp hello.c > hello.i
```

Compilación: el compilador compila el código fuente preprocesado en código ensamblador para un procesador específico. La opción `-S` especifica producir código ensamblador, en lugar de código objeto. El archivo de ensamblaje resultante es `hello.s`.

```c
gcc -S hello.i
```

Ensamblado: el ensamblador (`as.exe`) convierte el código ensamblador en código máquina en el fichero objeto `hello.o`.

```c
as -o hello.o hello.s
```

Enlazador: finalmente, el enlazador (`ld.exe`) enlaza el código objeto con el código de la biblioteca para producir un archivo ejecutable `hello.exe`.

```c
ld -o hello.exe hello.o ...libraries...
```

## El proceso de compilación un programa Arduino

El proceso de compilación un programa Arduino involucra varios pasos:

1. *Preprocesamiento*: En esta fase, el preprocesador de C/C++ maneja las directivas de preprocesamiento, como `#include` y `#define`. Los archivos `.ino` de Arduino son concatenados en un solo archivo `.cpp` y se añade automáticamente `#include <Arduino.h>` al principio del archivo.

2. *Compilación*: En esta etapa, el código preprocesado es compilado en código de máquina por el compilador de C/C++ (GCC para Arduino). Esto produce un archivo de objeto para cada archivo de código fuente.

3. *Ensamblado*: Los archivos de ensamblador (`.S`), si existen, son convertidos en código de máquina para producir archivos de objeto adicionales.

4. *Enlazado*: Todos los archivos de objeto se enlazan juntos para formar un solo archivo ejecutable. Esto incluye la concatenación de las distintas secciones de código y datos, así como la resolución de las referencias a funciones y variables.

5. *Creación del archivo binario*: Finalmente, se crea un archivo binario a partir del archivo ejecutable. Este archivo binario es lo que se carga en la placa Arduino.

Cada uno de estos pasos es controlado por el IDE de Arduino, que configura y llama a las herramientas de compilación apropiadas en el orden correcto.

## Manuales

- [GNU C Language Introduction and Reference Manual](../pdf/gcc/GNU_C_Language_Introduction_and_Reference_Manual.pdf)
- [The GNU C Library Reference Manual](../pdf/gcc/The_GNU_C_Library_Reference_Manual.pdf)
- [The GNU C Reference Manual](../pdf/gcc/The_GNU_C_Reference_Manual.pdf)

## Recursos

- [GCC y Make](https://isnca.org/es/gcc-y-make/)
- [GNU Compiler Collection](https://es.wikipedia.org/wiki/GNU_Compiler_Collection)
